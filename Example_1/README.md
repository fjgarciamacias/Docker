# Docker Hello World
*Run container*
`docker run hello-world`

*_output:_*
<pre>
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
1b930d010525: Pull complete 
Digest: sha256:4fe721ccc2e8dc7362278a29dc660d833570ec2682f4e4194f4ee23e415e1064
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
 </pre>

*List all containers*
`docker ps -a`

*_output:_*
<pre>
CONTAINERID         IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
2bf52987cbec        hello-world         "/hello"            10 minutes ago      Exited (0) 10 minutes ago                       agitated_solomon
</pre>

*Delete hello-world container*
`docker rm agitated_solomon`

*_output:_*
<pre>
agitated_solomon
</pre>

*Delete hello-world image*
`docker rmi hello-world`

*_output_:*
<pre>
Untagged: hello-world@sha256:4fe721ccc2e8dc7362278a29dc660d833570ec2682f4e4194f4ee23e415e1064
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3
</pre>
