```Windows 11 to install Curl, Ubuntu, NVM, Node, and Yarn.
// => comment     > => command from Powershell (admin)      $ => command from Ubuntu (bash)     && => 'and'


// powershell (admin)
> wsl --install
> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

&&

IN A BROWSER => https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

&&

$ wsl --set-default-version 2
$ wsl --list --verbose
$ wsl --install -d Ubuntu

&& *restart machine*

// open windows terminal (admin)
> bash

&&

// curl install
sudo apt update
sudo apt install curl

&&

// nvm install
$ curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
$ source ~/.profile

&&

// node && nodejs install
$ nvm install node
$ nvm install node
$ nvm install 14.18.1
$ nvm uninstall v17.1.0
$ node -v

&&

// yarn install
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt install --no-install-recommends yarn
$ sudo apt update
$ yarn -v
```
