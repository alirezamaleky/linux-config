## Tor

### Install

```bash
sudo apt install -y tor
```

```bash
sudo systemctl start tor; sudo systemctl enable tor
```

### Bridges

[Get Bridge](https://bridges.torproject.org/bridges)

```bash
echo 'UseBridges 1' >> /etc/tor/torrc
echo 'Bridge ip:port hash' >> /etc/tor/torrc
```

### Location

```bash
echo 'ExcludeNodes {US},{CA}' >> /etc/tor/torrc
echo 'ExitNodes {GB},{UA},{AT},{DK},{FR},{DE}' >> /etc/tor/torrc
```

## ProtonVPN

### Install

```bash
sudo apt install -y openvpn dialog python3-pip python3-setuptools
sudo pip3 install protonvpn-cli
sudo protonvpn init
```

### Usage

```
sudo protonvpn c -f -p UDP
```
