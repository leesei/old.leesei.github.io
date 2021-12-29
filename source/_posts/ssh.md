---
title: "SSH"
date: 2014-12-17 13:45:59
categories:
  - app
tags:
  - shell-tool
  - ssh
toc: true
---

[OpenSSH](https://www.openssh.com/)

[Understanding the SSH Encryption and Connection Process | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-the-ssh-encryption-and-connection-process)
[SSH Essentials: Working with SSH Servers, Clients, and Keys | DigitalOcean](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys)
[How to SSH Properly | SSH Security Best Practices | Teleport](https://goteleport.com/blog/how-to-ssh-properly/)
[SSH Handshake Explained | What is SSH Handshake? | Teleport](https://goteleport.com/blog/ssh-handshake-explained/)

[ssh-agent - OpenSSH authentication agent - man page](https://www.mankier.com/1/ssh-agent)
[ssh-add command man page - openssh-clients | ManKier](https://www.mankier.com/1/ssh-add)

[ssh-keygen - man page](https://www.mankier.com/1/ssh-keygen)
[Generating SSH keys - User Documentation](https://help.github.com/articles/generating-ssh-keys/)
[Working with SSH key passphrases - User Documentation](https://help.github.com/articles/working-with-ssh-key-passphrases/)
[How to manage SSH keys? | Teleport](https://goteleport.com/blog/ssh-key-management/)
[Comparing SSH Keys - RSA, DSA, ECDSA, or EdDSA? | Teleport](https://goteleport.com/blog/comparing-ssh-keys/)

[Hardening SSH with 2fa](https://gist.github.com/lizthegrey/9c21673f33186a9cc775464afbdce820)
[SSH Honey Keys](https://kulinacs.com/ssh-honey-keys/amp/)
[DIY Single Sign-On for SSH](https://smallstep.com/blog/diy-single-sign-on-for-ssh/)

[How to use multiplexing to speed up the SSH - TechRepublic](https://www.techrepublic.com/google-amp/article/how-to-use-multiplexing-to-speed-up-the-ssh/)
[networking - How can I specify a local port when establishing SSH connections? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/526745/how-can-i-specify-a-local-port-when-establishing-ssh-connections)

[Mosh: the mobile shell](https://mosh.org/)
[What Is the Mosh Shell and How Do You Use It?](https://www.cloudsavvyit.com/1224/what-is-the-mosh-shell-and-how-do-you-use-it/amp/)
[TimeToogo/tunshell: Remote shell into ephemeral environments 🐚 🦀](https://github.com/TimeToogo/tunshell)

[How To Configure X11 Forwarding Using SSH In Linux - OSTechNix](https://ostechnix.com/how-to-configure-x11-forwarding-using-ssh-in-linux/)

## `ssh_config`

[Using the SSH Config File | Linuxize](https://linuxize.com/post/using-the-ssh-config-file/)
[Simplify Your Life With an SSH Config File | Nerderati](http://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/)
[OpenSSH Config File Examples – nixCraft](https://www.cyberciti.biz/faq/create-ssh-config-file-on-linux-unix/)
[ssh_config(5): OpenSSH SSH client config files - Linux man page](https://linux.die.net/man/5/ssh_config)

[moul/advanced-ssh-config: make your ssh client smarter](https://github.com/moul/advanced-ssh-config)

## password-less login

[The Computer Kid: Password-less SSH](http://www.thecomputerkid.com/2013/07/password-less-ssh.html#.VR4fbemUdhE)
[SSH - Using Keys Instead of Passwords](https://www.marksanborn.net/security/ssh-using-keys-instead-of-passwords/)

You can specify host alias, user and id in `~/.ssh/config`:

```
Host 64.28
    HostName 10.6.64.28
    User kylee
    IdentityFile ~/.ssh/kylee.id_rsa
```

I now use this setting instead of multiple global `IdentityFile` entries.

[Ssh-copy-id for copying SSH keys to servers | SSH.COM](https://www.ssh.com/ssh/copy-id)

Also see `ssh-copy-id` command instead of using `scp` as below.
It handles pushing public key to server and properly setting the permissions of the key.

With CA signed cert and not personal SSH cert
[SSH Recipes in Go — An interlude – Tarka Labs Blog – Medium](https://medium.com/tarkalabs/ssh-recipes-in-go-an-interlude-6fa88a03d458)
[Signed SSH Certificates - SSH - Secrets Engines - Vault by HashiCorp](https://www.vaultproject.io/docs/secrets/ssh/signed-ssh-certificates.html)
[Improving security by drawing identicons for SSH keys - DEV Community 👩‍💻👨‍💻](https://dev.to/krofdrakula/improving-security-by-drawing-identicons-for-ssh-keys-24mc)
[How to Lock Down Your SSH Server](https://www.cloudsavvyit.com/363/how-to-lock-down-your-ssh-server/amp/)

### on client

```sh
ssh-keygen -t rsa -b 4096 -f jwtRS256.key
# Don't add passphrase
openssl rsa -in jwtRS256.key -pubout -outform PEM -out jwtRS256.key.pub
```

```sh
# generate ssh key pair (if you don't have one)
ssh-keygen -t rsa
ssh-keygen -t ed25519 -C <email>
# generate key with no passphrase
ssh-keygen -t rsa -b 4096 -f privateKey.pem -N ""
openssl rsa -in privateKey.pem -pubout -outform PEM -out publicKey.pem
ssh-keygen -f privateKey.pem -e -m pem > publicKey.pem

# scp requires next step on server
scp ~/.ssh/id_rsa.pub user@server:~/.ssh/

# or ssh-copy-id, no need to chmod on server
ssh-copy-id user@server
ssh-copy-id -i ID_FILE user@server
```

[Using ssh-copy-id to install SSH keys on servers as authorized keys for passwordless authentication. Options and troubleshooting.](https://www.ssh.com/academy/ssh/copy-id)

### on server

```sh
# add public key to authorized_keys
cat ~/id_rsa.pub >> ~/.ssh/authorized_keys

# enforce permission settings
chmod 700 ~/.ssh
chmod 640 ~/.ssh/authorized_keys

\rm ~/id_rsa.pub
```

## copying lots of small files

```sh
tar czf - <files> | ssh user@host "cd /wherever && tar xvzf -"
# if the files are not compressible
tar cf - <files> | ssh user@host "cd /wherever && tar xvf -"

git archive --format=tar origin/master | gzip -9c | ssh user@yourserver.com "tar --directory=/var/www -xvzf -"
docker save image | ssh user@yourserver.com "docker import -"
```

## X over ssh

use `-x` to allow remote X content to render locally

```sh
ssh -x SERVER "xclock"
```

## sudo over ssh

use `-t` to allocate pesudo-terminal to enter password

```sh
ssh -t SERVER "sudo COMMAND"
```

## `sshd_config`

[sshd_config is the OpenSSH server configuration file. How to configure and troubleshoot. Avoid getting accidentally locked out of remote server.](https://www.ssh.com/academy/ssh/sshd_config)

## SSH Tunneling

[How an SSH tunnel can bypass firewalls, add encryption to application protocols, and help access services remotely.](https://www.ssh.com/academy/ssh/tunneling)
[Quick-Tip: SSH Tunneling Made Easy](https://www.revsys.com/writings/quicktips/ssh-tunnel.html)
[SSH port forwarding/tunneling use cases and concrete examples. Client command, server configuration. Firewall considerations.](https://www.ssh.com/academy/ssh/tunneling/example)
[SSH Tunneling Explained | Source Open](https://chamibuddhika.wordpress.com/2012/03/21/ssh-tunnelling-explained/)
[The power of SSH tunneling. How it can make your developer life easier](https://medium.com/swlh/the-power-of-ssh-tunneling-how-it-can-make-your-developer-life-easier-17ea6e8ee8ea)
[Howto use SSH local and remote port forwarding | Debian Admin](http://www.debianadmin.com/howto-use-ssh-local-and-remote-port-forwarding.html)
[SSH Tunneling - Local & Remote Port Forwarding (by Example) - YouTube](https://www.youtube.com/watch?v=N8f5zv9UUMI)
[networking - How does reverse SSH tunneling work? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/a/118650) diagrams

`-f` puts ssh in background, implies `-n`
`-n` prevents reading stdin
`-N` disable execution of remote command
`-T` disable pseudo-terminal allocation

Note: domain resolution is done AFTER SSH (on the SSH server).

**Local port forwarding**
allows you to forward a **local** port number to a remote server

```sh
# `localhost:3306` (at `server.com`) is accessable at `localhost:8000`
$ ssh -fNT -L 8000:localhost:3306 user@server.com

# Access `restricted-domain.com:80` via `remote-server.com`, exposed at `localhost:8000`
$ ssh -L 8000:restricted-domain.com:80 user@remote-server.com

$ ssh -fNT-L 9906:127.0.0.1:3306 coolio@database.example.com
```

```sh
# or with config
$ ssh -f -N tunnel

Host tunnel
    HostName database.example.com
    IdentityFile ~/.ssh/coolio.example.key
    LocalForward 9906 127.0.0.1:3306
    User coolio
```

**Remote port forwarding**
forward all requests on a **remote** servers’ port to your machine.
Can also expose SSH server.

```sh
# `localhost:3000` will be accessible at `remote-server.com:8000`
ssh -fNT -R 8000:localhost:3000 user@remote-server.com

# expose SSH server to `proxyserver`
# on target machine (`target`)
ssh -fNT -R 10002:localhost:22 proxyuser@proxyserver

# on client, with GatewayPorts
ssh targetuser@proxyserver -p 10002
# on client, without GatewayPorts
ssh proxyuser@proxyserver
ssh targetuser@localhost:10002

vi /etc/ssh/sshd_config
# set GatewayPorts to yes
```

[Bypass Firewall and NAT with Reverse SSH Tunnel - MarkSanborn.net](http://www.marksanborn.net/howto/bypass-firewall-and-nat-with-reverse-ssh-tunnel/)
[Power of SSH Tunneling. Quoting SSH man page to remind us all… | by Dhruva Sagar | Tarka Labs Blog](https://blog.tarkalabs.com/power-of-ssh-tunneling-cf82bc56da67)
[Access web pages through your home network via SSH](https://coolaj86.com/articles/access-web-pages-through-your-home-network-via-ssh/)
[SSH Tunneling - Poor Techie's VPN | Linux Journal](https://www.linuxjournal.com/content/ssh-tunneling-poor-techies-vpn)
[Set Up SSH Tunneling on a Linux - Unix - BSD Server To Bypass NAT](http://www.cyberciti.biz/faq/set-up-ssh-tunneling-on-a-linux-unix-bsd-server-to-bypass-nat/)
[ssh tunnelling Archives - Everything CLI](https://www.everythingcli.org/tag/ssh-tunnelling/)
[Running a Bokeh server — Bokeh Documentation](https://docs.bokeh.org/en/latest/docs/user_guide/server.html#ssh-tunnels) via ssh tunnel

[sshuttle/sshuttle: Transparent proxy server that works as a poor man's VPN. Forwards over ssh. Doesn't require admin. Works with Linux and MacOS. Supports DNS tunneling.](https://github.com/sshuttle/sshuttle)
[sshuttle: where transparent proxy meets VPN meets ssh — sshuttle documentation](https://sshuttle.readthedocs.io/en/stable/)
[How to use SSH as a VPN with sshuttle - TechRepublic](https://www.techrepublic.com/google-amp/article/how-to-use-ssh-as-a-vpn-with-sshuttle/)
[VPN Technologies: A primer](http://tomoconnor.eu/blogish/vpn-technologies-primer/#.VvZp1WF96_4)
[Linux Fu: VPN For Free With SSH | Hackaday](https://hackaday.com/2020/11/23/linux-fu-vpn-for-free-with-ssh/)

[ssh -R (reverse tunnel) man page hell – zwischenzugs](https://zwischenzugs.com/2016/05/21/ssh-r-reverse-tunnel-man-page-hell/)

[Hacking Windows 10: How to Use SSH Tunnels to Forward Requests & Hack Remote Routers « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/hacking-windows-10-use-ssh-tunnels-forward-requests-hack-remote-routers-0198465/)

```sh
# forwarding `git://` (at port 9418)
$ ssh -L 9418:gitorious.org:9418 your.remote.host
$ git clone git://localhost/path/to/repository.git
```

### Keep alive

[shell - How to keep SSH tunnel alive - Server Fault](https://serverfault.com/questions/823393/how-to-keep-ssh-tunnel-alive)
[ssh tunnel - Prevent closing of SSH Local Port Forwarding - Server Fault](https://serverfault.com/questions/598210/prevent-closing-of-ssh-local-port-forwarding)

[autossh](https://www.harding.motd.ca/autossh/)
[autossh man page - General Commands | ManKier](https://www.mankier.com/1/autossh)
[autossh(1): monitor/restart ssh sessions - Linux man page](https://linux.die.net/man/1/autossh)
[autossh – Automatically restart SSH sessions and tunnels | Debian Admin](http://www.debianadmin.com/autossh-automatically-restart-ssh-sessions-and-tunnels.html)
[ctroncoso/alpine-autossh: Persistent SSH tunneling image for Docker](https://github.com/ctroncoso/alpine-autossh)

For example, if you are using a recent version of OpenSSH, you
may wish to explore using the `ServerAliveInterval` and
`ServerAliveCountMax` options to have the SSH client exit if it
finds itself no longer connected to the server. In many ways
this may be a better solution than the monitoring port.

[JayGoldberg/RSTunnel: A continuation of Reliable SSH Tunnel, to set up and maintain persistent SSH (reverse) tunnels](https://github.com/JayGoldberg/RSTunnel)

You should look into the `ClientAliveInterval` keyword for `sshd_config` and the `ServerAliveInterval` interval for `ssh_config` or `~/.ssh/config`.

```
Host *
ServerAliveInterval 60
```

`ssh -o TCPKeepAlive=yes -o ServerAliveInterval=300`

## SSH Agent Forwarding/Jump Host

Forward your local machine's credential to remote machine.

[SSH Agent Forwarding: How to use SSH properly and what is SSH Agent Forwarding - DEV](https://dev.to/levivm/how-to-use-ssh-and-ssh-agent-forwarding-more-secure-ssh-2c32)

[Using SSH Agent Forwarding | GitHub Developer Guide](https://developer.github.com/v3/guides/using-ssh-agent-forwarding/)
[How to Access a Remote Server Using a Jump Host](https://www.tecmint.com/access-linux-server-using-a-jump-host/amp/)
[How to use SSH to proxy through a Linux jump host - TechRepublic](https://www.techrepublic.com/article/how-to-use-ssh-to-proxy-through-a-linux-jump-host/)
[OpenSSH/Cookbook/Proxies and Jump Hosts - Wikibooks, open books for an open world](https://en.wikibooks.org/wiki/OpenSSH/Cookbook/Proxies_and_Jump_Hosts#Jump_Hosts_--_Passing_Through_a_Gateway_or_Two)
[Tutorial for setting up an SSH Jump Server | Teleport](https://goteleport.com/blog/ssh-jump-server/)
[Self healing reverse SSH setup with systemd](https://blog.stigok.com/2018/04/22/self-healing-reverse-ssh-systemd-service.html)
[SSH ProxyCommand example: Going through one host to reach another server - nixCraft](https://www.cyberciti.biz/faq/linux-unix-ssh-proxycommand-passing-through-one-host-gateway-server/)

[SSH Agent forwarding using different usernames and different keys - Super User](https://superuser.com/questions/1140830/ssh-agent-forwarding-using-different-usernames-and-different-keys/1141035#1141035)
[What is SSH Agent Forwarding and How Do You Use It?](https://www.cloudsavvyit.com/25/what-is-ssh-agent-forwarding-and-how-do-you-use-it/amp/)
