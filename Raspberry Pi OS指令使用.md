# 相關網址&後續設定
## 下載區
一開始不確定要用哪個系統和不會燒錄SD卡者，可以選NOOBS使用<br>
若確定要使用哪個系統但猶豫選擇或不太會操作者，推薦他們自家的 Raspberry Pi Imager
```
https://www.raspberrypi.org/downloads/
```
## 保護您的Raspberry Pi(Raspberry Pi OS)
在基礎設定下完成之後，由於裡面設定還是預設狀態，而pi使用者跟Windows的系統管理員權限相當，可能會有入侵風險(帶有防火牆的路由器雖安全，但也建議做)，下列操作是個人增加安全性的方法
```
1.用passwd更改pi的密碼
2.安裝ufw防火牆套件(詳細參見第二個網址)並設定
3.開始新增使用者名稱(也就是之後主要的用戶)並給予權限(詳細參見第一個網址的3、4條指令)
4.要求pi用戶使用sudo時要用戶密碼(詳細參見第一個網址的9、10條指令，vi的用法在倒數第二個)
5.使用sudo passwd指令來設定UNIX密碼(之後若把Pi鎖住或刪除時要使用Root權限或sudo無法使用時，這是唯一後路)
6.切換使用者後用sudo passwd --lock pi來鎖定pi(解鎖sudo passwd --unlock pi)，或刪除pi(詳細參見第一個網址的6~8條指令)，但我不建議對pi做刪除的動作，以防跟pi有關的問題發生
```
```
https://www.raspberrypi.org/documentation/configuration/security.md
```
```
https://www.taiwaniot.com.tw/%E6%8A%80%E8%A1%93%E6%96%87%E4%BB%B6/%E6%A8%B9%E8%8E%93%E6%B4%BE%E6%8A%80%E8%A1%93%E6%96%87%E4%BB%B6/%E6%A8%B9%E8%8E%93%E6%B4%BE%EF%BC%8Draspberry%EF%BC%8C%E5%85%A7%E7%BD%AE%E7%9A%84%E9%98%B2%E7%81%AB%E7%89%86ufw%E8%A8%AD%E7%BD%AE%E5%92%8C%E5%95%9F%E7%94%A8/
```
若在新用戶裡無法使用sudo時，可查看下面網址
```
https://www.itread01.com/content/1532680819.html
```
# APT運用
## 更新
```
sudo apt update  (需要時再改成apt-get)
```
## 升級
```
sudo apt upgrade (需要時再改成apt-get)
```
## 完整升級
```
sudo apt full-upgrade (apt-get為另一條指令，無法套用)
```
## 新增 PPA 個人套件庫
```
sudo add-apt-repository ppa:
```
## 移除 PPA 個人套件庫
```
sudo add-apt-repository --remove ppa:
```
## 安裝套件
```
sudo apt install (套件名稱) (需要時再改成apt-get)
```
## 移除套件
```
sudo apt purge (套件名稱) (需要時再改成apt-get)
```
或
```
sudo apt remove --purge '(套件名稱)' (需要時再改成apt-get)
```
## 自動移除套件(相依套件)
```
sudo apt autoremove (需要時再改成apt-get)
```
## 清除之前安裝(install)的安裝檔
```
sudo apt clean (需要時再改成apt-get)
```
## 清除之前下載的安裝檔，但不刪除已安裝軟體的安裝檔
```
sudo apt autoclean (需要時再改成apt-get)
```
# 已知套件
"apt"有問題的話再改成"apt-get"看看

## 支援exFAT(FAT64)
```
sudo apt install exfat-utils
sudo apt install exfat-fuse
```
#### 省略的
```
sudo apt install 'exfat-*'
```
#### 舊版(無法更新)用法
```
sudo apt-add-repository ppa:relan/exfat
sudo apt-get update
sudo apt-get install 'exfat-utils'
sudo apt-get install 'exfat-fuse'
```
## 支援NTFS
```
sudo apt install ntfs-3g-dev
```
## 印表機
```
sudo apt install libcups2-dev
sudo apt install cups
sudo apt install system-config-printer
```
## 光碟燒錄軟體
注意!!請在足夠的電源下再使用光碟機!!!
### K3b(比較推薦)
```
sudo apt install k3b
```
### Xfburn(易於操作)
```
sudo apt install xfburn
```
## GNOME磁碟(可執行格式化＆完整格式化)
建議！完整格式化請在電源充足的情況(不能出現閃電降壓符號)並且搭配主動式散熱器(風扇+散熱片)使用
```
sudo apt install gnome-disk-utility
```
## Nautilus檔案瀏覽器(GNOME檔案瀏覽器)
```
sudo apt install nautilus
```
## GParted(硬碟分割區軟體)
```
sudo apt install gparted
```
## Audacity(錄音與音訊編輯器，須搭配USB聲卡使用)
```
sudo apt install audacity
```
## Kdenlive(影片編輯器)
```
sudo apt install kdenlive
```
## GIMP(圖像編輯器)
```
sudo apt install gimp
```
## GNOME影像檢視器(可順利跑GIF檔，BCM2835無法)
```
sudo apt install eog
```
## Calibre(電子書軟體)
```
sudo apt install calibre
```
## Firefox瀏覽器
```
sudo apt install firefox-esr
```
## Chromium瀏覽器
```
sudo apt install chromium-browser
```
# 其他指令
## 安裝.deb檔
```
(先用"cd"調整該檔資料夾的位置)sudo dpkg -i *.deb
```
## 溫度狀態
```
vcgencmd measure_temp
```
## 時鐘速度狀態
```
watch -n 0 vcgencmd measure_clock arm  ("0"為0.1秒刷新。若改為"1"為1秒刷新、"2"為2秒刷新，以此類推)
```
## 卸載USB
```
sudo eject /dev/sdXX(XX是移除該位置的裝置。可以用"fdisk -l"檢視該裝置的位置)
```
## vchiq影片播放問題
```
sudo chmod 447(最大權限777) /dev/vchiq
```
## 給予使用Bash權限
```
(先用"cd"調整該檔資料夾的位置)chmod u+x P.sh ("P"是檔案名稱，副檔名為".sh")
```
## CPU 10次壓力溫度測試(sh腳本)
```
(來自ExplainingComputers.com)
#! /bin/bash
clear

for x in {1..10}
do
  vcgencmd measure_temp
  sysbench --test=cpu --cpu-max-prime=20000 --num-threads=4 run >/dev/null 2>&1
done
 
vcgencmd measure_temp
```
# vi簡單用法
## 操作模式
```
a 由游標之後進行寫入模式
```
```
i 由游標之前進行寫入模式
```
```
o 新增一行於該行之下進行寫入模式(如同Enter鍵後開始打字)
```
```
x 刪除游標該字
```
```
dd 刪除游標該行
```
```
:w 存檔
```
```
:w! 強制存檔
```
```
:q 退出
```
```
:q! 強制退出
```
```
:x 存檔後離開(僅當檔案被修改時才寫入,並更新檔案修改時間,否則不會更新檔案修改時間)
```
```
:wq 存檔後離開(強制更新檔案的修改時間)
```
## 寫入模式
```
esc 退出寫入模式到操作模式
```
# 其他操作
##### >(建立檔案)
##### touch(建立檔案或修改檔案時間)
##### cat(瀏覽或編輯文字檔)
##### cat>文字檔(新增文字檔或覆蓋原有的文字並編輯)
##### cat>>文字檔(編輯加入文字而不覆蓋原有的文字)
## 鍵盤動作
##### Ctrl+D(存檔在cat編寫的文字)
##### Ctrl+C(中止目前的執行)
