### Steps to download and install nodejs in ubuntu
How to install latest NodeJS version on Linux Ubuntu Desktop or Server using the .tar.xz downloaded file.

#### Step 1: Download latest or recommended node .tar.xz file from [Node JS official website](https://nodejs.org/en/download)
Make sure you select Linux from the drop down menu.

#### Step 2: Go to the directory in which (.tar.xz file) is downloaded.
It should be the /Download directory

#### Step 3: Update System Repositories by running the following command
```bash
sudo apt update
```

#### Step 4: Install the package xz-utils using the following command
```bash
sudo apt install xz-utils
```

#### Step 5: Extract the .tar.xz file using the following command
```bash
sudo tar -xvf node-v22.14.0-linux-x64.tar.xz
```

#### Step 6: Copy files to the files to /usr/ directory
```bash
sudo cp -r node-v22.14.0-linux-x64/{bin,include,lib,share} /usr/
```

#### Step 7: Check the node version
```bash
node --version
```

Result In my case -> v22.14.0
