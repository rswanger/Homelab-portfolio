Once you've built the Virtual Machine according to image below

![[Pasted image 20260813154538.png]]

turn on the VM and let it begin. The first prompt is an end user agreement. If you agree to the terms and wish to continue hit Accept.

This leads you to the next prompt, Install or Rescue Shell. Since we are here to install PFSense that is what we will be pressing. That will bring us to the next prompt setting up the network. 

It's going to give you 2 options em0 or em1 if you configured this vm to have 2 network cards as shown in the above image. You will notice it gives you the mac address to each card. If you aren't sure which is which you can find the mac addresses under the advance tab in the virtual machine options. 

![[Pasted image 20260813144635.png]]

Once you know which one is your bridged adapter select that option as the WAN (Wide Area Network)

First page is do we want to have this adapter set as a DHCP Client? Since this is our bridged adapter and we are going to actually be able to touch the internet from here we want to make sure that option is selected. if interface mode does not say DHCP (client) go into that option and change it. 

Right now we are going to leave Use Local Resolver as False. In a future version we will tackle having PFSense handle its own DNS query's but for now we'll leave it up to our home router.

![[Pasted image 20260813145821.png]]

Next we configure the LAN interface. The thing to remember for this is this one is not internet facing, this is our intranet network. There should only be one adapter left em1. 

![[Pasted image 20260813150237.png]]

This will bring you to a similar screen as it did for the WAN but this one is a little different. It should populate the information, which is correct but we'll go over it anyway. 

![[Pasted image 20260813152137.png]]

Since this is a simple homelab and we don't want the other machines not being able to find pfSense on the chance our system resets, we're going to keep the interface mode as Static. Tagging is disabled because again this is just small business setup the IP address and DHCPD ranges are correct. we want anything from 192.168.1.100-199 to be given out as ip addresses. Since we only have 4 machines 2 of which will have their own static ip's we won't run into any ip conflicts in the future. This page is complete. If yours populated with anything different just make the changes needed to match it up.

Next verify that em0 is WAN and em1 is LAN and continue

Let the installer verify your internet connection, select install ce software (unless you wanted to pay for pfsense plus but if you're reading this you're probably not there yet)

![[Pasted image 20260813154836.png]]

This can be left alone. The only thing you might change would be ZFS to UFS if you have a very limited amount of Ram.

We're not setting up a Raid system so this is fine the way it is.

Continue through, select the drive we prepared and commit. I'm choosing the current stable version of pfSense CE

Hit ok and let it install.

Congratulations! You've just installed pfSense.





JUST KIDDING there's more

![[Pasted image 20260813165108.png]]![[Pasted image 20260813165204.png]]