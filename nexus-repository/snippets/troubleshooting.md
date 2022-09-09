
<details>
  <summary><b>How can I resolve a 403 error in the pipeline?</b></summary><br>

Add the following commands before `docker login nexus-docker-publish.ship.gov.sg`

```
rm -f ~/.docker/config.json
```

```
docker logout
```

This is because the login points to the docker hub and needs to be refreshed using the above commands.
</details>
<br>
<details>
  <summary><b>I am unable to update docker in the pipeline?</b></summary><br>

Add the following commands before `docker login nexus-docker-publish.ship.gov.sg`

```
rm -f ~/.docker/config.json
```

```
docker logout
```

This is because the login points to the docker hub and needs to be refreshed using the above commands.
  </details>
