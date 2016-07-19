## Server has gone away
If you are receiving the error **"MySQL - server has gone away"** when inserting data, you have to increase the number of **max\_allowed\_packet**'s.

Put the following in `/etc/my.cnf`:

```ini
[mysqld]
; ...
max_allowed_packet=500M
```
