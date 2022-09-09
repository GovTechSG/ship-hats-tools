# Roles and permissions

User roles and their permissions determine the actions a user can perform in NexusIQ. NexusIQ as a COTS product comes with system defined roles and permissions. We have customised these system-defined roles and permissions to meet your requirements.

The following table lists the available roles and permissions on NexusIQ with SHIP-HATS:

|Roles |Permissions|
|---|---|
Application Security Tester|A user with this role can review policy violations, test security vulnerabilities, and can change security vulnerabilities. <br><br>This role can be assigned to a GT user or an application vendor user if project team plans to have a vendor user. <br><br>Alternately, team can have another GT user go through the findings, and then update the analysis before the Security Lead reviews the analysis and suppresses the false positives.<br><br>This role corresponds to the *Application Security Tester V2* role in Nexus IQ.|
|Application Evaluator|Evaluates applications<br>Views policy violation summary results|
Component Evaluator|Evaluates individual components<br>Views policy violation results for a specific application|
Developer|Views all information for their assigned organisation or application|
Legal Reviewer|Reviews legal obligations for component licenses|
Owner with Claim Components|A user with this role can manage assigned organizations, applications, policies, and policy violations and can claim components. <br><br>The user with the Project Admin (PA) role in the SHIP-HATS portal is assigned this role by default. If you change the PA for the project, the new PA will be assigned the Owner with Claim Components role.

For more information, refer to the Nexus IQ documentation: https://help.sonatype.com/iqserver/managing/user-management/role-management 