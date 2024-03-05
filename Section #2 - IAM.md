<h1>IAM - Identity and Access Management</h1>
<p><strong>Global service</strong> - Groups can only contain users - M:M relationship</br>
<strong>Always apply the <em>principle of least privilege</em></strong></p>
</br>

<h3>IAM Policy Structure</h3>
Version</br>
Id</br>
Statement :

```json
[{
    Sid: optional identifier
    Effect: allow/deny access
    Principal: account/user/role which the policy applies to
    Action: list of actions the policy allows/denies
    Resource: list of resources which the action applies to
    Condition: optional parameter for when this policy takes effect
}]

```

</br>

<h3>Password Policy:</h3>
<ul>
    <li>Strong passwords</li>
    <li>MFA : protect Root account + IAM users
        <ul>
            <li>Virtual MFA device</li>
            <li>Universal 2nd factor (U2F) security key</li>
            <li>Hardware key fob device</li>
            <li>Hardware key fob for AWS GovCloud (US)</li>
        </ul>
    </li>
</ul>

<h3>Access to AWS</h3>
<ol>
    <li>AWS Management Console: password + MFA</li>
    <li>AWS Command Line Interface (CLI)</li>
    <li>AWS Software Development Kit (SDK)</li>
</ol>
*Last 2 require access keys
</br>

<h3>IAM Roles</h3>
To perform actions on behalf of a user
</br>

<h3>IAM Security Tools</h3>
<ul>
    <li>IAM Credentials Report (account)</li>
    <li>IAM Access Advisor (user-level): granular user permissions on AWS</li>
</ul>
</br>

<h2>Best Practices</h2>
<ul>
    <li>Don't use root account, except for account setup</li>
    <li>One user = one AWS user</li>
    <li>Assign user to groups, add permissions to groups</li>
    <li>Strong password policy</li>
    <li>Enforce MFA</li>
    <li>Create <i>roles</i> for giving permissions to services</li>
    <li>Access keys for programmatic access (CLI/SDK)</li>
    <li>Audit permissions using <i>Credential Reports</i> and <i>Access Advisor</i></li>
    <li>Never share neither <i>IAM Users</i> nor <i>Access Keys</i></li>
</ul>
</br>

<h2>Shared Responsibility Model for IAM</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| User, groups, roles, policy management | Infrastructure, configuration and vulnerability analysis |
| MFA | Compliance validation |
| IAM use of tools | |
| Analyze access patterns and permissions review | |
