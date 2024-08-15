# Docker Most Commands to Use

To run the compose.yaml file that I created, that contains the docker instructions, like postgres instructions. You can specify ports username, servername and etc

```bash
docker compose up
```

And to turn off the docker after Ctrl+C, because even if I Cancel the process still docker will be running of that process,

```bash
docker compose down
```

And sometimes the above command do not work then I need to manually stop the process either in controll process or your system or the docker process controller(ps). For example in postgres

```bash
docker ps
```

After that command I will see the ids of the running docker processes then I can manually stop them by typing this command,

```bash
docker stop <The ID of the Docker Container>
```

Also I can terminate in my Linux machine using the process manager like ps aux and kill

```bash
ps aux | grep "<The name of the docker process>"
```

The I can kill the process forcefully or gently

```bash
kill -9 <Process ID from the Linux>
```

Or

```bash
kill -15 <Process ID from the Linux>
```
