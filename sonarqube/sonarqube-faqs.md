# FAQs

<details>
  <summary><b>What are the 15 supported languages?</b></summary><br>

Java, JavaScript, C#, TypeScript, Kotlin, Ruby, Go, Scala, Flex, Python, PHP, HTML, CSS, XML, VB.NET.
Do take note that there is no restriction of lines of code and number of applications.

  </details>
<br>
 <details>
  <summary><b>Based on SonarQube’s add-ons, what are the 7 others supported languages?</b></summary><br>

C, C++, Obj-C, Swift, ABAP, T-SQL, PL/SQL are supported. Public officers can refer to the <a href="https://sgdcs.sgnet.gov.sg/sites/IDA-GoSync/gdspdd-ai/ship/_layouts/15/start.aspx#/SitePages/Pricing.aspx">pricing</a> for the add-ons.

  </details>
<br>
 <details>
  <summary><b>Are COTS (commercial off-the-shelf) products supported on SonarQube?</b></summary><br>

Yes. SonarQube can scan for any customisation that the COTS product supports.
Example: Configuration files in XML or Javascript/ Java or plugins written in Java or Python.
  </details>
<br>

<br>
Refer to this section if you have previously been assigned permissions in SonarQube via groups and have lost your access.  

<br>

<details>
<summary><b>My SonarQube Projects are not appearing</b>
</summary>
<br>
<p>During the month of June 2021, we have implemented LDAP group support in SonarQube. Due to this change, the user membership from the <a href="https://www.ship.gov.sg">SHIP-HATS portal</a> will be automatically synced in SonarQube based on your SHIP-HATS subscription. If your subscription contains 20 users, all 20 users should be able to access SonarQube without the SA having to raise a service request to manage users in SonarQube.</p>
<p>We are able to do this because each SHIP-HATS subscription has a master LDAP group containing all the members of the subscription. Depending on whether you already have a group in SonarQube, we will create or rename your existing group name for it to be automatically synchronized in SonarQube. However, any groups created in SonarQube previously might not work as intended since it is not created in SHIP LDAP and will lead to unnsuccessful sync, causing the users in the group to lose access to their projects.</p>

<b>To fix this issue:</b>

- Raise a [service request on JIRA](https://jira.ship.gov.sg) and let us know about this issue.  
We will manually find your master LDAP group and create or rename your existing SonarQube group if any. After this is done, user will be automatically be reassigned to the SonarQube projects that they had access to previously.
</details>
<br>

<details>
<summary><b>How do we manage users in Sonarqube moving forward?</b>
</summary>
<br>
<b>To manage users within your subscription:</b>  
 
<ol><li>The Subscription Admin (SA) and Project Admin (PA) can log in to the <a href="https://www.ship.gov.sg">SHIP-HATS portal</a>.</li>
<li>Add or remove members under the subscription.   
The user membership will be synced to the master LDAP group created for you and will be synced to the SonarQube group.</li></ol>

</details>

