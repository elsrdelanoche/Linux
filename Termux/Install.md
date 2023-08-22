Install from https://github.com/termux/termux-app

After install
```console
apt update && apt upgrade
termux-setup-storage
apt list
```

optional
https://github.com/mayTermux/myTermux
```console
apt update && upgrade
pkg i -y git bc
git clone --depth=1 https://github.com/mayTermux/myTermux.git
export COLUMNS LINES
./install.sh
```
si aparece advertencia, dar zoom out


```console
apt install git curl wget nvim zip unzip python3
apt update && upgrade
```



```console
#!/data/data/com.termux/files/usr/bin/bash

for i in termux-api termux-elf-cleaner termux-tools util-linux x11-repo apr apr-util autoconf axel bat bc fontconfig-utils bison clang cmake coreutils curl debianutils dns2tcp dnsutils file findutils fish gawk git gpgme hexedit irssi jq libassuan libffi libgcrypt libgmp libgpg-error libgrpc libiconv libmpc libmpc-static libmpfr libmpfr-static libpcap libsodium libsodium-static libsqlite libtool libxml2 libxml2-static libxml2-utils libxslt libxslt-static gnupg make man megatools mlocate ncurses ncurses-utils neofetch nodejs rust ninja openjdk-17 openssh openssl openssl-tool perl php php-apache pkg-config procps proot pv python2 python ruby readline sqlite strace tar tor torsocks translate-shell unzip weechat wget youtubedr zip zlib
do
    yes|apt install $i
done
echo "chsh -s fish" > ~/.bashrc
```
