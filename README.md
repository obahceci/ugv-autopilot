# ARDUPİLOT VE GAZEBO EKLENTİSİNİ KURULUMU 

**1- Gerekli bağımlılıkların kurulumu**

  $ sudo apt-get update

  $ sudo apt-get install python3-gz-sim8 


**2- Ardupilot gazebo eklentisi indirmek**

`git clone https://github.com/ArduPilot/ardupilot_gazebo`
`cd ardupilot_gazebo`


**3- İlk derlemeyi yapmak** 

`mkdir build && cd build`

`cmake ..`
    
`make -j4`



# GAZEBONUN EKLENTIYLE BİRLİKTE ÇALIŞTIRILMASI 

**1-  Ortam değişkenlerini tanıtmak (bu kod ~/.bashrc dosyasının içine yazılırsa kalıcı olur)**

#Eğer gazebo güncel olan dünyayı açamıyorsa öncekşi gazebo fonksiyonlarını kapat.

`pkill -9 gz`
`pkill -9 ruby`

#EKLENTİ YOLUNU TANIT 

`export GZ_SIM_RESOURCE_PATH=$GZ_SIM_RESOURCE_PATH:$HOME/ardupilot_gazebo/models:$HOME/ardupilot_gazebo/worlds`

`gz sim -v4 teknofest_final.sdf`    #aktif model dünyasını çalıştırır




# ÖNEMLİ NOTLAR : 

"~/ardupilot_gazebo/models/teknofest_rover/"  adresinde aracımızın model dosyaları bulunmaktadır

"~/ardupilot_gazebo/worlds/" adresinde teknofest parkurunun model dosyaları bulunur. Bu dosyalar teknofest parkurunun modellenmiş halidir.
