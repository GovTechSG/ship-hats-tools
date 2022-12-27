In SHIP-HATS 2.0 platform, there are 3 types of runners:  

- **SHIP-HATS hosted Shared Runner:** The shared runners are hosted by the SHIP-HATS team. There are 3 variants in the shared runner pool. These runners are easily accessible to users and are scalable on demand.

    |Runner Variant|Executor|Privileged|Cache Enabled|Run Untag|Notes|
    |---|---|---|---|---|---|
    |CStack Runner|kubernetes|FALSE|YES|YES|Run as non-root
    |Docker Runner|docker + machine|FALSE|YES|NO|We have removed privileged access for SHIP-HATS shared runner. This affects build of systems that used the shared runners with docker-in-docker. Alternatively, you can use [Kaniko](#docker-alternative-faqs).
    |[Windows Runner](#windows-runner)|shell|N/A|YES|NO|- OS: MS Windows Server 2019 Base<br>- Git: 2.36.1<br>- Visual Studio 2022 version 17.0<br>- .Net framework 4.8 development tools<br>- Refer to [GitLab Windows Runners](#windows-runner) for important details on **cleanup job** included with Windows Runner.

- **Agency-hosted Remote Runner:** The agency-hosted remote runners are the dedicated machines that are set-up and managed by agencies. These runners can connect to SHIP-HATS via the *IPSec tunnel* or *VPC endpoint* if they are hosted on GCC AWS or CC AWS. 
- **GitLab Shared Runner on SaaS:** The GitLab shared runner on SaaS will be available over the next couple months. 

For more information, refer to the [GitLab Runner](https://docs.gitlab.com/runner/) documentation.