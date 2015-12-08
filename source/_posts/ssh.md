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

Also see `ssh ssh-copy-id` command

### on client

```sh
# generate ssh key pair (if you don't have one)
ssh-keygen -t rsa

scp ~/.ssh/id_rsa.pub user@server:~/
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

## ssh tunneling

[SSH Tunneling Explained | Source Open](https://chamibuddhika.wordpress.com/2012/03/21/ssh-tunnelling-explained/)
[Bypass Firewall and NAT with Reverse SSH Tunnel - MarkSanborn.net](http://www.marksanborn.net/howto/bypass-firewall-and-nat-with-reverse-ssh-tunnel/)
[SSH tunnels for fun and profit](https://underthehood.myob.com/ssh-tunnels-for-fun-and-profit/)
[Access web pages through your home network via SSH](https://coolaj86.com/articles/access-web-pages-through-your-home-network-via-ssh/)

## sshfs

[How to Mount a Remote Folder using SSH on Ubuntu](http://www.howtogeek.com/howto/ubuntu/how-to-mount-a-remote-folder-using-ssh-on-ubuntu/)
[How to mount a remote directory over ssh on Linux - Xmodulo](http://xmodulo.com/how-to-mount-remote-directory-over-ssh-on-linux.html)

```sh
# install sshfs (once)
sudo apt-get install sshfs

# mount sshfs
sshfs user@yourdomain.com:/path/to/remote local/path

# unmount sshfs
fusermount -u local_mountpoint
```
