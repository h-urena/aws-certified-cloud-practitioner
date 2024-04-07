<h1>S3: Simple Storage Service</h1>

<p><b>S3 buckets must have globally unique names</b></p>
<p><b>They're global</b>, but created in a region</p>
<p>Files are actually <b>objects</b>, which have a key, which is composed of their full path</p>
<p>Objects larger than 5GBs in size must be uploaded using the multi-part functionality</p>
<p>Versioning is an optional setting provided as part of the service</p>

<h3>Security</h3>

| Resource-Based | User-Based |
| --------------  | --------  |
| Bucket Policies | IAM Policies |
| Object Access Control List | |
| Bucket Access Control List | |
<br>

<p><b>Replication:</b> optional setting that requires versioning to be enabled to become available</p>
<ul>
    <li>Cross-Region Replication</li>
    <li>Same-Region Replication</li>
</ul>

<h3>Storage Classes</h3>

<p>All classes take into the account these two considerations:</p>
<p><b>- Durability:</b> possibility of loss</p>
<p><b>- Availability:</b> how readily the object is</p>

<p>Classes:</p>
<ul>
    <li>S3 Express One Zone: lowest latency for the most frequently accessed data</li>
    <li>S3 Standard: general-purpose for active, frequently accessed data</li>
    <li>S3 Standard-Infrequent Access: low-cost storage for data accessed monthly, that require milliseconfs retrieval</li>
    <li>S3 One Zone-Infrequent Access: infrequently accessed data in a single AZ for cost savings</li>
    <li>S3 Glacier Instant Retrieval: low-cost storage for long-lived data, with retrieval in milliseconds</li>
    <li>S3 Glacier Flexible Retrieval: long-term, low-cost storage for backups and archives,
    with bulk data retrieval from minutes to hours</li>
    <li>S3 Glacier Deep Retrieval: lowest-cost cloud storage for long-term archived data, with retrieval in hours</li>
</ul>
<br>

![image_def]

[image_def]: /images/storage-classes-infographic.png "AWS - Storage Classes Infographic"
<br>

<p><b>Encryption</b></p>
<ul>
    <li>Server Side Encryption (default one)</li>
    <li>Client Side Encryption (before the upload)</li>
</ul>
<br>

<h3>IAM Access Analyzer</h3>
<p>Ensures that only intended people have access to the S3 buckets</p>

<h2>Shared Responsibility Model for S3</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| Versioning | Infrastructure |
| Bucket Policies | Configuration Analysis |
| Replication | Compliance Validation |
| Logging and monitoring | |
| Class selection | |
| Data Encryption | |

<h3>Snow Family</h3>
<p>Portable devices</p>
<ul>
    <li>Snowcone</li>
    <li>Snowedge</li>
    <li>Snowmobile</li>
</ul>
<br>

<p>S3 is <b>propietary</b>, one will need <b>AWS Storage Gateway</b> for a hybrid approach</p>
