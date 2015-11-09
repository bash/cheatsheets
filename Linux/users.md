## Change to disabled user
If you need to execute a command as a user like apache or nginx, you have to
give them a proper shell.

```bash
chsh -s /bin/bash nginx
```

Switch back
```bash
chsh -s /sbin/nologin nginx
```
