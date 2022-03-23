## Installing programs

- **Generate ssh key**   
`ssh-keygen -t rsa`  
If a config file is needed:  
`touch ~/.ssh/config`  

- **Install git**  
`sudo apt install git`  
`git config --global user.name "Aleksei Briushinin"`  
`git config --global user.email "a.briushinin@novotorica.com"`  

- **Install telegram**  
`wget https://telegram.org/dl/desktop/linux`  
`sudo tar xJf linux -C /opt/`  
`sudo ln -s /opt/Telegram/Telegram /usr/local/bin/telegram-desktop`  

- **Install postman**  
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

 - **Install sublime text**  
`wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`  
`sudo apt install apt-transport-https`  
`echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`  
`sudo apt update`  
`sudo apt install sublime-text`



