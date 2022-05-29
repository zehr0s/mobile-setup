# A mobile setup

## Firefox (Nightly/Beta)
1. Toggle Desktop Mode.
2. Search [your User Agent](https://duckduckgo.com/?q=my+user+agent&ia=answer).
    - Copy User Agent e.g: Mozilla/5.0 (X11; Linux x86_64; rv:91.0) Gecko/20100101 Firefox/91.0
3. Type about:config in the address bar.
4. Create a new entry
    - Type: string
    - Name: general.useragent.override
    - Value: [your user agent](https://duckduckgo.com/?q=my+user+agent&ia=answer).
5. Restart browser.

## Termux
```bash
# Permissions
termux-setup-storage

# Packages
pkg install git
pkg install python
pkg install wget
pkg install ffmpeg

# Python modules
pip install requests
pip install youtube-dl

# Directories
mkdir $HOME/storage/external-1/scripts
mkdir -p $HOME/bin

# Dowloader
wget https://raw.githubusercontent.com/zehr0s/mobile-setup/main/termux-url-opener -O $HOME/bin/termux-url-opener
chmod +x $HOME/bin/termux-url-opener

# Spiders (wget)
wget https://raw.githubusercontent.com/zehr0s/spiders/main/createGallery -O $HOME/storage/external-1/scripts/createGallery.py
wget https://raw.githubusercontent.com/zehr0s/spiders/main/zahard/pwnWindBreaker -O $HOME/storage/external-1/scripts/pwnWindBreaker.py

# Spiders (git)
# git clone https://github.com/zehr0s/spiders $HOME/storage/external-1/scripts/spiders
```
