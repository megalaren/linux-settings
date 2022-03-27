## Installing programs

- **Generate ssh key**   
`ssh-keygen -t rsa`  
If a config file is needed:  
`touch ~/.ssh/config`  

- **Install git**  
`sudo apt install git`  
`git config --global user.name "Aleksei Briushinin"`  
`git config --global user.email "a.briushinin@novotorica.com"`  

- **Install docker**  
Remove old docker versions:  
`sudo apt remove docker docker-engine docker.io containerd runc`  
`sudo apt update`  
  Install packages for https download:  
  ```
  sudo apt install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common -y
  ```
  Add a GPG key:  
`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`  
Add a Docker Repository:  
Ubuntu:  
`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`  
Linux mint:  
`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(. /etc/os-release; echo "$UBUNTU_CODENAME") stable"`  
`sudo apt update`  
Install docker:  
`sudo apt install docker-ce docker-compose -y`  
 Check Docker is running:  
`sudo systemctl status docker`  
Automatic start of the docker daemon at system startup:  
`sudo systemctl enable docker`  

- **Install Telegram**  
`wget https://telegram.org/dl/desktop/linux`  
`sudo tar xJf linux -C /opt/`  
`sudo ln -s /opt/Telegram/Telegram /usr/local/bin/telegram-desktop`  

- **Install Postman**  
`wget https://dl.pstmn.io/download/latest/linux64`  
`sudo tar xzf linux64 -C /opt/`  
`touch ~/.local/share/applications/Postman.desktop`  
  Open file in editor, paste text:
  ```
  [Desktop Entry]
  Encoding=UTF-8
  Name=Postman
  Exec=/opt/Postman/app/Postman %U
  Icon=/opt/Postman/app/resources/app/assets/icon.png
  Terminal=false
  Type=Application
  Categories=Development;
  ```
  Run as root to update:  
  `sudo /opt/Postman/app/postman -no-sandbox`

- **Install Sublime Text**  
`wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`  
`sudo apt install apt-transport-https`  
`echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`  
`sudo apt update`  
`sudo apt install sublime-text`  
  Preferences -> Settings, paste text:  
  ```
  {
    "color_scheme": "Packages/Color Scheme - Legacy/IDLE.tmTheme",
    "font_size": 10,
    "ignored_packages":
    [
        "Vintage",
    ],
    "margin": 0,
    "theme": "Default.sublime-theme",
    "ui_scale": 1.25,
  }
  ```
- **Install Rocket Chat**  
Download deb package from here:   
`https://github.com/RocketChat/Rocket.Chat.Electron/releases`  

- **Install PyCharm**  
Download from here:  
`https://www.jetbrains.com/ru-ru/pycharm/download/#section=linux`  
`sudo tar xzf pycharm-*.tar.gz -C /opt/`  
`cd /opt/pycharm-*/bin`  
`sh pycharm.sh`  
  Tools -> Create Desktop Entry  
  
  To update:  
`sudo chown -R laren:root /opt/pycharm_dir/`  
  The program will update and after restarting it will offer to import the previous configuration file, which is usually located here: `~/.PyCharm201X.X/config`  
  After update:  
`sudo chown -R root:root /opt/pycharm_dir/`  

- **Install Skype**  
`curl -s https://repo.skype.com/data/SKYPE-GPG-KEY | sudo apt-key add -`  
`echo "deb https://repo.skype.com/deb stable main" | sudo tee -a /etc/apt/sources.list.d/skype.list`  
`sudo apt update`  
`sudo apt -y install skypeforlinux`  

- **Install Zoom**  
`https://zoom.us/download`  
