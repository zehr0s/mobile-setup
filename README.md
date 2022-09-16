# A mobile setup

## Termux
To download media from YT and TT run this lines of code in [Termux](https://wiki.termux.com/wiki/Main_Page), then share an url with [Termux](https://wiki.termux.com/wiki/Intents_and_Hooks).

```bash
# Permissions
termux-setup-storage

# Packages (use apt in case pkg is not working)
pkg install git
pkg install python
pkg install wget
pkg install ffmpeg

# Python modules
pip install requests
pip install youtube-dl
pip install json
pip install beautifulsoup4

# Bin directory
mkdir -p $HOME/bin

# TT Downloader
wget https://raw.githubusercontent.com/zehr0s/mobile-setup/main/tiktok-dl -O /data/data/com.termux/files/usr/bin/tiktok-dl
chmod +x /data/data/com.termux/files/usr/bin/tiktok-dl

# YT Downloader
wget https://raw.githubusercontent.com/zehr0s/mobile-setup/main/termux-url-opener -O $HOME/bin/termux-url-opener
chmod +x $HOME/bin/termux-url-opener

# DEPRECATED: Spiders (wget)
# mkdir $HOME/storage/external-1/scripts
# wget https://raw.githubusercontent.com/zehr0s/spiders/main/createGallery -O $HOME/storage/external-1/scripts/createGallery.py
# wget https://raw.githubusercontent.com/zehr0s/spiders/main/zahard/pwnWindBreaker -O $HOME/storage/external-1/scripts/pwnWindBreaker.py
# git clone https://github.com/zehr0s/spiders.git 

# DEPRECATED: Spiders (git)
# git clone https://github.com/zehr0s/spiders $HOME/storage/external-1/scripts/spiders
```

## Firefox (Nightly/Beta)
Set Firefox to Desktop Mode permanently.

1. Toggle Desktop Mode.
2. Search [your User Agent](https://duckduckgo.com/?q=my+user+agent&ia=answer).
    - Copy User Agent e.g: Mozilla/5.0 (X11; Linux x86_64; rv:91.0) Gecko/20100101 Firefox/91.0
3. Type about:config in the address bar.
4. Create a new entry.
    - Type: string
    - Name: general.useragent.override
    - Value: [your user agent](https://duckduckgo.com/?q=my+user+agent&ia=answer).
5. Restart browser.
