<h1>EC2 - Elastic Compute Cloud</h1>

<h2>Amazon EC2 - Elastic Compute Cloud - IaaS</h2>
<ul>
    <li>Virtual Machines (EC2)</li>
    <li>Virtual Drives (EBS)</li>
    <li>Load Balancer (ELB)</li>
    <li>Auto Scaling (ASG)</li>
</ul>
<br>

<h3>Security Groups (Firewalls)</h3>
<p>Allows rules referenced by IP address or security group</p>
<ul>
    <li>It can be assigned to multiple instances</li>
    <li>It can also be assigned by Region/VPC combination</li>
    <li>It lives outside of the EC2 instance</li>
    <li>Inbound traffic blocked by default</li>
    <li>Outbound traffic allowed by default</li>
</ul>
<p>Notes</p>
<ul>
    <li>Create one SG exclusively for SSH</li>
    <li>Time out = likely a SG issue</li>
</ul>

|   |   |
| --------  | ---  |
| SSH | Port 22 (Linux) |
| FTP | Port 21 |
| SFTP | Port 22 |
| HTTP | Port 80 |
| HTTPS | Port 443 |
| RDP | Port 3389 (Windows) |

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
<br>

<h2>Shared Responsibility Model for EC2</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| Security Groups | Infrastructure |
| OS and Software Maintenance | Physical Hosts Isolation |
| IAM | Faulty Hardware Replacement |
| Data Security | Compliance Validation |
