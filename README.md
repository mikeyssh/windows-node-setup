```Windows 11 to install Curl, Ubuntu, NVM, Node, and Yarn.
// => comment     > => command from Powershell (admin)      $ => command from Ubuntu (bash)     && => 'and'


// powershell (admin)
> wsl --install
> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

&&
> wget https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

if that doesn't work, try in browser => https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

&&

&& *restart machine*

// open windows terminal (admin)

> wsl --set-default-version 2
> wsl --install -d Ubuntu

// open windows terminal

> bash

// curl install
sudo apt install curl

&&

// nvm install
$ curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
$ source ~/.profile

&&

// node && nodejs install

$ nvm install v14.18.1
$ node --version

&&

// yarn install
$ sudo apt update
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt install --no-install-recommends yarn
$ yarn --version
```
