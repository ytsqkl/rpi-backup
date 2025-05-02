# rpi-backup

树莓派系统备份脚本     
## 一、back.sh（备份脚本，需要root权限）   
   ‌操作步骤‌：  
   克隆脚本：rpi-rw; git clone https://github.com/nanhantianyi/rpi-backup.git && cd rpi-backup   
‌   用法：sudo bash back.sh xxx.img  (xxx.img为备份文件名，自行修改)  
   **1. 备份镜像大小计算：(boot分区全部 + root分区已使用) * 1.2**     
   **2. 如果sd卡剩余空间充足，可以备份到卡内，如果剩余空间有限，请备份到外部设备**     
   **3. 如果需要备份到外部设备，设备务必挂载到/media,不要挂载到/mnt,因为创建的镜像会挂载到/mnt进行操作**     
## 二、resize.sh（扩容脚本，需要root权限）  
   用法：img镜像写入工具恢复系统后执行 sudo bash resize.sh 扩容root分区，也可以用树莓派raspi-config进行扩容
