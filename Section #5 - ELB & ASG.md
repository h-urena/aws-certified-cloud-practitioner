<h1>ELB & ASG - Elastic Load Balancing & Auto Scaling Groups</h1>

<h3>Elastic Load Balancing</h3>
<p><b>Vertical Scalability:</b> increase in the size of an instance</p>
<p><b>Horizontal Scalability:</b> increase in the number of instances. Implies distributed systems</p>
<p><b>High availability:</b> it  means running in at least two AZ</p>
<p><b>Scalability:</b> ability to scale up and out</p>
<p><b>Elasticity:</b> it means auto scaling based on load</p>
<p><b>Agility:</b> it means resources are one-click away</p>
<br>

<p><b>Elastic Load Balancer</b></p>
<p>Server that forwards traffic to an EC2 instance downstream</p>
<p>Types:</p>
<ul>
    <li>Application Load Balancer</li>
        <ul>
            <li>Layer 7: HTTP/HTTPS</li>
            <li>Static DNS</li>
            <li>gRPC</li>
        </ul>
    <li>Network Load Balancer</li>
    <ul>
        <li>Layer 4: TCP</li>
        <li>Ultra high performance</li>
        <li>Static IP</li>
    </ul>
    <li>Gateway Load Balancer</li>
    <ul>
        <li>Layer 3: GENEVE</li>
        <li>Routes traffic to firewalls</li>
    </ul>
</ul>
<br>

<h3>Auto Scaling Group</h3>
<p>Scales in and/or out, to run at optimal capacity given a current load</p>
<p>Strategies:</p>
<ul>
    <li>Manual</li>
    <li>Dynamic</li>
    <li>Predictive</li>
</ul>
