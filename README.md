# How to install docker-compose on fedora 31
If you install docker service with https://get.docker.com script, when you want install docker-compose
with below command, you get python library error.
``` \# dnf --enablerepo=docker-ce-stable install docker-compose ```

also if you want install docker-compose with this command #pip3 install --upgrade docker-compose
you get below error.
```
\# docker-compose
Traceback (most recent call last):
  File "/usr/local/bin/docker-compose", line 5, in <module>
    from compose.cli.main import main
  File "/usr/local/lib/python3.7/site-packages/compose/cli/main.py", line 35, in <module>
    from ..project import get_image_digests
  File "/usr/local/lib/python3.7/site-packages/compose/project.py", line 14, in <module>
    from docker.errors import ImageNotFound
ImportError: cannot import name 'ImageNotFound' from 'docker.errors' (/root/.local/lib/python3.7/site-packages/docker/errors.py)
```

> Solution
```
Install with below command
\# pip3 install docker-compose --force-reinstall --user
```
