# Docksal: Installation 

Content index:

* [Install on Ubuntu-Debian Linux](#install-on-ubuntu-debian-linux)

## Install on Ubuntu-Debian Linux

System prerequisites:
* RAM requirement: 8GB or more.
* CPU with SSE4.2 instruction set supported
  ```bash
  # If you get output from the following command, then your CPU is good to go
  $ cat /proc/cpuinfo | grep sse4_2
  ```
* The installer script (get.docksal.io) requires administrative privileges to complete the installation.
* If have Apache installed and his listen 0.0.0.0:80 and 0.0.0.0:443 you must do any of following things:
  * Reconfigure Apache to listen on different host (e.g., 127.0.0.1:80 and 127.0.0.1:443)
  * Reconfigure Apache to listen on different ports (e.g., 8080 and 4433)
  * Stop and disable Apache
* You need another software:
  * curl
  * sudo

Instalation script:

```bash
# Run in terminal
$ bash <(curl -fsSL https://get.docksal.io)
```
