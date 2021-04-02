---
title: Demo upload
parent: IDO-SBC2D70
grand_parent: SSD201
nav_order: 1
---
# Demo Upload

Go to the download directory and write
`scp demo root@192.168.1.15:/root/`
the file is uploaded to the board. 
Note: You have to change the ip address accordingly.

Then `ssh root@192.168.1.15` and you should find the file demo.
Next `chmod 655 demo`

`kill usr/sbin/demo` and any other demo widget running.

Then `./demo`