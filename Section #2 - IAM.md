<h1>IAM - Identity and Access Management</h1>
<p><strong>Global service</strong> - Groups can only contain users - M:M relationship</br>
<strong>Always apply the <em>principle of least privilege</em></strong></p>

<h3>IAM Policy Structure</h3>
Version<br>
Id<br>
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
    <li>AWS CloudShell (not available in all regions yet)</li>
    <li>AWS Command Line Interface (CLI)</li>
    <li>AWS Software Development Kit (SDK)</li>
</ol>
<p>*Last 2 require access keys</p>

<h3>IAM Roles</h3>
<p>To perform actions on behalf of a service</p>

<h3>IAM Policies</h3>
<p>JSON documents that define a set of permissions for making requests to AWS services</p>
<p>They can be used by IAM users, IAM roles, and user groups</p>


<h3>IAM Security Tools</h3>
<ul>
    <li>IAM Credentials Report (account-level): lists all of one's account users and their credential statuses</li>
    <li>IAM Access Advisor (user-level): user's service permissions granted on a granular level</li>
</ul>

<h3>Organizations</h3>
<ul>
    <li>Global services that allow the management of multiple AWS accounts</li>
    <li>The main account is the management one</li>
    <li>Consolidated billing and pricing benefits (if apply) across all accounts</li>
</ul>

<h3>IAM Conditions</h3>
<p>Specific set of conditions that can be applied to policies. Types:</p>
<ul>
    <li>aws:SourceIp: restrict clients' ip addresses where an API call is being made from</li>
    <li>aws:RequestedRegion: prevent a region from receiving API calls</li>
    <li>E.g. ec2:ResourceTag/aws:PrincipalTag: allow/deny access based on tags</li>
    <li>aws:MultiFactorAuthPresent: enforce MFA prior to performing actions on resources</li>
    <li>aws:PrincipalOrgID: allow/deny access based on organization accounts</li>
</ul>

<h3>Permission Boundaries</h3>
<ul>
    <li>Boundaries that can be set to a user or a role (not a group)</li>
    <li>The take precedence over session permissions policies</li>
</ul>

<h3>IAM Identity Center</h3>
<ul>
    <li>SSO for multiple accounts, based on permission sets</li>
</ul>

<h3>Control Tower</h3>
<ul>
    <li>Easy way to set up and govern a secure and compliant multi-account AWS environment. It uses
    Organizations to create the accounts</li>
</ul>

<h2>Best Practices</h2>
<ul>
    <li>Don't use root account, except for account setup</li>
    <li>One user = one AWS user</li>
    <li>Assign user to groups, add permissions(policies) to groups/roles</li>
    <li>Strong password policy</li>
    <li>Enforce MFA on Root account and IAM users</li>
    <li>Create <i>roles</i> for giving permissions to services</li>
    <li>Access keys for programmatic access (CLI/SDK)</li>
    <li>Audit permissions using <i>Credential Reports</i> and <i>Access Advisor</i></li>
    <li>Never share neither <i>IAM Users</i> nor <i>Access Keys</i></li>
    <li>Avoid inline policies for specific users</li>
</ul>
<br>

<h2>Shared Responsibility Model for IAM</h2>

| CUSTOMER  | AWS  |
| --------  | ---  |
| User, groups, roles, policy management | Infrastructure, configuration and vulnerability analysis |
| MFA | Compliance validation |
| IAM use of tools | |
| Analyze access patterns and permissions review | |
