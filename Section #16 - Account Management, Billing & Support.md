<h1>Account Management, Billing & Support</h1>

<h3>AWS Organizations</h3>
<p>Central management for multiple AWS accounts</p>
<ul>
    <li>Account creation automation</li>
    <li>Consolidated billing (master / child accounts)</li>
    <ul>
        <li>One bill</li>
        <li>Combined usage. Share:</li>
        <ul>
            <li>Volume pricing</li>
            <li>Reserved instances</li>
            <li>Discount plans</li>
        </ul>
    </ul>
    <li>Restrain accounts' privileges using <i>Service Control Policies (SCP)</i>. SCP is hierarchical, based on strategies (grant/deny)</li>
</ul>

<h3>Control Tower</h3>
<p>Set up and govern multi-account AWS environments</p>

<h3>RAM - Resource Access Manager</h3>
<p>Share resources and avoid duplication</p>

<h3>Service Catalog</h3>
<p>Products created by admins for users' usage</p>

<h3>Pricing models</h3>
<ul>
    <li>Pay as-you-go</li>
    <li>Save when you reserve</li>
    <li>Pay less by using more</li>
    <li>Pay less as AWS grows</li>
    <li>Free services and free tier</li>
</ul>

<h3>Compute Pricing</h3>
<ul>
    <li>EC2: pay for usage (running instances)</li>
    <li>Lambda: pay per call and duration</li>
    <li>ECS: pay for AWS created and stored resources</li>
    <li>Fargate: pay for vCPU and memory resources on containers</li>
    <li>S3: depends on storage class, number and size of objects; number and type of requests,
    data transfer out, and acceleration</li>
    <li>EFS: similar to S3</li>
    <li>EBS: based on volume and size</li>
    <li>RDS: per-hour billing, depending on characteristics</li>
    <li>CloudFront: depends on geographic location and usage</li>
</ul>

<h3>Networking costs</h3>
<p>Maximize private IP addresses and same AZ for savings</p>

<h3>Saving Plans</h3>
<p>Commit to spending a certain amount for the next 1-3 years</p>
<ul>
    <li>EC2 savings plan</li>
    <li>Compute savings plan</li>
    <li>ML savings plan</li>
</ul>

<h3>Compute Optimizer</h3>
<p>Reduce cost and improve performance by recommending optimal resources</p>

<h3>Billing and Cost Management Tools</h3>
<ul>
    <li>Estimate costs on the Cloud:</li>
    <ul>
        <li>Pricing calculator</li>
    </ul>
    <li>Track costs on the Cloud:</li>
    <ul>
        <li>Billing Dashboard</li>
        <li>Cost allocating tag</li>
    </ul>
    <li>Monitor cost plans</li>
    <li>Choose optimal savings plan and forecast usage:</li>
    <ul>
        <li>Cost Explorer</li>
        <li>Cost Usage Reports</li>
    </ul>
</ul>

<br>
<p>Note: Billing data metric in CloudWatch is store only in <i>us-east-1</i> (worldwide costs, still)</p>

<h3>AWS Budgets</h3>
<p>Sends alarms when costs exceed the budget</p>

<h3>Cost Anomaly Detection</h3>
<p>ML-powered continuos monitor for detecting unusual spending</p>

<h3>Services Quotas</h3>
<p>Notifies when one is close to an established service quota</p>

<h3>Trusted Advisor</h3>
<p>High-level account assessments, gouped by 6 categories</p>

<h3>Support Plans Pricing</h3>
<ul>
    <li>Basic Support Plan</li>
    <li>Developer Support Plan</li>
    <ul>
        <li>Basic +</li>
        <li>Business hours email access</li>
        <li>Better response time</li>
    </ul>
    <li>Business Support Plan (24/7)</li>
    <p>For production workloads</p>
    <ul>
        <li>Trusted advisor</li>
        <li>24/7 phone, email and chat</li>
        <li>Production response time</li>
    </ul>
    <li>Enterprise On-Ramp (24/7)</li>
    <p>For production or business critical workloads</p>
    <ul>
        <li>Business Support Plan (24/7) +</li>
        <li>Pool of technical account managers (TAM)</li>
        <li>Concierge support team</li>
        <li>Infrastructure event management, operations reviews</li>
        <li>Business-critical response time</li>
    </ul>
    <li>Enterprise Support Plan (24/7)</li>
    <p>Mission critical workloads</p>
    <ul>
        <li>Business Support Plan (24/7) +</li>
        <li>Designated technical account manager (TAM)</li>
    </ul>
</ul>
