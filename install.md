# linux-settings
- Generate ssh key:  
```ssh-keygen -t rsa```
- Install git:  
```sudo apt install git```
- Install telegram:  
```wget https://telegram.org/dl/desktop/linux```  
```sudo tar xJf linux -C /opt/```  
```sudo ln -s /opt/Telegram/Telegram /usr/local/bin/telegram-desktop```
- Install postman:  
```wget https://dl.pstmn.io/download/latest/linux64```  
```sudo tar xzf linux64 -C /opt/```  
```touch ~/.local/share/applications/Postman.desktop```  
Открыть файл редактором, вставит текст:  
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

Открыть и сохранить файл ~/.local/share/applications/Postman.desktop вручную



# Для обновления запустить от root:
sudo /opt/Postman/app/postman —no-sandbox
