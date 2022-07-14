Step 5: Run test 
=============

After adding the properties and run the test and Check the logs.

    13:30:59.352  INFO   --- [    Test worker] o.t.d.DockerClientProviderStrategy       : Found Docker environment with local Npipe socket (npipe:////./pipe/docker_engine)
    13:30:59.369  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : Docker host IP address is localhost
    13:30:59.431  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : Connected to docker: 
      Server Version: 20.10.11
      API Version: 1.41
      Operating System: Docker Desktop
      Total Memory: 3929 MB
    13:31:03.294  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : Ryuk started - will monitor and terminate Testcontainers containers on JVM exit
    13:31:03.295  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : Checking the system...
    13:31:03.296  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : ✔ Docker server version should be at least 1.6.0
    13:31:03.588  INFO   --- [    Test worker] org.testcontainers.DockerClientFactory   : ✔ Docker environment should have more than 2GB free disk space

As you can see, Testcontainers quickly discovered your environment and connected to Docker. It did some pre-flight checks as well to ensure that you have a valid environment.

### Disable check
Add the following line to your `~/.applicaiton-testcontainers.properties` file to disable these checks and speed up the tests:

```checks.disable=true```


