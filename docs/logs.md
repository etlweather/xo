# Logs

This section will explain how to check the XOA logs, and be able to detect issues.

## From the web interface

Go into Settings/Logs view.

## CLI

All XOA logs are stored in `/var/log/syslog`.

To filter only on what you need, you can use `journalctl`. Let's see some example to filter only logs for `xo-server`:

```
$ journalctl -u xo-server -f -n 50
```

This will return the 50 last lines and tail the file. If you have an error message in your application, start this command and try to reproduce the issue. You'll see clearly what the problem is.

You can also filter for the updater program:

```
$ journalctl -u xoa-updater -f -n 50
```
