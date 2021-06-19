# Qortal UI 

Decentralizing The World

Building and Running Qortal UI Server from source:
-----------------------------------------------------
Follow the steps below to download, install, build and run Qortal UI locally.


Installation
------------
Packages required:
 - Node.js
 - npm
 - yarn

Easiest way to install the lastest required packages is via nvm. 

``` sudo apt update && sudo apt install curl -y ``` <br/>
``` curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash ``` <br/>
``` source ~/.profile ``` (For Debian based distro) <br/>
``` source ~/.bashrc ``` (For Fedora / CentOS) <br/>
``` nvm ls-remote ``` (Fetch list of available versions) <br/>
``` nvm install v14.17.0 ```  (Latest LTS: Fermium as of writing) <br/>
``` npm -g install yarn ``` <br/>

Verify with node --version <br/>

Clone the following repos
 - ``` git clone https://github.com/Qortal/qortal-ui.git ```
 - ``` git clone https://github.com/Qortal/qortal-ui-core.git ```
 - ``` git clone https://github.com/Qortal/qortal-ui-plugins.git ```
 - ``` git clone https://github.com/Qortal/qortal-ui-crypto.git ```

Dependency installation and linking
-----------------------------------
In `qortal-ui-core/`, `qortal-ui-plugins/`, `qortal-ui-crypto/`  directories, run: 
```
yarn install
yarn link
```

Finally, in the `qortal-ui` directory, run:
```
yarn install
yarn link qortal-ui-core
yarn link qortal-ui-plugins
yarn link qortal-ui-crypto
```



Build UI server and files
-------------------------
In `qortal-ui` directory, run:
```
yarn run build
```

Start UI Server
---------------
```
yarn run server
```


Run UI using electron
---------------------
```
yarn run start-electron
```
