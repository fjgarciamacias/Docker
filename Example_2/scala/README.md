# Simple scala docker script.
*Build scala image*<br/>
`docker build -t scala:2.13.1 .`<br/>
**output:**
<pre>
Sending build context to Docker daemon  4.608kB
Step 1/8 : FROM openjdk:8
 ---> f8146facf376
Step 2/8 : WORKDIR /usr/src/app
 ---> Using cache
 ---> 71f8a9f9ea92
Step 3/8 : ENV SCALA_HOME=/usr/local/share/scala
 ---> Using cache
 ---> d5cbb1184536
Step 4/8 : ENV PATH=$PATH:$SCALA_HOME/bin
 ---> Using cache
 ---> 324595d34ecd
Step 5/8 : RUN mkdir $SCALA_HOME
 ---> Using cache
 ---> 0b8c942da4d2
Step 6/8 : RUN curl https://downloads.lightbend.com/scala/2.13.1/scala-2.13.1.tgz -o $SCALA_HOME/scala-2.13.1.tgz
 ---> Using cache
 ---> 2d59527601f8
Step 7/8 : RUN tar --strip-components=1 -xvzf $SCALA_HOME/scala-2.13.1.tgz -C $SCALA_HOME; rm $SCALA_HOME/scala-2.13.1.tgz
 ---> Using cache
 ---> 4e91c24d4bbe
Step 8/8 : CMD scala
 ---> Using cache
 ---> 7a24b9ffc124
Successfully built 7a24b9ffc124
Successfully tagged scala:2.13.1
</pre>

*Run container*<br/>
`docker run -it --rm --name my-running-script -v "$PWD":/usr/src/app -w /usr/src/app scala:2.13.1 scala script.scala`<br/>
**output:**
<pre>
Simple scala script
</pre>
*Scala interactive with docker*<br/>
`docker run -it --rm scala:2.13.1`<br/>
**output:**
<pre>
Welcome to Scala 2.13.1 (OpenJDK 64-Bit Server VM, Java 1.8.0_232).
Type in expressions for evaluation. Or try :help.

scala> _
</pre>
**OPTIONS:**
<pre>
-i, --interactive      Keep STDIN opn even if not attached
-t, --tty              Allocate a pseudo-TTY
--rm                   Automatically remove the container when it exits
--name string          Assign a name to the container
-v, --volume list      Bind mount a volume
-w, --wordir string    Working directory inside the container
</pre>

**ARGUMENTS:**
<pre>
--name my-running-script    The name of the container
-v "$PWD":/usr/src/app    Bind current directory to /usr/src/app
-w /usr/src/app           Working directory /usr/src/app
scala:2.13.1                    Image scala:2.13.1
scala script.scala            Run command python with argument script.py
</pre>

<br/>
You can also create the following script:
<pre>
#!/bin/sh
# cpython script (container python)

docker run -it --rm --name my-running-script -v "$PWD":/usr/src/app -w /usr/src/app python:3 python $1
</pre>

And change the permisions as following:
`chmod u+x cscala`<br/>
Finally execute ./cscala script.scala
