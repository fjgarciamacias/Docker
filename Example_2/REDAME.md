# Simple python docker script.
*Run container*<br/>
docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp python:3 python script.py
