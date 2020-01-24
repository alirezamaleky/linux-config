# Firewald

## Install

```bash
yum install -y firewalld
systemctl start firewalld; systemctl enable firewalld
```

## Allow service

```bash
firewall-cmd --permanent --add-service=http
firewall-cmd --permanent --add-service=https
firewall-cmd --reload
```

## Allow port

```bash
firewall-cmd --permanent --zone=public --add-port=8000/tcp
```
