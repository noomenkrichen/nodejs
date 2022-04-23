# Steps to download and install nodejs in ubuntu
How to install latest NodeJS v16.14.2 LTS on the latest Ubuntu 22.04 LTS using the node-v16.14.2-linux-x64.tar.xz downloaded file.

# Step 1: Download latest or recommended node .tar.xz file from https://nodejs.org/en/
As of now, the latest stable and LTS version file is: node-v16.14.2-linux-x64.tar.xz

# Step 2: Go to the directory in which (.tar.xz file) is downloaded.
It should be the /Download directory

# Step 3: Update System Repositories by running the following command
sudo apt update

# Step 4: Install the package xz-utils using the following command
sudo apt install xz-utils

# Step 5: Extract the .tar.xz file using the following command
sudo tar -xvf node-v16.14.2-linux-x64.tar.xz

# Step 6: Copy files to the files to /usr/ directory
sudo cp -r node-v16.14.2-linux-x64/{bin,include,lib,share} /usr/

# Step 7: Check the node version
node --version

Result In my case -> v16.14.2
