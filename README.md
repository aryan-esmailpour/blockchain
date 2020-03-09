
![Hyperledger Sawtooth](images/sawtooth_logo_light_blue-small.png)

# Blockchain98

This essay is an instruction to execute projects of blockchain cource (Mathematics and computer science, Amirkabir university of technology ).
## Contents

- [Prerequisite](#Prerequisite)
- [Clone Project](#Clone Project)
- [Start Up](#Start Up)
  - [Run Processor](#Run Processor)
  - [Run Ledger-Sync](#Run Ledger-Sync)
  - [Run Server](#Run Server)
  - [Run App](#Run App)
- [Test](#Test)
- [Development](#development)




## Prerequisite

You should first install [Docker](https://www.docker.com/what-docker). You can install it by the following command in terminal of Ubuntu:
```bash
sudo apt install docker.io
```

Now install **docker-compose** by the following command:
```bash
sudo apt install curl
```
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```
Now check the version:
```bash
docker-compose --version
```

Install **nvm** and **node**.  first nvm:
```bash
    sudo apt-get update
    sudo apt-get install build-essential libssl-dev
	curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh -o install_nvm.sh
	bash install_nvm.sh
	source ~/.profile
```
Now for install node, run the command:
```bash
nvm install 12
```

The best way to get and manage project is **git**. install it with:
```bash
sudo apt-get install git
```
##  Clone Project

Now you can by the following command get the project:

Go to project folder and run command:
```bash
docker-compose up
```
This will take awhile the first time it runs, but when complete will be running
all required components in separate containers. Many of the components will be available through HTTP endpoints. If everything is ok, the following services will run:

- **Sawtooth-validator**
- **Sawtooth-settings-tp**
- **Sawtooth-intkey-tp-python**
- **Sawtooth-devmode-engine-rust**
- **Sawtooth-rest-api** will be at **http://localhost:8024**
- **Sawtooth-shell**
- **RethinkDB** will be at **http://localhost:8023**
- **MongoDB** 

In bash you can shutdown these components with the key combination: `ctrl-C`.
You can shutdown _and_ remove the containers (destroying their data), with the
command:

```bash
docker-compose down
```
## Start Up
Running `docker-compose up`, will automatically run all scripts necessary to
use all Infrastructure components. 

### Run Processor

Go to processor folder and run the following commands.
```bash
npm install
```
```bash
node index.js
```
### Run Ledger-Sync

Go to ledger-sync folder and run the following commands.
```bash
npm install
```
```bash
node index.js
```
### Run Server

Go to server folder and run the following commands.
```bash
npm install
```
```bash
node index.js
```
### Run App

Go to app folder and run the following commands.
```bash
npm install
```
```bash
npm run start
```
Now open a browser and go to **http://localhost:3000**. If you see the greeting , everything is ready.
## Test
The following routes are ready. You should develope in according to your paln.

- **http://localhost:3000/register** to register.
- **http://localhost:3000/login** to login.
- **http://localhost:3000/chargeAccount** to charge account.

After login, click `تولید کلید` to generate key pair. Save the private key. Go to **http://localhost:3000/chargeAccount**. Fill the form and sign it with the private key. After the transaction you should see the change in balance. 

## Developement

Now its your turn ...!

please contact me if you have questions.





