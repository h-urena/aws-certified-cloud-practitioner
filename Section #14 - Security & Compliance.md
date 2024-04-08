<h1>Cloud Monitoring</h1>

<p>Protection and mitigation against DDoS attacks</p>
<ul>
    <li>AWS Shield: Protection against DDoS</li>
    <ul>
        <li>Standard (default)</li>
        <li>Premium ($3000)</li>
    </ul>
    <li>AWS WAF: Firewall</li>
    <li>CloudFront and Route 53</li>
</ul>

<h3>AWS Network Firewall</h3>
<p>Full VPC protection</p>

<h3>AWS Firewall Manager</h3>
<p>VPC security rules and WAF rules that apply to all resources from all accounts</p>

<h3>KMS - Key Management Services</h3>
<p>Encryption for an AWS service. Key types:</p>
<ul>
    <li>Customer managed</li>
    <li>AWS managed (e.g. aws/s3, aws/ebs)</li>
    <li>AWS owned</li>
    <li>Cloud HSM</li>
</ul>

<h3>Cloud HSM</h3>
<p>Encryption's hardware</p>

<h3>ACM - AWS Certificate Manager</h3>
<p>Provision, manage and deploy SSL/TLS certificates</p>

<h3>Secrets Manager</h3>
<p>Store and force rotation opf secrets in RDS</p>

<h3>AWS Artifact</h3>
<p>Portal to access AWS compliance documentations and AWS agreements</p>

<h3>GuardDuty</h3>
<p>Provision, manage, and deploy SSL/TLS certificates</p>

<h3>Inspector</h3>
<ul>
    <li>Automated security assesments for EC2, Lambda and ECR</li>
    <li>Reporting and integration with AWS Security Hub</li>
    <li>Findings are sent to Event Bridge</li>
</ul>

<h3>AWS Config</h3>
<p>Records configuration and changes for compliance</p>

<h3>Macie</h3>
<p>ML-powered service to discover sensitive data (PII)</p>

<h3>Security Hub</h3>
<ul>
    <li>Central security tool to manage security access AWS accounts and automate security checks</li>
    <li>AWS Config service must be enabled</li>
</ul>

<h3>Detective</h3>
<p>Deeper analysis on root causes</p>

<h3>Abuse</h3>
<p>Send reports to a focused AWS team to handle these types of issues</p>

<h3>IAM Access Analyzer</h3>
<ul>
    <li>Find out which resources are shared externally</li>
    <li>Enables one to define a zone of trust</li>
</ul>

<h3>Root User Privileges</h3>
<p>Has complete access to all AWS services and resources. Main actions:</p>
<ul>
    <li>Change account settings</li>
    <li>Close an AWS account</li>
    <li>Change or cancel a support plan</li>
    <li>Register as a seller in the Marketplace</li>
    <li>etc</li>
</ul>

<h2>Shared Responsibility Model</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| Security IN the Cloud | Security OF the Cloud |

<h3>Shared</h3>
<ul>
    <li>Patch management</li>
    <li>Configuration management</li>
    <li>Awareness and Training</li>
</ul>

<br>
<p>Note: PenetrationTesting, anything that looks like an attack is unauthorized</p>
