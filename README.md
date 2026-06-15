### Running GitLab CE with docker

### Install docker

```shell
service docker status 
# active (running)
```

### Docker compose

```shell
mkdir docker_gitlab_service; cd docker_gitlab_service
```

```shell
nano .env
```

```shell
nano docker-compose.yml
```

```yaml
docker compose up -d
```

### Docker swarm
