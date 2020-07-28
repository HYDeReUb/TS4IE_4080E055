# Raspberry Pi 已知說明
## 降電壓
![image](https://github.com/HYDeReUb/TS4IE_4080E055/blob/master/Picture%20Saved/under_volt.png)
```
這代表著電力提供不足(低於4.63V (+/-5%))，會調降CPU時鐘性能，需要更換符合指定的線材跟電源，若不需要太麻煩可以直接買他們的電源直接來用即可
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
![image](https://github.com/HYDeReUb/TS4IE_4080E055/blob/master/Picture%20Saved/maxresdefault.jpg)
```
用風扇把熱氣帶走，需要時可以加散熱片一起使用
```
```
好處:可以維持一定溫度不再上升
適合:長時間運算操作、超頻玩家
```
## 被動式散熱
![image](https://i.ytimg.com/vi/VJC6OpGpq0Y/maxresdefault.jpg)
```
純粹利用散熱片把熱導出來並慢慢消去而無使用風扇
```
```
好處:由於不需風扇，降低了耗電並增加了安靜感
適合:短時間運算操作、長時間待機
```
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
1.建議在執行格式化或移動檔案這樣的操作時，別執行其他程式來多工操作，避免使用量過高強關或重起
2.GPIO不要做熱插拔的動作，更不能短路3V3接腳，否則易造成損壞
```
未完成
