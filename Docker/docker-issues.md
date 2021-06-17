---
layout: default
title: Docker issues
parent: Docker
nav_order: 3
has_children: false
has_toc: true

---

# Some Docker issues I 


## No space left on device
This issue showed up when I ran `docker compose up` after I updated the database from remote latest. One of the containers cried out:
```bash
nginx_1		: ..."var/tmp/nginx/client_body" failed (28: No space left on device)

```

It's not the machine space but it's Docker's. Clean it by [pruning the Docker containers](https://forums.docker.com/t/docker-no-space-left-on-device/69205/3):

With options:

```bash
docker system prune --all
        - all stopped containers
        - all networks not used by at least one container
        - all dangling images
        - all dangling build cache

```
To skip the prompt options:
```bash
docker system prune --all --force
```

This will clean up some space and should be good.