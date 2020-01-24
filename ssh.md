# SSH

## Security

```bash
echo "Protocol 2" >>/etc/ssh/sshd_config
echo "AllowUsers root" >>/etc/ssh/sshd_config
echo "ClientAliveCountMax 0" >>/etc/ssh/sshd_config
echo "ClientAliveInterval 3600" >>/etc/ssh/sshd_config
echo "PermitEmptyPasswords no" >>/etc/ssh/sshd_config
```

## OTP

```bash
yum install -y google-authenticator
google-authenticator
echo "auth required pam_google_authenticator.so" >>/etc/pam.d/sshd
```

```bash
vim /etc/ssh/sshd_config
```

```
ChallengeResponseAuthentication yes
```

## Restart

```bash
service sshd restart
```
