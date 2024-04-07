<h1>ELB & ASG - Elastic Load Balancing & Auto Scaling Groups</h1>

<h3>Elastic Load Balancing</h3>
<p><b>Vertical Scalability (scale up/down):</b> increase in the size of an instance</p>
<p><b>Horizontal Scalability(scale out/in):</b> increase in the number of instances. Implies distributed systems</p>
<p><b>High availability:</b> it  means running in at least two AZ</p>
<p><b>Scalability:</b> ability to scale up and out</p>
<p><b>Elasticity:</b> it means auto scaling based on load</p>
<p><b>Agility:</b> it means resources are one-click away</p>
<br>

<p><b>Elastic Load Balancer</b></p>
<p>Server that forwards traffic to an EC2 instance downstream</p>
<p>Why use a Load Balancer:</p>
<ul>
    <li>Spread load across multiple downstream instances</li>
    <li>Expose a single point of access (DNS) to you application</li>
    <li>Seamlessly handle failures of the downstreamed instances</li>
    <li>Regular health checks on one's instances</li>
    <li>Provide SSL termination (HTTPS) for one's websites</li>
    <li>Enforce stickiness with cookies</li>
    <li>High availability across multiple zones</li>
    <li>Separate public traffic from private traffic</li>
</ul>
<p>Types:</p>
<ul>
    <li><h3>Application Load Balancer<h3></li>
        <ul>
            <li>Layer 7: HTTP/HTTPS/WebSocket</li>
            <li>Static DNS</li>
            <li>gRPC</li>
            <li>Load balancing to multiple HTTP applications across EC2 instances (target groups)</li>
            <li>Load balancing to multiple HTTP applications on the same EC2 instance (e.g. containers)</li>
            <li>Supports routing tables to different target groups (e.g. routing based on params from an URL)</li>
        </ul>
        <p>Target Groups</p>
        <ul>
            <li>EC2 instances (could be managed by an Auto Scaling Group) - HTTP</li>
            <li>ECS tasks (managed by ECS itself) - HTTP</li>
            <li>Lambda functions - HTTP request is translated into a JSON event</li>
            <li>Private IP addresses</li>
            <br>
            <p>Notes</p>
            <li>ALB can route to multiple target groups</li>
            <li>Health checks are performed at the target group level</li>
        </ul>
    </li>
    <li><h3>Network Load Balancer</h3></li>
    <ul>
        <li>Layer 4: TCP/TLS (secure TCP)/UDP</li>
        <li>Ultra high performance, it can handle millions of requests per second</li>
        <li>One static IP per AZ</li>
    </ul>
    <p>Target Groups</p>
    <ul>
        <li>EC2 instances</li>
        <li>Private IP addresses</li>
        <li>An ALB</li>
        <br>
        <p>Notes</p>
        <li>Health checks support TCP, HTTP and HTTPS protocols</li>
    </ul>
    <li><h3>Gateway Load Balancer</h3></li>
    <ul>
        <li>Layer 3: Network - IP Protocol/GENEVE</li>
        <li>Deploy, scale and manage a fleet of 3rd party network virtual appliances in AWS</li>
        <li>Routes traffic to be inspected first, before getting to one's applications</li>
    </ul>
    <p>Target Groups</p>
    <ul>
        <li>EC2 instances</li>
        <li>Private IP addresses</li>
        <br>
    </ul>
</ul>

<h3>Target Groups</h3>
<p>They route requests to individual targets using the protocol and port specified</p>

<h3>Sticky Sessions</h3>
<p>Clients are redirected to a specific server(EC2 instance) for client-specific purposes (e.g. authentication, cookie info)</p>

<h3>Auto Scaling Group</h3>
<ul>
    <li>Scales out/in, to run at optimal capacity given a current load</li>
    <li>Ensures we have a minimun and maximum number of EC2 instances running</li>
    <li>Automatically registers new instances to a Load Balancer</li>
    <li>Recreates an EC2 instance if a previous one has been terminated</li>
</ul>
<p>Attributes:</p>
<ul>
    <li>Launch Template</li>
    <li>Min Size / Max Size / Initial Capacity</li>
    <li>Scaling Policies</li>
</ul>
<p>Scaling policies:</p>
<ul>
    <li>Dynamic--> e.g. SG CPU to stay at 50%</li>
    <li>Scheduled: based on known usage patterns (e.g. increase min capacity on Flash Sales)</li>
    <li>Predictive: continuously forecast load and schedule scaling actions ahead (e.g. cyclical)</li>
    <li>Target Tracking--> e.g. number of connections to EC2 instances = 100</li>
</ul>
