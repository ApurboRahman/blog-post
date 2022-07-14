Step 3: Docker Setup
=============

### Check Docker
Make sure you have Docker available on your machine by running the following command:

```$ docker version```

### Docker Installation 
We need Docker to run containers. Refer to Docker documentation for installation instructions.
https://docs.docker.com/install/

### Docker configuration
For additional configuration Refer the following link
https://docs.docker.com/engine/swarm/configs/


###Start Container
To start it up, we simply have to execute the start method:

```container.start();```

###Stop Container

To stop the container

```container.stop();```

###Disbale Proxy
If you use proxy, you can disable those checks by creating the file  in the tests resources directory  ```application-testcontainers.properties``` with this content:

```check.disable=true```

