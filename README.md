### Running GitLab CE with docker

### 1. Install docker

```shell
service docker status 
# active (running)
```

### 2.1 Docker compose
```shell
# Copy the text and change the default settings in these files
touch .env compose.yml
```

```shell
docker compose up -d
```

### 2.2 Docker swarm
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

### 3. Get default pass for root user
```shell
docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
#d23jd23d2j3dj2j&!dddd#dwdawda2@das
```