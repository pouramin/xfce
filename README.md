# xfce : دسکتاپ گرافیکی در لینوکس
#### این نسخه روی اوبنتو 20 نصب شده، برای توزیعای دیگه بررسی کنید اسکریپت با توزیع هم خوانی داشته باشه

###### Video : لینک ویدیو یوتیوب
```

```

###### خرید دامنه از نیم چیپ: 
```
https://namecheap.pxf.io/BX7m6W
```
###### خرید دامنه سایت ایرانی: 
```
https://www.hub.shatelhost.com/aff.php?aff=290
```
###### خرید سرور از دیجیتال اوشن : 
```
https://m.do.co/c/0fb522deafa4
```
###### خرید سرور از سایت ایرانی : 
```
https://dashboard.azaronline.com/order/?aff=790
```

**If you think this project is helpful to you, you may wish to give a** 🌟

**Feel Free To Donation :** ❤️

>TRC20: ```TGTyqv2MH7dZztMvaP5PKuS9Bma8RY5Pk8```

>ETH: ```0x5b5202a54e5ce4fb25f0d886254eeb07bb088614```

###### Update & Upgrade Server : آپدیت و آپگرید سرور

```
sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get autoremove -y 
```

###### Import xfce : نصب و ایمپورت شبیه ساز

```
apt install -y xfce4 xfce4-goodies
```
###### Install Vnc : نصب وی ان سی

```
apt install tightvncserver autocutsel
```
###### Add User : ساخت یوزر

```
useradd -m -s /bin/bash USERNAME

```
###### User Mode : تغییر نوع یوزر

```
usermod -aG sudo USERNAME
```
###### Set User Pass : پسورد برای یوزر
```
passwd USERNAME
```
###### Change User root to USERNAME : تغییر یوزر از روت به کاربری که ساختیم
```
su - USERNAME_HERE
```
###### Set VNC Password : ست کردن پسورد وی ان سی
```
vncpasswd
```
###### VNC XstartUp : تنظیمات استارت آپ وی ان سی
```
nano ~/.vnc/xstartup
```
###### Paste the following code in nano :  کدای زیر رو توی تکست ادیتو پیست کنید
```
#!/bin/bash

xrdb $HOME/.Xresources
autocutsel -fork
startxfce4 &
```
###### Change Permission : تغییر دسترسی دایرکتوری وی ان سی
```
chmod 755 ~/.vnc/xstartup
```
###### Run the VNCServer : راه اندازی وی ان سی
```
vncserver
```
###### Enable the vnc on root : فعالسازی وی ان سی در روت
```
nano /etc/systemd/system/vncserver@.service
```
###### Paste the following code in nano :  کدای زیر رو توی تکست ادیتو پیست کنید
###### Don't forget to Change the USERNAME to YouR Created USER
```
[Unit]
Description=Start VNC server at startup
After=syslog.target network.target

[Service]
Type=forking
User=USERNAME
Group=USERNAME
WorkingDirectory=/home/USERNAME

PIDFile=/home/USERNAME/.vnc/%H:%i.pid
ExecStartPre=-/usr/bin/vncserver -kill :%i > /dev/null 2>&1
ExecStart=/usr/bin/vncserver -depth 24 -geometry 1920x1080  :%i
ExecStop=/usr/bin/vncserver -kill :%i

[Install]
WantedBy=multi-user.target
```
###### Enable Vncserver : فعالسازی وی ان سی
```
systemctl enable vncserver@1
```
###### Start Vncserver : استارت وی ان سی سرور
```
systemctl start vncserver@1
```

###### To install firefox and chrome : برای نصب فایرفاکس
```
sudo apt install firefox
```
##### Extract and Install Chrome : اکسترکت و نصب کروم
```
d Downloads/

ls -l

sudo dpkg -i ---

sudo apt install -f
```





