# scala-play

Package the host app and create a docker image

`sbt docker:publishLocal`

Start mongo instance

`docker run --name mongo -p 27017:27017 -d mongo`

then link host app to mongo and run

`docker run --name play-8080 -p 8080:9000 --link mongo:mongo -d play-scala:1.0-SNAPSHOT`