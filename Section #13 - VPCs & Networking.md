<h1>VPC - Virtual Private Cloud</h1>
<p>Region-specific, private network to deploy resources in</p>

<h3>CIDR - Classless Inter-Domain Routing</h3>
<p>It's a method for defining IP address ranges; hence, allocating IP addresses</p>
<p>Used in networking in general, including <b>Security Groups</b></p>
<p>Components:</p>
<ul>
    <li>Base IP: represents an IP address contained in the range (e.g. 192.168.0.0)</li>
    <li>Subnet Mask: defines how many bits can change in the IP address (/8, /16, /24, /32)</li>
</ul>

<h3>Subnet</h3>
<p>Partitioned network within a VPC</p>
<ul>
    <li>Public</li>
    <li>Private</li>
</ul>

<h3>Bastion Hosts</h3>
<p>EC2 instance residing in a public subnet, that allows to SHH into the EC2 instances living in a private subnet</p>

<h3>NACL - Network Access Control List</h3>
<ul>
    <li>Firewall at <b>subnet</b> level</li>
    <li>One NACL per subnet, new subnets are assigned to the defatul NACL</li>
    <li>One can set <b>allow/deny</b> rules. The default inbound/outbound NACLs rules have traffic allowed</li>
    <li>First rule number match will drive the decision (e.g. 100 over 200)</li>
    <li>Stateless</li>
</ul>

<h3>Security Groups</h3>
<ul>
    <li>Firewall at <b>ENI/EC2</b> instance level</li>
    <li>One can set <b>allow/deny</b> rules</li>
    <li>Stateful (The server retains the session info)</li>
</ul>

![image_def]

[image_def]: /images/security-groups-vs-nacls.png "Security Groups vs NACLs"

<h3>Internet Gateway</h3>
<ul>
    <li>Allows resources in a VPC to connect to the Internet</li>
    <li>Only one VPC can be attached to one IGW and vice-versa, and the IGW must be created separately from the VPC</li>
    <li><b>Note</b>: IGWs do not allow Internet access without the route tables definition</li>
</ul>

<h3>NAT Gateway</h3>
<ul>
    <li>Allows your private subnet to access the Internet, while remaining private</li>
    <li>It gets created in a specific AZ, and uses an elastic IP address</li>
    <li>It requires an Internet Gateway</li>
    <li>It cannot be used by an EC2 instance from the same subnet (does not actually make sense)</li>
</ul>

<h3>Transit Gateway</h3>
<p>Allows one to interconnect VPCs and on-prem networks</p>

<h3>Egress-only Internet Gateway</h3>
<ul>
    <li>Allows instances in one's VPC outbound connections over IPv6, while preventing the Internet to
    initiate an IPv6 connection to one's EC2 instances</li>
    <li>Route tables must be updated</li>
</ul>

<h3>VPC Flow Logs</h3>
<ul>
    <li>Enables one to capture IP traffic information from/to network interfaces in a VPC, subnet and ENIs</li>
    <li>Helps monitor & troubleshoot connectivity issues</li>
</ul>

<h3>VPC Peering</h3>
<ul>
    <li>Connects 2 VPCs privately, using AWS' network. It makes them behave as if they were in the same one</li>
    <li>The VPCs must not have overlapping CIDRs</li>
    <li><b>Note</b>:One must update the route tables in each VPC's subnets, to ensure communication between the EC2 instances</li>
</ul>

<h3>VPC Endpoints</h3>
<ul>
    <li><b>Resource</b> to connect a service to a VPC, using a private network (powered by PrivateLink)
    </li>
    <li>They can remove the need of an IGW, NATGW to access AWS services</li>
</ul>

<h3>PrivateLink</h3>
<p><b>Technology</b> that allows to privately connect services to a VPC. It is the most
secure and scalable way to expose a service to a VPC</p>

<h3>Site-to-Site VPN</h3>
<ul>
    <li>Enables access to one's on-prem network through a Virtual Private Gateway </li>
    <li>Route Propagation must be enabled for the Virtual Private Gateway in the subnet's route table</li>
    <li>VPN CloudHub: for multiple VPN connections, it provides secure communication between them (over the public Internet)</li>
</ul>
<p></p>
<p></p>

<h3>Client VPN</h3>
<p>Enables secure access to resources within both AWS and one's on-prem network</p>

<h3>DX - Direct Connect</h3>
<ul>
    <li>Dedicated private physical connection between on-prem to AWS' network</li>
    <li>In-transit data is not encrypted, but it is private</li>
</ul>

<h3>VPC Traffic Mirroring</h3>
<ul>
    <li>Allows one to capture and inspect network traffic in a VPC in a non-intrusive way</li>
</ul>

<h3>Network Firewall</h3>
<ul>
    <li>Protects one's entire VPC</li>
    <li>Provides layer 3 to layer 7 protection</li>
    <li>Any type of traffic direction can be inspected:</li>
        <ul>
            <li>VPC to VPC</li>
            <li>Inbound from Internet</li>
            <li>Outbound to Internet</li>
            <li>Between Direct Connect & Site-to-Site VPN</li>
        </ul>
    <li>It internally uses a Gateway Load Balancer</li>
    <li>Rules can be centrally cross-acount managed to apply to many VPCs</li>
</ul>

<h3>IP Addresses</h3>
<ul>
    <li>Private IPv4: static IP address</li>
    <li>Elastic IP: attach an static IP address to an EC2 instance</li>
    <li>Public IPv6</li>
</ul>
