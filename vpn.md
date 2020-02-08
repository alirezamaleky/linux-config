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

## Warp

### Install

```bash
sudo add-apt-repository ppa:wireguard/wireguard
sudo apt install -y wireguard resolvconf

wget https://gist.githubusercontent.com/oskar456/594f1b5e84ca887c439fb457800b377e/raw/ec61b40885eaf6c36e7680c5bd6231202eda8673/wgcf.py
chmod +x ./wgcf.py
sudo ./wgcf.py
```

### Usage

```bash
sudo wg-quick up /home/ubuntu/.wgcf/wgcf.conf
```
