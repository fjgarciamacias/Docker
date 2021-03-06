# Simple python docker script.
*Run container*<br/>
`docker run -it --rm --name my-running-script -v "$PWD":/usr/src/app -w /usr/src/app python:3 python script.py`<br/>
**output:**
<pre>
Simple python script
</pre>
*Python interactive with docker*<br/>
`docker run -it --rm python:3`<br/>
**output:**
<pre>
Python 3.8.1 (default, Dec 20 2019, 21:56:21) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> _
</pre>
**OPTIONS:**
<pre>
-i, --interactive      Keep STDIN opn even if not attached (It gets the `docker run`'s STDIN and executes it into the container)
-t, --tty              Allocate a pseudo-TTY (This option is optional, it only creates a TTY)
--rm                   Automatically remove the container when it exits
--name string          Assign a name to the container
-v, --volume list      Bind mount a volume
-w, --wordir string    Working directory inside the container
</pre>

**ARGUMENTS:**
<pre>
--name my-running-script    The name of the container
-v "$PWD":/usr/src/app      Bind current directory to /usr/src/app
-w /usr/src/app             Working directory /usr/src/app
python:3                    Image python:3
python script.py            Run command python with argument script.py
</pre>

<br/>
You can also create the following script:
<pre>
#!/bin/sh
# cpython script (container python)

docker run -it --rm --name my-running-script -v "$PWD":/usr/src/app -w /usr/src/app python:3 python $1
</pre>

And change the permisions as following:
`chmod u+x cpython`<br/>
Finally execute ./cpython script.py
