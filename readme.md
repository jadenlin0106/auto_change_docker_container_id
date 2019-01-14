# Auto change container uid & gid when generating container from image

This program performs like this command:

```shell
$  docker run -d --name ${1} -it ${2} /bin/bash
```

  and it will detect your host and  modify the container's uid & gid.

### used:

```shell
$ ./idrun <new container name> <image name:tag>
```

after this command, it will create a new container with your host id.

check:

```shell
$ docker ps
```

You should see the container that you just create.



Check container id in container's bash:

```shell
$ docker exec -it <container naem> /bin/bash
```

then

```shell
$ id
```

It will show the same uid & gid as your host.