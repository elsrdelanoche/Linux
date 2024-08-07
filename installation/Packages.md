# Based on Debian
This is a compilation of the packages I usually install when starting on a new Linux distribution.

Download the .deb files from the following links.
https://code.visualstudio.com/download 
https://mega.io/es/cmd#downloadapps
https://mega.io/es/desktop#downloadapps

```console
sudo apt update && upgrade
sudo apt-get install curl
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
sudo apt update
sudo apt install brave-browser
sudo apt-get install neofetch
sudo apt install --reinstall build-essential
sudo apt-get install git cmatrix
sudo apt-get install golang
```

```console
cd Descargas
sudo dpkg -i *.deb
rm *.deb

sudo apt --fix-broken install -y
cd
```
```console
sudo apt-get install python -y
sudo apt-get install clang python3 -y
sudo apt-get install tree lolcat figlet -y
```

```console
sudo apt-get install git make pip npm node cargo -y
```

https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally/
