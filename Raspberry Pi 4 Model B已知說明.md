## 事先警告:本文是善意提供，若有任何風險請自行負責
----------------------------------
## 降電壓
![image](https://github.com/HYDeReUb/TS4IE_4080E055/blob/master/Picture%20Saved/under_volt.png)
```
這代表著電力提供不足而導致終點端電壓過度下降(低於4.63V (+/-5%))，會調降CPU時鐘性能，需要更換符合指定的線材跟電源，若不需要太麻煩可以直接買他們的電源直接來用即可
```
```
造成的影響:會影響USB跟SD卡的運作，長期使用下會有損壞的可能性
```
## 溫度過高(80~85°C)
![image](https://github.com/HYDeReUb/TS4IE_4080E055/blob/master/Picture%20Saved/over_temperature_80_85.png)
```
這代表著溫度已經到達80~85°C，會調降CPU時鐘性能，需要更換或使用主動式散熱或被動式散熱
```
```
造成的影響:可能導致機器跟週邊的運行壽命縮短
```
## 溫度過高(85°C以上)
![image](https://github.com/HYDeReUb/TS4IE_4080E055/blob/master/Picture%20Saved/over_temperature_85.png)
```
這代表著溫度已經到達85°C以上，會調降CPU跟GPU時鐘性能，建議立即關機散熱，並更換或使用主動式散熱或被動式散熱
```
```
造成的影響:可能導致機器跟週邊的運行壽命縮短甚至損壞
```
## 主動式散熱
![image](https://i.ytimg.com/vi/5Ud-grj4Zl0/maxresdefault.jpg)
```
用風扇把熱氣帶走，需要時可以加散熱片一起使用
```
```
好處:可以維持一定溫度不再上升
適合:長時間運算操作、超頻玩家、保持低溫運作等
```
## 被動式散熱
![image](https://i.ytimg.com/vi/VJC6OpGpq0Y/maxresdefault.jpg)
```
純粹利用散熱片把熱導出來並慢慢消去而無使用風扇
```
```
好處:由於不需風扇，降低了耗電並增加了安靜感
適合:短時間運算操作、長時間待機、後續清理容易等
```
# Raspberry Pi 4 Model B已知問題
## USB部份
``` 
1.若要提供SSD、HDD、光碟機這樣的高耗電外接裝置時，在足夠電力的情況下只能選一個來使用，若同時使用兩個會不夠電並發生問題
2.若上述要使用2個以上時，只能接HUB並確保線材與電源提供電量充足
3.使用像Argon one有帶電源鍵的外殼，若在HUB有接電源的情況下可能會有開不了機的情況，重新插拔HUB的電源線即可解決
```
## 音訊部份
```
1.使用音效卡只能打開一個音訊程式，打開第二個會顯示忙碌或錯誤
2.若有用Argon one外殼，要注意音訊孔有些可能會插不夠深，導致只有單喇叭播放
```
## 其他部份
```
1.建議在執行格式化或移動檔案這樣的操作時，別執行其他程式來多工操作，避免使用量過高強關或重起導致資料毀損
2.GPIO不要做熱插拔的動作，更不能短路3V3接腳，否則易造成損壞(Raspberry Pi 3 Model B+只要GND或5V去接觸3V3接腳，直接掛點!)
```
# Raspberry Pi 4 Model B已知操作
## 把USB儲存裝置當主硬碟開機(注意：這裡的操作只對Raspberry Pi OS有效而已，NOOBS跟其他OS可能無效)
```
網址提供:

https://www.raspberrypi.org/documentation/hardware/raspberrypi/bcm2711_bootloader_config.md#usbmassstorageboot

https://www.youtube.com/watch?v=2zrwjGcyM5s
```
```
說明:
在這兩個資訊中，我推薦先看第二個網址(影片中的Firmware Update)然後再看第一個網址(USB-MSD firmware setup instructions的部份)，下面會配合影片的部份說明

1.在打開"bootloader"資料夾後，要選擇"stable"資料夾而不是影片的"beta"資料夾，因為該影片發布時還沒有穩定版可用

2.輸入"vcgencmd bootloader_version"後，他指定的第一行是要確認eeprom中的最後套件升級時間，而要支援USB開機就是要手動更新eeprom套件(如果日期是2020-6月多可以從6-1開始試)

3-1.而他接下來做的事情，其實中間省略的一個步驟，這個在他的說明欄最後兩段話有說明，我個人也是遵循他的方法(詳見4-3)，如果想按照官方作法，請看3-2，否則跳過
3-2.使用"su"切換為root模式時，輸入"vi /etc/default/rpi-eeprom-update"並將"critical"改為"stable"，這個在第一個網址裡"Update the bootloder"裡的第二行"As root, edit"那一部分

4-1.輸入"sudo rpi-eeprom-update -d -f "後，把stable點開來後找"pieeprom"開頭後面日期比較新的，並把該檔案的路徑打上去，不懂可以看4-2範例修改
4-2.ex:"sudo rpi-eeprom-update -d -f /lib/firmware/raspberrypi/bootloader/stable/pieeprom-2020-07-16.bin"
4-3.在3-1提到會做不更動的動作是因為做"sudo rpi-eeprom-update -d -f "的"-d -f"強制動作時就會忽略rpi-eeprom-update的範圍設置，若選擇為"stable"未來的可能會接收到"stable"版的更新套件
而不是原始的"critical"版套件，相對選"critical"若更新eeprom套件時可能會有刷回去一開始無法使用USB開機的風險(不過就情況來看是很小的，通常偵測到更新的固件日期是不會有用舊換掉新的情況)，
穩定程度"critical">"stable">"beta"(關鍵>穩定>測試)

5-1.完成之後照影片方式重新啟動
5-2.再次輸入"vcgencmd bootloader_version"查看是否和"pieeprom"後寫的日期一致

6-1.在影片的15:12中，插入日後要當主硬碟USB裝置後，並注意SD Card Copier的Copy from跟Copy to(from是指來源，to是指定到)，一旦反了可能就變成SD卡的資料消失了
6-2.假如SD卡或USB裝置資料真的搞消失了日後也不需要在做4-1跟4-2的步驟，3-2若一開始有去改的話再去改一下就可以了

7.copy完成後先關機並切斷電源，然後把SD卡抽走後在通電開機，若能成功進入彩屏畫面就表示成功了
```
