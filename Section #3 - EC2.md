<h1>EC2 - Elastic Compute Cloud</h1>

<h2>Amazon EC2 - Elastic Compute Cloud - IaaS</h2>
<ul>
    <li>Virtual Machines (EC2)</li>
    <li>Virtual Drives (EBS)</li>
    <li>Elastic Load Balancer (ELB)</li>
    <li>Auto Scaling Group (ASG)</li>
</ul>
<br>

<h3>Security Groups (Firewalls on EC2 Instances)</h3>
<p>Allows rules referenced by IP address or security group. They regulate:</p>
<ul>
    <li>Access to ports</li>
    <li>Authorized IP ranges - IPv4 and IPv6</li>
    <li>Inbound network (from "other" to the instance)</li>
    <li>Outbound network (from the instance to "other")</li>
</ul>

<p>Notes</p>
<ul>
    <li>It can be assigned to multiple instances</li>
    <li>Locked down to a specific region/VPC combination</li>
    <li>It lives outside of the EC2 instance</li>
    <li>Create one SG exclusively for SSH</li>
    <li>Time out = likely a SG issue</li>
    <li>Inbound traffic blocked by default</li>
    <li>Outbound traffic allowed by default</li>
</ul>

|   |   |
| --------  | ---  |
| SSH | Port 22 (Linux instance) |
| FTP | Port 21 |
| SFTP | Port 22 (Files upload using SSH) |
| HTTP | Port 80 |
| HTTPS | Port 443 |
| RDP | Port 3389 (Windows instance) |

<h3>EC2 Spot Instances</h3>
<ul>
    <li>Most cost-efficient option</li>
    <li>Not suitable for critical jobs or DBs</li>
</ul>

<h3>EC2 Dedicated Instances</h3>
<ul>
    <li>Reservation and access of a physical server</li>
</ul>

<h3>EC2 Dedicated Host</h3>
<ul>
    <li>For compliance/license requirements</li>
    <li>Most expensive option</li>
</ul>

<h3>EC2 User Data</h3>
<p>Allows one to bootstrap (launch commands when a machine starts) EC2 instances, such as:</p>
<ul>
    <li>Install updates</li>
    <li>Install software</li>
    <li>Files download/upload</li>
    <li>Anything one can think of</li>
</ul>

<h3>ENI - Elastic Network Interfaces</h3>
<ul>
    <li>Logical component in a VPC, that represents a virtual network card</li>
    <li>One can create ENIs and attach them on to EC2 instances on-the-fly (for failover)</li>
    <li>They are bound to a specific AZ</li>
</ul>
<br>

<h2>Shared Responsibility Model for EC2</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| Security Groups | Infrastructure |
| OS and Software Maintenance | Physical Hosts Isolation |
| IAM | Faulty Hardware Replacement |
| Data Security | Compliance Validation |
