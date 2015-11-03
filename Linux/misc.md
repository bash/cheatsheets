## Start GUI from CLI
To start a graphical application from TTY1 - TTY6 or via SSH you have to export the **DISPLAY** variable.

```bash
export DISPLAY=:0
```

## Environment Variables
System - wide persistent env vars can be put into ``` /etc/environment ```.

Example
```bash
LANG=en_US.UTF-8
LC_ALL=en_US.UTF-8
```

Links:
- https://help.ubuntu.com/community/EnvironmentVariables#A.2Fetc.2Fenvironment
- https://my.fusioned.net/knowledgebase/10093/CentOS-cannot-change-locale-UTF-8.html
