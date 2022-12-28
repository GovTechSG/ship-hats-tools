>**Tip:** Click the question or triangle to view the answer.

<details>
  <summary><b>What docker alternatives are available to replace docker commands?</b></summary><br>

In [SHIP-HATS Templates](pipeline-templates) (from tag v1.0.4), the docker alternative tools used in our templates include Kaniko, Skopeo, and Crane. 
</details>
<br>

<details>
  <summary><b>Why can't SHIP-HATS Templates use one tool (e.g. Buildah or Podman) to replace all docker commands? </b></summary><br>
<!--Why multiple docker alternative tools are available in SHIP-HATS Templates?-->

In our testing, Buildah and Podman require minimally some elevated capabilities on runner to work. These elevated capabilities are undesirable in a shared runner model as they allow host escape. So, SHIP-HATS Templates leverage several tools that do not require such runner settings to fulfil some docker commands. For example: 

<!--Based on the docker alternatives that we have identified and used in SHIP-HATS Templates, there isn't one tool that can replace docker commands completely. Therefore, we have included multiple docker alternatives that can perform certain operations that docker commands offer. -->

- Kaniko is able to build an image from a `Dockerfile` and push it to a registry. For example, it is ideal to replace `docker build` and `docker push` commands.
- Skopeo is known for copying an image from and to various storage mechanisms. For example, it is ideal to replace `docker tag`.
- Crane is a tool for interacting with remote images and registries. For example, it is ideal to replace `docker pull` and `docker push` (that cannot be performed by Kaniko and Skopeo).
</details>
<br>

<details>
  <summary><b>Are the docker alternatives identified able to fully replace the docker commands?</b></summary><br>

No, there are certain functions that cannot be performed by the suggested docker alternatives, such as `docker run` and `docker compose`. You may consider using [GitLab services](https://docs.gitlab.com/ee/ci/services/) with your services designed to provide additional features which are network accessible.
</details>
<br>

<details>
  <summary><b>Docker alternative tools are insufficient for me and I would still need to run docker commands directly. What can I do?</b></summary><br>

SHIP-HATS does not supply Docker-in-Docker (`dind`) or privileged shared runners. You need to self host privileged runner to use `dind` image for running docker commands directly. Refer to [Set up GitLab Runners documentation](gitlab-runners) to set up self-hosted GitLab Runner.
</details>
<br>

<details>
  <summary><b>Can the docker alternatives run on non-root and non-privileged runners (CStack runners)?</b></summary><br>

Based on our testing on docker alternatives, Skopeo and Crane can run on non-root and non-privileged runners (tags: cstacks, non_privileged, no_root) whereas Kaniko can run on runners with root and non-privileged runners (tags: ship_docker, non_privileged).
</details>
<br>

<details>
  <summary><b>Are there any image or job templates that I can reference in my job if there are tasks that require multiple tools. For example, AWS assumes role with Kaniko to build and push image to AWS ECR.</b></summary><br>

[Pipeline COE](https://sgts.gitlab-dedicated.com/pipelinecoe/containers) is an InnerSource project where custom images are built and shared across all projects. Most images in Pipeline COE are built from container base image that comes with multiple common tools (e.g., Wget, Git, curl, and JQ).

Please note that this project is a work in progress and the location of the images might be changed later. You may refer to the images there in your job should you find any one suitable.<!--You may refer to the images in your job to find something suitable to your requirements.--> 

If you are unable to find a suitable image in Pipeline COE, you may [raise a request](https://jira.ship.gov.sg/servicedesk/customer/portal/11) or if you find an image that can add on the tools that you require, you may edit the Dockerfile and raise an MR for platform team to review and approve. 
</details>
<br>