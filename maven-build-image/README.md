# Build container

This docker container is our default build container for java based applications.
It should be used to compile java projects with maven

## usage
Check out your Java project containing the maven build file. Run the container
to start the maven compilation. You mount the root directory of your project
into the container and call maven install:

```docker run -v $PWD:/build maven-build install```

This will mount your current working directory into "/build" of the container
call ```mvn install``` in that directory.

The downloaded artifacts are stored in a folder called "maven-repo" in the /build
directory. If you don't want that, then you can override the maven environment
by passing a different or empty MAVEN_OPTS to the command:

```docker run -v $PWD:/build -e "MAVEN_OPTS=-Dmaven.repo.local=/build/local-maven-repo" maven-build install```
