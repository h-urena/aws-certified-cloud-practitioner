<h1>Databases & Analytics</h1>

<p><b>Main DB Types</b></p>
<ul>
    <li>Relational DBs</li>
    <li>NoSQL DBs</li>
</ul>

<h3>RDS: Relational Database Service</h3>
<p>Storage backed up by EBS</p>
<p>Note: Can't SSH into an RDS instance</p>

<h3>Aurora (propietary)</h3>
<ul>
    <li>Supports PostgreSQL and MySQL</li>
    <li>Serverless function</li>
    <li>More cloud-based</li>
</ul>

<h3>Elastic Cache</h3>
<p>In-memory DB</p>

<h3>Dynamo DB</h3>
<ul>
    <li>NoSQL DB, with replication across 3 availability zones</li>
    <li>Low latency, serverless</li>
    <li>Global tables: multiple regions (read/write)</li>
</ul>
<p><b>DAX:</b> in-memory cache for DynamoDB</p>

<h3>RedShift</h3>
<p>Data warehousing and analytics columnar</p>
<p>Serverless: pay as-you-go computing without worrying about scalability</p>

<h3>EMR</h3>
<p>Run and scale big data workloads easily</p>

<h3>Athena</h3>
<p>Serverless SQL query service to perform analytics against S3 objects</p>

<h3>Quicksight</h3>
<p>Interactive dashboards for DB services</p>

<h3>DocumentDB</h3>
<p>Document DB, AWS' MongoDB flavor</p>

<h3>Neptune</h3>
<p>Graph DB</p>

<h3>Timestream</h3>
<p>Time series DB for IoT</p>

<h3>Quantum Ledger Database</h3>
<p>Fully managed immutable transaction log, mostly used for financial services</p>

<h3>Blockchain</h3>
<p>Web3 service</p>

<h3>Glue</h3>
<p>ETL, data catalog service</p>

<h2>Shared Responsibility Model for DBs</h2>

<p>AWS will provide different options</p>
<ul>
    <li>High availability</li>
    <li>Backup</li>
    <li>Scaling</li>
</ul>

<p>OS patching is handled by AWS in this case</p>
