# Docker Hello World
*Run container* <br/>
`docker run hello-world`

*_output:_*<br/>
Unable to find image 'hello-world:latest' locally<br/>
latest: Pulling from library/hello-world<br/>
1b930d010525: Pull complete <br/>
Digest: sha256:4fe721ccc2e8dc7362278a29dc660d833570ec2682f4e4194f4ee23e415e1064<br/>
Status: Downloaded newer image for hello-world:latest<br/>

Hello from Docker!<br/>
This message shows that your installation appears to be working correctly.<br/>

To generate this message, Docker took the following steps:<br/>
 1. The Docker client contacted the Docker daemon.<br/>
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.<br/>
    (amd64)<br/>
 3. The Docker daemon created a new container from that image which runs the<br/>
    executable that produces the output you are currently reading.<br/>
 4. The Docker daemon streamed that output to the Docker client, which sent it<br/>
    to your terminal.<br/>

To try something more ambitious, you can run an Ubuntu container with:<br/>
 $ docker run -it ubuntu bash<br/>

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

*List all containers*<br/>
`docker ps -a`

*_output:_*<br/>
<pre>
>CONTAINERID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES<br/>
>2bf52987cbec        hello-world         "/hello"            10 minutes ago      Exited (0) 10 minutes ago                       agitated_solomon
</pre>

*Delete hello-world container*<br/>
`docker rm agitated_solomon`

*_output:_*<br/>
agitated_solomon

*Delete hello-world image*<br/>
`docker rmi hello-world`

*_output_:*<br/>
Untagged: hello-world@sha256:4fe721ccc2e8dc7362278a29dc660d833570ec2682f4e4194f4ee23e415e1064<br/>
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e<br/>
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3<br/>
