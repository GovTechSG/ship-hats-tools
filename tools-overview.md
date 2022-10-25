# Tools Overview

The following table provides list of tools for each stage in CI/CD pipeline offered under **SHIP-HATS**. 

|Stage|GitLab Native|Alternative Tool|
|---|---|---|
|Access|TechPass & SEED|TechPass & SEED|
|Plan|GitLab Issues|Jira 	
|Plan|GitLab Wiki| Confluence 	
|Plan|Gitlab Security Dashboard|NA|	
|Build|GitLab CI/CD|NA|
|Build|GitLab Package Registry|Nexus Repository Pro|
|Build|GitLab Dependency Scanning|Nexus Intelligence/Nexus IQ Server|
|Build Testing|GitLab SAST|Fortify-on-Demand SAST(new!)
|Other Tests|GitLab Code Quality Scanning Tool |SonarQube Community/Developer Edition
|Other Tests|GitLab DAST|Fortify-on-demand DAST (new!)
|Other Tests|GitLab Container Scanning|NA
|Other Tests|NA|pCloudy Test Farm
|Other Tests|GitLab (Pa11y)|Purple HATS
|Deploy & Release|GitLab CI/CD|NA|

## Supported Tools and Versions

*Updated on: 29 October, 2022*

SHIP-HATS provides following tools while adhering to security and compliance requirements.  

The following table provides a list of tools integrated with SHIP-HATS and the supported version:

|Tools |  Supported Version | Endpoint (URL) |
| --- | --- | --- |
|[GitLab](gitlab/gitlab-overview)|NA|https://sgts.gitlab-dedicated.com/
|[Confluence](confluence/confluence-overview)|[7.19.2](https://confluence.atlassian.com/doc/confluence-7-19-release-notes-1141976784.html)|https://confluence.ship.gov.sg/|
|[Fortify on Demand](fod-overview)|NA|https://sgp.fortify.com/
|[Jira](jira/jira-overview.md) |[9.2.0](https://confluence.atlassian.com/jirasoftware/jira-software-9-2-x-release-notes-1163763245.html) |https://jira.ship.gov.sg/|
|[Nexus IQ](nexus-iq/nexus-iq-overview) |[145](https://help.sonatype.com/iqserver/product-information/release-notes)  | https://nexus-iq.ship.gov.sg/assets/index.html |
|[Nexus Repository Pro](nexus-repository/nexus-repository-overview) |  [3.42.0](https://help.sonatype.com/repomanager3/product-information/release-notes/2022-release-notes/nexus-repository-3.42.0-release-notes)<br><br>Refer to [Critical Cleanup Policy](https://help.sonatype.com/repomanager3/product-information/critical-cleanup-policy-bug-advisory) for more details. | https://nexus.ship.gov.sg/|
|[pCloudy](pcloudy/pcloudy-overview) | NA | https://hats.pcloudy.com/ <br><br> As the pCloudy web dashboard needs proxy settings configured in your browser, we recommend you use Firefox to use pCloudy so that these proxy settings do not impact your system&#39;s proxy.|
|[Purple HATS](purple-hats/purple-hats-overview) | 1.17.0  | NA as it is a CLI tool. |
|[SonarQube](sonarqube/sonarqube-overview) |Community edition 9.3  | https://sonar.hats.stack.gov.sg/sonar|
|[SonarQube](sonarqube/sonarqube-overview) |Developer edition 9.3 | https://sonar1.hats.stack.gov.sg/sonar|
