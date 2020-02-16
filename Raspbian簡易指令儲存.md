## 新增 PPA 個人套件庫
```
sudo add-apt-repository ppa:
```
## 移除 PPA 個人套件庫
```
sudo add-apt-repository --remove ppa:
```
## 支援exFAT(FAT64)
```
sudo apt-get install 'exfat-utils'
sudo apt-get install 'exfat-fuse'
```
省略的
```
sudo apt-get install 'exfat-*'
```
舊版用法
```
sudo apt-add-repository ppa:relan/exfat
sudo apt-get update
sudo apt-get install 'exfat-utils'
sudo apt-get install 'exfat-fuse'
```
## 安裝.deb檔
```
(cd位置目標設定)sudo dpkg -i *.deb
```
## 移除套件
```
sudo apt-get remove --purge '(套件名稱)'
```
## 溫度查詢
```
vcgencmd measure_temp
```
## 卸載USB
```
sudo eject /dev/sdXX(移除指定的Device裝置,用fdisk -l 檢視裝置)
```
## vchiq影片播放問題
```
sudo chmod 447(最大權限777) /dev/vchiq
```
## 給予使用Bash權限
```
(cd位置目標設定)chmod u+x P.sh (P是檔案名稱，副檔名為.sh)
```
## CPU100% 10次壓力溫度測試(腳本)
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
-----------------------------------------------------
## 其他
##### >(建立文字檔)
##### touch(建立檔案)
##### cat(瀏覽或編輯文字檔)
##### cat>文字檔(新增文字檔或覆蓋原有的文字並編輯)
##### cat>>文字檔(編輯加入文字而不覆蓋原有的文字)
## 鍵盤動作
##### Ctrl+D(存檔在cat編寫的文字)
##### Ctrl+C(中止目前的執行)
