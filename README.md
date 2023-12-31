# journaltail
Tail -f files and systemd-journald at the same time

# usage

To view messages logged by apache2 and nginx to systemd-journald as well as lines being added to 2 log files, run the following:

```
journaltail -u apache2.service -u nginx /var/log/messages /var/log/mail.log
```

Prefix systemd units with `-u` (`.service` suffix is optional)

# install

`apt install python3-systemd` or `yum install systemd-python` or something similar for your distribution. Then copy journaltail to `/usr/local/bin`, `~/bin` or another directory of your preference.

## oneliner for RHEL

`[[ $(rpm -E %rhel) -le 7 ]] && yum install -y systemd-python || yum install -y systemd-python3 && wget -O /usr/local/bin/journaltail https://github.com/gjedeer/journaltail/raw/main/journaltail && chmod +x /usr/local/bin/journaltail`
