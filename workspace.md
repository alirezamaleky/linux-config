# Linux

## Apps

```bash
apt install -y cron curl git htop make nano net-tools tmux unrar unzip vim wget
apt install -y optipng jpegoptim
apt install -y x265 x264 ffmpeg
apt install -y youtube-dl
```

```bash
snap install code --classic
snap install telegram-desktop
snap install obs-studio
snap install postman
snap install skype --classic
snap install spotify
snap install uget --edge
snap install vlc
```

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
nvm install --lts
```

```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
apt update && apt install --no-install-recommends yarn
```

## Privacy

```bash
echo $'\n# Privacy' >> ~/.bashrc
echo 'history -c' >> ~/.bashrc
echo 'rm -rf ~/.bash_history ~/.wget-hsts ~/.viminfo' >> ~/.bashrc
```
