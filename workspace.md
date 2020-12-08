# Linux

## Privacy
```bash
echo $'\n# Privacy' >> ~/.bashrc
echo 'history -c' >> ~/.bashrc
echo 'rm -rf ~/.bash_history ~/.wget-hsts ~/.viminfo' >> ~/.bashrc
```

## Apps

```bash
sudo apt install -y cron curl git htop make nano net-tools tar tmux unrar unzip vim wget gnome-mpv
sudo apt install -y optipng jpegoptim
sudo apt install -y x265 x264 ffmpeg
sudo apt install -y youtube-dl
```

### Chrome
```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install -y ./google-chrome-stable_current_amd64.deb && rm -f google-chrome-stable_current_amd64.deb
```

### Spotify
```bash
curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | sudo apt-key add - 
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt update && sudo apt install -y spotify-client
```

### Skype
```bash
wget https://repo.skype.com/latest/skypeforlinux-64.deb
sudo apt install -y ./skypeforlinux-64.deb && rm -f skypeforlinux-64.deb
```

### Postman
```bash
wget https://dl.pstmn.io/download/latest/linux64 -O postman-linux-x64.tar.gz
tar -xf postman-linux-x64.tar.gz
sudo mv Postman /mnt && rm -f postman-linux-x64.tar.gz
```

### Lantern
```bash
wget https://github.com/getlantern/lantern-binaries/raw/master/lantern-installer-64-bit.deb
sudo apt install -y ./lantern-installer-64-bit.deb && rm -f lantern-installer-64-bit.deb
```

### NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
nvm install --lts
```

### Yarn
```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install --no-install-recommends -y yarn
```

### PHP
```bash
sudo add-apt-repository ppa:ondrej/php
sudo apt install -y php8.0-{common,cli}
sudo apt install -y php8.0-0{fpm,mbstring,curl,xml,mysql,zip}
```

### Composer
```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```
