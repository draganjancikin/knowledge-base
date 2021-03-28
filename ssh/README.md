# SSH

<https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows>

## Content Index

* [What is SSH](#what-is-ssh)
* [How to Install an OpenSSH server](#how-to-install-an-openssh-server)
* [How to Generate a SSH key](#how-to-generate-a-ssh-key)

## What is SSH?

Secure Shell is a protocol which allows you to connect securely to a remote computer by using a text-based interface.

When a secure SSH connection is established, a shell session will be started, and you will be able to manipulate the server by typing commands within the client on your local computer.

You need SSH client.

```bash
# Check if SSH client instaled on your computer
$ ssh
# If the client is installed, you will receive a response that looks like this:
usage: ssh [-1246AaCfGgKkMNnqsTtVvXxYy] [-b bind_address] [-c cipher_spec]
[-D [bind_address:]port] [-E log_file] [-e escape_char] ...
# Check version
$ ssh -V
```

## How to Install an OpenSSH server

```bash
$ sudo apt update
$ sudo apt install openssh-server

# Check SSH server status
$ sudo systemctl status ssh
```

## How to Connect via SSH

```bash

```

## How to Generate a SSH key

```bash
# Generate a RSA key pair
$ ssh-keygen


```
