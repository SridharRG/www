+++
title = "Hosted my first website on Server"

[taxonomies]
tags = ["server", "blog"]

[extra]
toc = false 
+++

There is overwhelming amount of options today for deploying something to the Internet. We have got some PaaS like fly.io and heroku that allow us to deploy worldwide with simple commands. Also there is platform like Neocites that expose our static stie and there is Bearblog and Pika exclusively for blogging

But I want to learn the basics of renting a virtual private server(VPS), configuring it and running my own site, which gives me yet another cool feeling beyond words. Is learning the nitty-gritty of server setup obsolete these days? Maybe, but it's fun! So this is why I'm going to spend the rest of this blog post highlighting my personal checklist for provisioning and hardening a VPS!

### Prerequisites

*First things first* : We need a server to put our website up. My preference for a newbie like me would be renting a Shared CPU - you can get a nice starter server for $5/month - [basic Nanode 1GB](https://www.linode.com/pricing/#compute-shared). If you encounter any doubts or any help regarding this... you can contact my guy Kamalavelan(btw he works for Linode) 

### Connecting to the Server

After the purchase step, you will be provided with a root password for your server, then look around for your IPv4 address. using this you can login to your rental vps from your pc. 

Once you got those both, open up your terminal and `ssh root@SERVER_IP_ADDRESS`. Then you need to enter your root password and hit ENTER (boom). You got into your remote server.

### Basic setup


### Securing the Server

The basic setup is done! Let's secure the server.

First, we're going to disable the option to login as root because that user is too powerful and there's 
no reason to be logging in as it anymore. Open up the `/etc/ssh/sshd_config` file with the nano text editor:

```bash
PermitRootLogin no
```
Save this changes(Ctrl + S) and quit(Ctrl + X)


### Configuring a Web Server

Lets make our website working, 