# Tor

## Install

```bash
apt install -y tor
```

```bash
systemctl start tor; systemctl enable tor
```

## Bridges

[Get Bridge](https://bridges.torproject.org/bridges)

```bash
echo 'UseBridges 1' >> /etc/tor/torrc
echo 'Bridge ip:port hash' >> /etc/tor/torrc
```

## Location

```bash
echo 'ExcludeNodes {US},{CA}' >> /etc/tor/torrc
echo 'ExitNodes {GB},{UA},{AT},{DK},{FR},{DE}' >> /etc/tor/torrc
```
