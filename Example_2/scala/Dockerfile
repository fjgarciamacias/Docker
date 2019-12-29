# Creates image from OpenJDK 8
FROM openjdk:8

# Use this directory as a current directory
WORKDIR /usr/src/app

# Set environment variable SCALA_HOME directory 
ENV SCALA_HOME=/usr/local/share/scala

# Set SCALA_HOME in PATH to use scala command as system command
ENV PATH=$PATH:$SCALA_HOME/bin

# Creates SCALA_HOME directory
RUN mkdir $SCALA_HOME

# Download scala binaries inside SCALA_HOME 
RUN curl https://downloads.lightbend.com/scala/2.13.1/scala-2.13.1.tgz -o $SCALA_HOME/scala-2.13.1.tgz 

# Extracts the binaries inside SCALA_HOME
RUN tar --strip-components=1 -xvzf $SCALA_HOME/scala-2.13.1.tgz -C $SCALA_HOME; rm $SCALA_HOME/scala-2.13.1.tgz

# Use scala command as default docker command
CMD scala
