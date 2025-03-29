# Method to Install Latest version of NodeJS on Ubuntu Desktop
How to install latest NodeJS version on Linux Ubuntu Desktop or Server using the .tar.xz downloaded file.
## 1. Download latest or recommended node .tar.xz file from [Node JS official website](https://nodejs.org/en/download)
Make sure you select Linux from the drop down menu.
## 2. Go to the directory in which (.tar.xz file) is downloaded.
It should be the /Download directory
```bash
cd Download
```
Check the file in the folder
```bash
ls
```
## 3. Update System Repositories by running the following command
```bash
sudo apt update
```
## 4. Install the package xz-utils using the following command
```bash
sudo apt install xz-utils
```
## 5. Extract the .tar.xz file using the following command
In this case the file downloaded is version 22.14.0 of nodejs
```bash
sudo tar -xvf node-v22.14.0-linux-x64.tar.xz
```
## 6. Copy extracted files under /usr/ directory using the following command
```bash
sudo cp -r node-v22.14.0-linux-x64/{bin,include,lib,share} /usr/
```
## 7. Check the node version
```bash
node --version
```
## 8. Check npm version
```bash
npm --version
```
Result In my case -> v22.14.0
