<h1>EC2 Instance Storage</h1>
<p>EBS : Elastic Block Storage, network drive bound to an AZ</p>
<p>Many EBS : 1 EC2 relationship</p>
<p>Delete on termination:</p>

- [x] root by default
- [ ] yours

<br>

<h3>AMI - Amazon Machine Image</h3>
<ul>
    <li>Customization of an EC2 instance</li>
    <li>Region specific</li>
    <ul>
        <li>Public</li>
        <li>Custom</li>
        <li>AWS Marketplace</li>
    </ul>
</ul>
<br>

<h3>EC2 Image Builder</h3>
<p>Automates the creation, maintenance, validation and testing of EC2s/AMIs</p>
<p>It's a free service that can be run on a schedule</p>
<br>

<h3>EC2 Instance Store</h3>
<p>Better I/O performance</p>
<p>It loses the data if stopped</p>
<br>

<h3>EFS - Elastic File System</h3>
<p>One can be mounted on up to 100 EC2s (Linux/Multi AZ)</p>
<p>EFS-IA
    <ul>
        <li>It can be enabled with a policy</li>
        <li>Cost-saving optimization</li>
    </ul>
</p>
<br>

<h4>Amazon FSx for Windows File Server</h4>
<h4>Amazon FSx for Lustre: file storage for high performance computing in Linux</h4>

| EBS  | EFS  |
| ---  | ---  |
| Not shared | Shared
| Copy | In-sync
|


<h2>Shared Responsibility Model for EC2</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| Back-up/Snapshot settings | Infrastructure
| Data encryption setup | Data replication
| Data on drives | Faulty Hardware Replacement
| EC2 Instance Store Risk Assessment | Ensure Amazon's employees can't access your data