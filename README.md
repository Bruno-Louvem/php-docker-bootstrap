# PHP Docker bootstrap

This project was created for beginners on docker learning. this project follow the devops concepts and PHP best practices

1) First usage
---------------------------
### Copy env/local.sh.example to env/local.sh
```bash
$ cp env/local.sh.example env/local.sh
```

### Generate docker files and required enviroment variables for both local and production environments
```bash
$ ./build_files.py
```

### (Optional) Add bash utilities to your .bash_profile
```bash
source <project_path>/devops/docker/utilities.bash
```

2) Running/Building image
---------------------------
```bash
$ cd local/
$ docker-compose up -d
```

3) Docker's bash utilities
---------------------------
```bash
# Stop and remove all docker active containers
$ docker_cleanup

# Enter a running container without needing password or keys
$ docker_enter_container [<container-id> | -L ]
Args:
	<container-id> -> Enter a given running container
	-L -> Enter the last running container


# See logs for all running containers orchestrated by docker-compose
$ docker_logs

```

Dependencies
---------------------------
 * Docker
 * docker-compose
 * Python 2/3
