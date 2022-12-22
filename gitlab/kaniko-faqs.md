>**Tip:** Click the question or triangle to view the answer.

<details>
  <summary><b>What docker alternatives are available to replace docker commands?</b></summary><br>

In [SHIP-HATS Templates](pipeline-templates), the docker alternative tools used in our templates include Kaniko, Skopeo, and Crane. 
</details>
<br>

<details>
  <summary><b>Why multiple docker alternative tools are provided in SHIP-HATS Templates?</b></summary><br>

Based on the docker alternatives that we have identified and used in SHIP-HATS Templates, there isn't one tool that can replace docker commands completely. Therefore, we have included multiple docker alternatives that can perform certain operations that docker commands offer. 

- Kaniko is able to build an image from a `Dockerfile` and push it to a registry. For example, it is ideal to replace `docker build` and `docker push` commands.
- Skopeo is known for copying an image from and to various storage mechanisms. For example, it is ideal to replace `docker tag`.
- Crane is a tool for interacting with remote images and registries. For example, it is ideal to replace `docker pull` and `docker push` (that cannot be performed by Kaniko and Skopeo).
</details>
<br>

<details>
  <summary><b>Are the docker alternatives identified able to fully replace the docker commands?</b></summary><br>

No, there are certain functions that cannot be performed by the suggested docker alternatives, such as `docker run` and `docker compose`. You may consider using [Gitlab services](https://docs.gitlab.com/ee/ci/services/) with your services designed to provide additional features which are network accessible.
</details>
<br>

<details>
  <summary><b>I will still need to use docker commands for my jobs and pipeline. What can I do in this case?</b></summary><br>

Enabling docker-in-docker requires privileged runner, which is not offered in our shared runners. You can consider hosting your own docker machine that is capable of running docker commands. For more information, refer to [Set up GitLab Runners](gitlab-runners).
</details>
<br>

<details>
  <summary><b>Can the docker alternatives run on non-root and non-privileged runners (CStack runners)?</b></summary><br>

Based on our testing on docker alternatives, Skopeo and Crane can run on non-root and non-privileged runners (tags: cstacks, non_privileged, no_root) whereas Kaniko can run on runners with root and non-privileged runners (tags: ship_docker, non_privileged).
</details>
<br>

<details>
  <summary><b>Are there any image or job templates that I can reference in my job if there are tasks that require multiple tools. For example, AWS assumes role with Kaniko to build and push image to AWS ECR).</b></summary><br>

You may refer to the images in Pipeline COE to see if there is any image that is suitable for your use case. Most images in Pipeline COE are built from container base image that comes with multiple common tools (like wget, git, curl and jq). If you are unable to find a suitable image in Pipeline COE, you may [raise a request](https://jira.ship.gov.sg/servicedesk/customer/portal/11) or if you find an image that can add on the tools that you require, you may edit the Dockerfile and raise an MR for platform team to review and approve. 
</details>
<br>