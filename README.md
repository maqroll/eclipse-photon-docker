# eclipse-oxygen-docker
[![](https://images.microbadger.com/badges/image/openkbs/eclipse-oxygen-docker.svg)](https://microbadger.com/images/openkbs/eclipse-oxygen-docker "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/openkbs/eclipse-oxygen-docker.svg)](https://microbadger.com/images/openkbs/eclipse-oxygen-docker "Get your own version badge on microbadger.com")
* Eclipse-Oxygen + Java 8 (1.8.0_162) JDK + Maven 3.5.0 + Python 3.5.2 + X11 (display GUI)

# Run
Image is pulling from openkbs/eclipse-oxygen-docker
```
./run.sh
```

# Build
You can build your own image locally.
```
./build.sh
```

# Configurations (Optional)
If you run "./run.sh" instead of "docker-compose up", you don't have to do anything as below.
* The container uses a default "/workspace" folder. 
* The script "./run.sh" will re-use or create the local folder in your $HOME directory with the path below to map into the docker's internal "/workspace" folder.
```
$HOME/data_docker/eclipse-oxygen-docker/workspace
```

The above configuration will ensure all your projects created in the container's "/workspace" being "persistent" in your local folder, "$HOME/data_docker/eclipse-oxygen-docker/workspace", for your repetitive restart docker container.

# Display X11 Issue
More resource in X11 display of Eclipse on your host machine's OS, please see
* [X11 Display problem](https://askubuntu.com/questions/871092/failed-to-connect-to-mir-failed-to-connect-to-server-socket-no-such-file-or-di)
* [X11 Display with Xhost](http://www.ethicalhackx.com/fix-gtk-warning-cannot-open-display/)
## Other docker-based IDE
* [openkbs/intellij-docker](https://hub.docker.com/r/openkbs/intellij-docker/)
* [openkbs/netbeans](https://hub.docker.com/r/openkbs/netbeans/)
* [openkbs/scala-ide-docker](https://hub.docker.com/r/openkbs/scala-ide-docker/)
