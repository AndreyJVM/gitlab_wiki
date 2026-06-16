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
# change the default settings in these files
nano /var/lib/docker/volume/gitlab/_data/gitlab.rb
```

```shell
docker swarm deploy -c swarm-gitlab.yml gitlab
```

### Get default pass for root user
```shell
docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
#d23jd23d2j3dj2j&!dddd#dwdawda2@das
```