# docker-run-nginx-php-fpm-mysql-wordpress
1.Install docker
ตั้งค่า Repository  ติดตั้งแพคเกจสำหรับให้ apt ติดตั้งแพคเกจผ่าน HTTPS ได้

* apt-get install \

   apt-transport-https \
   
   ca-certificates \
   
   curl \
   
   software-properties-common

เพิ่ม Docker GPG Key

* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

ยืนยันคีย์ว่าตรงกับ 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88
* apt-key fingerprint 0EBFCD88

pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid                  Docker Release (CE deb) <docker@docker.com>
sub   4096R/F273FCD8 2017-02-22

เพิ่ม Stable repository

* add-apt-repository \

   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   
   $(lsb_release -cs) \
   
   stable"
   
ติดตั้ง Docker


