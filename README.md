<h1> DHCP Installation and setup on Member Server MS1</h1>
<h3>*To install DHCP using Powershell</h3>
<p>1. Opened power shell on your server and typed the following command; <b><i>“Install-WindowsFeature DHCP -IncludeManagementTools”</i></b> and hit enter.
This will take some times to install, just had to wait for it and then was shown a Success message and the Feature results of what was installed.</p>
<p align="center"><img src="https://i.imgur.com/qjqliVM.png" height="50%" width="50%" alt="image"/>

<p>2. To confirm that DHCP is installed, then to server manager-dashboard, clicked on Tools and checked the list and there is DHCP sitting pretty</p>
<p align="center"><img src="https://i.imgur.com/rIkwRn3.png" height="50%" width="50%" alt="image"/>
<p align="center"><img src="https://i.imgur.com/GIi21Y7.png" height="50%" width="50%" alt="image"/>

<br>
<br>

<h3>*To Assign DHCP Scope</h3>
<p>1. Opened power shell on your server and typed in the following command;<b><i> “Add-DhcpServerv4Scope -Name "Hyper V Scope" -StartRange 192.168.10.130 -EndRange 192.168.10.135 -SubnetMask 255.255.255.0”.</i></b> Where Name parameter = The descriptive name you want to give the scope, Start Range and End Rage = The range between the IP addresses available for lease to Dhcp clients, and Subnet mask = subnet mask of your IP address. </p>
<p align="center"><img src="https://i.imgur.com/QuBjDfg.png" height="50%" width="50%" alt="image"/>

<p>2. To confirm this, I opened DHCP on the Server and expand IPv4, then expandeded Scope and clicked on the Address Pool to verify the assigned IP range I configured using powershell command, and there it is.</p>
<p align="center"><img src="https://i.imgur.com/M4BYy4Z.png" height="50%" width="50%" alt="image"/>

<br>




