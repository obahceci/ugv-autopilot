ARDUPİLOT VE GAZEBO EKLENTİSİNİ KURMAK İÇİN:

1- Gerekli bağımlılıkların kurulumu

$ sudo apt-get update
$ sudo apt-get install python3-gz-sim8 


2- Ardupilot gazebo eklentisi indirmek

$ git clone https://github.com/ArduPilot/ardupilot_gazebo
$ cd ardupilot_gazebo


3- İlk derlemeyi yapmak 

$ mkdir build && cd build


$ cmake ..


$ make -j4



ÇALIŞTIRMAK İÇİN :

1-  Ortam değişkenlerini tanıtmak (bu kod ~/.bashrc dosyasının içine yazılırsa kalıcı olur)

$ export GZ_SIM_SYSTEM_PLUGIN_PATH=$HOME/ardupilot_gazebo/build:$GZ_SIM_SYSTEM_PLUGIN_PATH
