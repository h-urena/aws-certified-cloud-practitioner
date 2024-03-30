<h1>VPC - Virtual Private Cloud</h1>
<p>Region-specific, private network to deploy resources in</p>

<h3>Subnet</h3>
<p>Partitioned network within a VPC</p>
<ul>
    <li>Public</li>
    <li>Private</li>
</ul>

<h3>NACL - Network Access Control List</h3>
<ul>
    <li>Firewall at <b>subnet</b> level</li>
    <li>One can set <b>allow/deny</b> rules</li>
    <li>Stateless</li>
</ul>

<h3>Security Groups</h3>
<ul>
    <li>Firewall at <b>ENI/EC2</b> instance level</li>
    <li>One can set <b>allow</b> rules</li>
    <li>Stateful (The server retains the session info)</li>
</ul>

<h3>Internet Gateway</h3>
<p>Allows one to connect a VPC to the Internet</p>

<h3>NAT Gateway</h3>
<p>Allows your private subnet to access the Internet, while remaining private</p>

<h3>Transit Gateway</h3>
<p>Allows one to interconnect VPCs and on-prem networks</p>

<h3>VPC Flow Logs</h3>
<p>Enables one to capture IP traffic information from/to network interfaces in a VPC</p>

<h3>VPC Peering</h3>
<p>Connects 2 VPCs privately, using AWS' network</p>

<h3>VPC Endpoints</h3>
<p><b>Resource</b> to connect a service to a VPC, using a private network</p>

<h3>PrivateLink</h3>
<p><b>Technology</b> that allows to privately connect services to a VPC. It is the most
secure and scalable way to expose a service to a VPC</p>

<h3>Site-to-Site VPN</h3>
<p>Enables public access to one's network from one's VPC</p>

<h3>Client VPN</h3>
<p>Enables secure access to resources within both AWS and one's on-prem network</p>

<h3>DX - Direct Connect</h3>
<p>Private physical connection between on-prem to AWS' network</p>
<br>

<p>IP Addresses</p>
<ul>
    <li>Private IPv4: static IP address</li>
    <li>Elastic IP: attach an static IP address to an EC2 instance</li>
    <li>Public IPv6</li>
</ul>
