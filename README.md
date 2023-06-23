# journaltail
Tail -f files and systemd-journald at the same time

# usage

```
journaltail -u apache2.service -u nginx /var/log/messages
```

Prefix systemd units with `-u` (.service suffix optional)

# install

`apt install python3-systemd ` or `yum install systemd-python` or something similar for your distribution.
