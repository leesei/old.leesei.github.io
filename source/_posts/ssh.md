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

[ssh-keygen - man page](https://www.mankier.com/1/ssh-keygen)

[Generating SSH keys - User Documentation](https://help.github.com/articles/generating-ssh-keys/)
[Working with SSH key passphrases - User Documentation](https://help.github.com/articles/working-with-ssh-key-passphrases/)

[Understanding the SSH Encryption and Connection Process | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-the-ssh-encryption-and-connection-process)
[SSH Essentials: Working with SSH Servers, Clients, and Keys | DigitalOcean](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys)

[ssh-agent(1): authentication agent - Linux man page](https://linux.die.net/man/1/ssh-agent)
`ssh-add`

[Hardening SSH with 2fa](https://gist.github.com/lizthegrey/9c21673f33186a9cc775464afbdce820)
[SSH Honey Keys](https://kulinacs.com/ssh-honey-keys/amp/)

[How to use multiplexing to speed up the SSH - TechRepublic](https://www.techrepublic.com/google-amp/article/how-to-use-multiplexing-to-speed-up-the-ssh/)
[networking - How can I specify a local port when establishing SSH connections? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/526745/how-can-i-specify-a-local-port-when-establishing-ssh-connections)

## `ssh_config`

[Using the SSH Config File | Linuxize](https://linuxize.com/post/using-the-ssh-config-file/)
[Simplify Your Life With an SSH Config File | Nerderati](http://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/)
[OpenSSH Config File Examples – nixCraft](https://www.cyberciti.biz/faq/create-ssh-config-file-on-linux-unix/)
[ssh_config(5): OpenSSH SSH client config files - Linux man page](https://linux.die.net/man/5/ssh_config)

[moul/advanced-ssh-config: make your ssh client smarter](https://github.com/moul/advanced-ssh-config)

## password-less login

[The Computer Kid: Password-less SSH](http://www.thecomputerkid.com/2013/07/password-less-ssh.html#.VR4fbemUdhE)

You can specify host alias, user and id in `~/.ssh/config`:

```
Host 64.28
    HostName 10.6.64.28
    User kylee
    IdentityFile ~/.ssh/kylee.id_rsa
```

I now use this setting instead of multiple global `IdentityFile` entries.

Also see `ssh-copy-id` command instead of using `scp` as below.
It handles pushing public key to server and properly setting the permissions of the key.

With CA signed cert and not personal SSH cert
[SSH Recipes in Go — An interlude – Tarka Labs Blog – Medium](https://medium.com/tarkalabs/ssh-recipes-in-go-an-interlude-6fa88a03d458)
[Signed SSH Certificates - SSH - Secrets Engines - Vault by HashiCorp](https://www.vaultproject.io/docs/secrets/ssh/signed-ssh-certificates.html)
[Improving security by drawing identicons for SSH keys - DEV Community 👩‍💻👨‍💻](https://dev.to/krofdrakula/improving-security-by-drawing-identicons-for-ssh-keys-24mc)

### on client

```sh
# generate ssh key pair (if you don't have one)
ssh-keygen -t rsa
# generate key with no passphrase
ssh-keygen -t rsa -b 4096 -f privateKey.pem -N ""

# scp requires next step on server
scp ~/.ssh/id_rsa.pub user@server:~/.ssh/

# or ssh-copy-id, no need to chmod on server
ssh-copy-id user@server
ssh-copy-id -i ID_FILE user@server
```

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
```

## SSH Tunneling

[SSH Tunneling Explained | Source Open](https://chamibuddhika.wordpress.com/2012/03/21/ssh-tunnelling-explained/)
[Bypass Firewall and NAT with Reverse SSH Tunnel - MarkSanborn.net](http://www.marksanborn.net/howto/bypass-firewall-and-nat-with-reverse-ssh-tunnel/)
[SSH tunnels for fun and profit](https://underthehood.myob.com/ssh-tunnels-for-fun-and-profit/)
[Power of SSH Tunneling – Tarka Labs Blog – Medium](https://medium.com/tarkalabs/power-of-ssh-tunneling-cf82bc56da67)
[Access web pages through your home network via SSH](https://coolaj86.com/articles/access-web-pages-through-your-home-network-via-ssh/)
[SSH Tunneling - Poor Techie's VPN | Linux Journal](https://www.linuxjournal.com/content/ssh-tunneling-poor-techies-vpn)
[Set Up SSH Tunneling on a Linux - Unix - BSD Server To Bypass NAT](http://www.cyberciti.biz/faq/set-up-ssh-tunneling-on-a-linux-unix-bsd-server-to-bypass-nat/)
[ssh tunnelling Archives - Everything CLI](https://www.everythingcli.org/tag/ssh-tunnelling/)
[The power of SSH tunneling. How it can make your developer life easier](https://medium.com/swlh/the-power-of-ssh-tunneling-how-it-can-make-your-developer-life-easier-17ea6e8ee8ea)

[GitHub - sshuttle/sshuttle: Transparent proxy server that works as a poor man's VPN. Forwards over ssh. Doesn't require admin. Works with Linux and MacOS. Supports DNS tunneling.](https://github.com/sshuttle/sshuttle)
[sshuttle: where transparent proxy meets VPN meets ssh — sshuttle documentation](https://sshuttle.readthedocs.io/en/stable/)
[How to use SSH as a VPN with sshuttle - TechRepublic](https://www.techrepublic.com/google-amp/article/how-to-use-ssh-as-a-vpn-with-sshuttle/)
[VPN Technologies: A primer](http://tomoconnor.eu/blogish/vpn-technologies-primer/#.VvZp1WF96_4)

[autossh](https://www.harding.motd.ca/autossh/)
[autossh(1): monitor/restart ssh sessions - Linux man page](https://linux.die.net/man/1/autossh)
[AutoSSH Tunnels for Linux | Chartio Support Documentation](https://support.chartio.com/autossh-tunnels-for-linux)
[ctroncoso/alpine-autossh: Persistent SSH tunneling image for Docker](https://github.com/ctroncoso/alpine-autossh)

[ssh -R (reverse tunnel) man page hell – zwischenzugs](https://zwischenzugs.com/2016/05/21/ssh-r-reverse-tunnel-man-page-hell/)

```sh
$ ssh -f -N -L 9906:127.0.0.1:3306 coolio@database.example.com
# -f puts ssh in background
# -N makes it not execute a remote command
# or with config
$ ssh -f -N tunnel
```

```
Host tunnel
    HostName database.example.com
    IdentityFile ~/.ssh/coolio.example.key
    LocalForward 9906 127.0.0.1:3306
    User coolio
```

This will forward all local port `9906` traffic to port `3306` on the remote `dev.example.com` server, letting me point my desktop to `localhost` (`127.0.0.1:9906`) and have it behave exactly as if I had exposed port 3306 on the remote server and connected directly to it.

## SSH Agent Forwarding

Forward your local machine's credential to remote machine.

[How to use SSH properly and what is SSH Agent Forwarding - DEV Community 👩‍💻👨‍💻](https://dev.to/levivm/how-to-use-ssh-and-ssh-agent-forwarding-more-secure-ssh-2c32)

[How to Access a Remote Server Using a Jump Host](https://www.tecmint.com/access-linux-server-using-a-jump-host/amp/)
[How to use SSH to proxy through a Linux jump host - TechRepublic](https://www.techrepublic.com/article/how-to-use-ssh-to-proxy-through-a-linux-jump-host/)

## sshfs

[How to Mount a Remote Folder using SSH on Ubuntu](http://www.howtogeek.com/howto/ubuntu/how-to-mount-a-remote-folder-using-ssh-on-ubuntu/)
[How to mount a remote directory over ssh on Linux - Xmodulo](http://xmodulo.com/how-to-mount-remote-directory-over-ssh-on-linux.html)
[How to use SSHFS to Mount Remote Directories over SSH | Linuxize](https://linuxize.com/post/how-to-use-sshfs-to-mount-remote-directories-over-ssh/)

[How to Use Linux SFTP Command to Transfer Files | Linuxize](https://linuxize.com/post/how-to-use-linux-sftp-command-to-transfer-files/) uses by SSHFS under the hood

```sh
# install sshfs (once)
sudo apt-get install sshfs

# mount sshfs
sshfs user@yourdomain.com:/path/to/remote local/path

# unmount sshfs
fusermount -u local_mountpoint
```
