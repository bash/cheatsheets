# Systemd

## Unit

Units generally look a little bit like this:
```
[Unit]
Description=My awesome service

[Service]
Restart=always
ExecStart=/usr/local/bin/myawesomeservice
```

... and belong in `/etc/systemd/system/` and are named `myawesomeservice.service`.

## Start on boot

**tl;dr** Add this to your unit file:

```bash
[Install]
WantedBy=multi-user.target
```

...and then run `systemctl enable myawesomeservice`

Systemd has this concept of targets, which are basically just groups of services that can be launched together.
A service can then say to which target it could be 'attached' when enabled by providing a list of target inside the `[Install]` section.

There are some special targets like `multi-user.target` which is run somewhen after system boot.

> See: https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/System_Administrators_Guide/sect-Managing_Services_with_systemd-Targets.html

## Journals

Use `journalctl -u myawesomeservice` to look at logs from your service

### Empty logs

If `journalctl` outputs nothing, then you might need to enable persistent logs first:

1. `mkdir -p /var/log/journal/`
2. `systemctl restart systemd-journald`

> See: https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/System_Administrators_Guide/s1-Using_the_Journal.html

Also, systemd sometimes doesn't like unit files that are symlinks, try without a symlink and see if the logs work.