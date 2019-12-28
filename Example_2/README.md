# Simple python docker script.
*Run container*<br/>
`docker run -it --rm --name my-running-script -v "$PWD":/usr/src/app -w /usr/src/app python:3 python script.py`<br/><br/>
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
