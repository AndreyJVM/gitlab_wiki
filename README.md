### Running GitLab CE with docker

### Install docker

```shell
service docker status 
# active (running)
```

### Docker compose
```shell
# Copy the text and change the default settings in these files
touch .env compose.yml
```

```shell
docker compose up -d
```

### Docker swarm
```shell
# Copy the text and change the default settings in these file
touch swarm-gitlab.yml
```

```shell
docker swarm deploy -c swarm-gitlab.yml gitlab
```