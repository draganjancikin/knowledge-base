# SSH

<https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows>

## Content Index

* [What is SSH](#what-is-ssh)
* [How to Install an OpenSSH server](#how-to-install-an-openssh-server)
* [How to Generate a SSH key](#how-to-generate-a-ssh-key)
* [Back up MySQL via SSH](#back-up-mysql-via-ssh)

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
# 
$ ssh your_username@host_ip_address
# 
$ ssh -Pnumber_of_port your_username@host_ip_address
```

## How to Generate a SSH key

```bash
# Generate a RSA key pair
$ ssh-keygen
```

## Back up MySQL via SSH

Use mysqldump to export your database:

```bash
# first login to remote server

# username is the username you can log in to the database with
# database_name is the name of the database to export
# data-dump.sql is the file in the current directory that stores the output.
$ mysqldump -u username -p database_name > data-dump.sql

# download db with secure copy (scp)
$ scp -Pport_number user_name@host_name:folder_name/file_name.sql /folder_name/file_name.sql
```
