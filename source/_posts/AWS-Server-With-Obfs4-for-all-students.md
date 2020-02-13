---
title: AWS Server With Obfs4 for all students
date: 2019-05-27 14:29:22
tags: Computer Science
categories: Computer Science
---

# Intro

If you are in college, you might notice some of the websites are blocked(even though they are useful), and you cannot find a proper VPN what is working.
So today, I will teach you how to make your own vpn with obfs4 which allows you to see any websites at school. (Don't use it for bad things, or I will be sad)

## Preparation

- Have any type of linux server that is not blocked. (I'm going to be using a AWS Server or leave a raspberry pi at your house)
- Viscosity(30 day trial, there is a loop hole though on mac, hit: minimize the tab)

## Let's start

Just some advices:
- I personally recommend you to ssh to your server, and if your SSH port(22) is blocked, I recommend you to use the google shell as a "proxy".

If you are using AWS, its ssh -i [pemfile] [user]@[ipv4 address]

#### Step 1:

Get into root by typing sudo su
then:
apt-get update
apt-get upgrade
Depends on the linux OS you are using, the command may vary


#### Step 2:

##### Read this before the following:
- Use TCP instead of UDP
- Set the port number for Openvpn/Pivpn as 1194 because port 443 is used for the obfs4, because thats the only port that most schools do not block.


Attention! if you haven't read the thing on the top, go and read it!
Install Openvpn(not needed if using raspberry pi):
apt-get install openvpn
Install Pivpn(I recommend it, I saves you a lot of time):
curl -L https://install.pivpn.io | bash


#### Step 3:

Install obfs4:
apt-get install obfs4proxy

Obfs4 directory:
mkdir -p /var/lib/tor/pt_state/obfs4

Add config file:
vim /var/lib/tor/pt_state/obfs4/obfs4.config

Add this line into config:
```
TOR_PT_MANAGED_TRANSPORT_VER=1TOR_PT_STATE_LOCATION=/var/lib/tor/pt_state/obfs4TOR_PT_SERVER_TRANSPORTS=obfs4TOR_PT_SERVER_BINDADDR=obfs4-0.0.0.0:443TOR_PT_ORPORT=127.0.0.1:1194
```

Create SystemD:
vim /etc/systemd/system/obfs4proxy.service

Paste this:
```
[Unit]Description=Obfsproxy Server[Service]EnvironmentFile=/var/lib/tor/pt_state/obfs4/obfs4.configExecStart=/usr/bin/obfs4proxy -enableLogging true -logLevelStr INFO[Install]WantedBy=multi-user.target
```

Enable obfs4proxy:
sudo systemctl start obfs4proxysudo systemctl enable obfs4proxy

Get obfs4 key:
cat /var/lib/tor/pt_state/obfs4/obfs4_bridgeline.txt

it should say cert=JKLFDSFKHSDIFHSIUSF(I made this up), but you will find it in ur obfs4_bridgeline.xt file and it is your obfs4 key.

#### Step 4:
create user:
pivpn -a
and follow the steps

by using sftp, get the ovpn file from your ovpns folder.
Note: same as how you connect to your machine, you just replace ssh to sftp
AWS: sftp -i [pemfile] [user]@[ipv4 address]

#### Step 5:
- Import the ovpn file into Viscosity
- Change the port number to 443
- In Transport-obfuscation choose obfs4
- Insert your key from step 3

#### Step 6:
Connect!

## Notes
I really hate adding pictures into my blog, so for all the visual learners, My apologies, but I and ensure you that as long as you carefully follow the steps, you will be free.
