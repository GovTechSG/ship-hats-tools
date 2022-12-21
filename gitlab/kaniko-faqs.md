>**Tip:** Click the question or triangle to view the answer.

<details>
  <summary><b>What are the docker alternatives available to replace docker commands?</b></summary><br>

In SHIP-HATS Templates (tags: v1.0.4), the docker alternative tools used in our templates include kaniko, skopeo and crane. Please refer to the SHIP-HATS Templates project on the templates and their usage. 
</details>
<br>

<details>
  <summary><b>Why are there multiple docker alternative tools in SHIP-HATS Templates?</b></summary><br>

Based on the docker alternatives that we have identified and used in SHIP-HATS Templates, there isn't one tool that can replace docker commands completely. Hence, we included multiple docker alternatives that can perform certain operations that docker commands have offered. 

- Kaniko is able to build an image from a Dockerfile and push it to a registry - example: ideal to replace docker build and push
- Skopeo is known for copying an image from and to various storage mechanisms - example: ideal to replace docker tag
- Crane is a tool for interacting with remote images and registries - example: ideal to replace docker pull/ push that were unable to be performed by kaniko and skopeo
</details>
<br>

<details>
  <summary><b>Are the docker alternatives identified able to fully replace the docker commands?</b></summary><br>

No, there are certain functions that can't be performed by the docker alternatives, such as `docker run` and `docker compose`. 
</details>
<br>

<details>
  <summary><b>I will still need to use docker commands for my jobs/ pipeline. What can I do in this case?</b></summary><br>

As enabling docker-in-docker requires privileged runner which is not offered in our shared runners, you can consider hosting your own docker machine that is capable of running docker commands. For more information, refer to [Set up GitLab Runners](gitlab-runners.md).
</details>
<br>

<details>
  <summary><b>Can the docker alternatives run on non-root and non-privileged runners (Cstack runners)?</b></summary><br>

Based on our testings on docker alternatives, skopeo and crane can run on non-root and non-privileged runners (tags: cstacks, non_privileged, no_root) whereas kaniko can run on runners with root and non-privileged (tags: ship_docker, non_privileged).
</details>
<br>

<details>
  <summary><b>Are there any image/ job templates that I can reference in my job if there are tasks that require multiple tools (Example: aws assume role with kaniko to build and push image to aws ecr)</b></summary><br>

answer
</details>
<br>

<details>
  <summary><b></b></summary><br>

</details>
<br>
