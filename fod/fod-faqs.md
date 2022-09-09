# FAQs

> **Note:** Click the question to view the answer.

 <details>
  <summary><b> How are applications counted within Fortify and Webinspect?</b></summary><br>
Applications are counted based on the number of components.

Example: If your system has 2 components such as Internet and Intranet compartment, these are treated as 2 separate applications. This also applies similarly to systems with several components

Example: Mobile apps for 2 OS (Android, iOS), a website, WebAPI and Batchjob are treated as 5 separate applications.
</details>
<br>
<details>
  <summary><b>My system is built using microservices architecture. How do I determine the total number of applications?</b></summary><br>
We recommend assigning 1 Fortify application per microservice to track and manage findings. However, if you want to reduce the number of Fortify applications and does not need to manage insights for each microservice, you can use the same Fortify app for multiple microservices where the last scan of one microservice can be overridden by the scan of another microservice.
</details>
<br>
<details>
    <summary><b>Can WebInspect be used for Dynamic Application Security Testing (DAST)?</b></summary><br>
Yes, you can use WebInspect for DAST. Note this is applicable for Internet-facing applications only.
</details>
<br>
<details>
    <summary><b> IM8 requires me to perform static code review for security vulnerabilities. Will using Fortify SCA fulfil this clause?</b></summary><br>
Yes, refer to <a href="https://docs.developer.tech.gov.sg/docs/devsecops-playbook/#/devsecops-playbook?id=static-application-security-testing-81s1-g8-g9">DevSecOps playbook</a> for best practices in terms of security testing.
</details>
<br>
<details>
    <summary><b> IM8 requires me to perform Vulnerability Assessment & Penetration Testing (VAPT) for my Internet-facing application. Will using Fortify WebInspect fulfil this clause?</b></summary><br>
It will partially fulfil the clause. WebInspect covers the VA component. The Agency would be required to engage Pentesters to perform penetration testing which is a manual effort.
Refer to <a href="https://docs.developer.tech.gov.sg/docs/devsecops-playbook/#/devsecops-playbook?id=static-application-security-testing-81s1-g8-g9">DevSecOps playbook</a> for best practices in terms of security testing.
</details>