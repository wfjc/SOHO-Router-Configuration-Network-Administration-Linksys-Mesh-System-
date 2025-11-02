# SOHO-Router-Configuration-Network-Administration-Linksys-Mesh-System-
A project that shows how to configure a Linkysys SOHO router and carry out basic network administration like changing wifi password, setting guest wifi, reserving DHCP lease, port forwarding and basic management/admin


<h1>SOHO-Router-Configuration-Network-Administration-Linksys-Mesh-System</h1>

<h2>Description</h2>
This project I perform basic networking administration and configuration on my Linkysys router. We have a mesh system set up so that there are additional child nodes and a TP-link extender set up to cover the house. Our ISP is Gigaclear.
I'm going to carry out:
1. Management and DHCP lease reserving
2. WiFi set up to include a SSID name change and setting up a Guest Wifi
3. Basic port forwarding
4. Testing and reflection
<br />


<h2>Utilities Used</h2>

- <b>Mac Terminal</b> 
- <b>Linksys iphone smart wifi app</b>

<h2>Environments Used </h2>

- <b>Iphone 13</b> (21H2)
- <b>Macbook Air 2020</b> (21H2)

  
<h2>Project walk-through:</h2>

<p align="center">
So because we have Linksys at home, I have to do the configuration and management itself on my iphone. Here is the main page from the app showing the router and the child nodes: <br/>
<img src="https://i.postimg.cc/WpZxJCRQ/1-showing-router-set-up.png" height="40%" width="40%" alt="Open command ready drive"/>
<img src="https://i.postimg.cc/nrq5bjY3/2-child-nodes.png" height="40%" width="40%" alt="Open command ready drive"/>
<br />
<br />
Now I wanted to reserve a DHCP lease. In this app I couldn't find a way to reserve a lease manually for my Macbook air, so could only select what was offered at 192.168.1.135
I tried to find a way to set my own lease number in but just couldn't find one. The Local network DHCP settings show that the range is between 192.168.1.10 and 192.168.1.254, so I know at least I am reserved in that pool range:  <br/>
<img src="https://i.postimg.cc/DfGRbHVH/3-DHCP-reserving.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/DfGRbHVR/4-Local-network-dhcp-settings.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />


Now that I have changed the reserved lease, I restarted my macbook and opened the Terminal to verify that I can still connect to the network and to the internet beyond. I pinged both 192.168.1.1 and Google's web server. Connection works still:  <br/>
<img src="https://i.postimg.cc/v8nC6kFZ/5-Mac-Terminal-testing-connectivity.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Next I wanted to create a guest Wifi. It's my families network and this hadn't been configured by the engineer who installed the system. I made a new network so that it's separate from our home wifi and adds an element of network segmentation, better for security:  <br/>
<img src="https://i.postimg.cc/gch16QFj/6-Creating-Guest-Segmentation.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here just shows me checking that the router created the guest network and it's showing up in my macs wifi list. It's under 'Choblet Guest access' and is showing correctly:  <br/>
<img src="https://i.postimg.cc/gch16QFJ/7-Guest-network-appearing-success.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now I wanted to configure some single port forwarding. I picked Remote Desktop Protocol RDP 3389 as an example so that I could control a PC remotely if needed, selecting TCP for sure delivery of data. I also made sure to disable the port afterwards for security:  <br/>
<img src="https://i.postimg.cc/QN7vWwGB/8-Port-Forwarding.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
