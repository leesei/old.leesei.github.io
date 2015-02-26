title: SSH
toc: true
date: 2014-12-17 13:45:59
tags:
- shell-tool
- ssh
---

## password-less login

http://www.thecomputerkid.com/2013/07/password-less-ssh.html

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

http://www.marksanborn.net/howto/bypass-firewall-and-nat-with-reverse-ssh-tunnel/

## sshfs

http://www.howtogeek.com/howto/ubuntu/how-to-mount-a-remote-folder-using-ssh-on-ubuntu/
[How to mount a remote directory over ssh on Linux - Xmodulo](http://xmodulo.com/how-to-mount-remote-directory-over-ssh-on-linux.html)

```sh
# install sshfs (once)
sudo apt-get install sshfs

# mount sshfs
sshfs user@yourdomain.com:/path/to/remote local/path

# unmount sshfs
fusermount -u local_mountpoint
```
