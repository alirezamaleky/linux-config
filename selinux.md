# SElinux

## Activate

```bash
sed -i 's/SELINUX=.*/SELINUX=enforcing/' /etc/selinux/config
```

```bash
reboot
```

## Enable

### Network

```bash
setsebool -P httpd_can_network_connect 1
```

### SSH
```bash
semanage port -a -t ssh_port_t -p tcp 123
```

### HTTP

```bash
semanage port -a -t http_port_t -p tcp 8000
```

### File

```bash
semanage fcontext -a -t httpd_sys_content_t .
semanage fcontext -a -t httpd_sys_rw_content_t "storage(/.*)?"
semanage fcontext -a -t httpd_sys_rw_content_t "bootstrap/cache(/.*)?"
restorecon -R -v .
```
