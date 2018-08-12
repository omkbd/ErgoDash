# ErgoDash Build Guide
**読まなくてもいいけどPromicro取付け時だけは注意しましょう。**
## 0 準備
組みたいレイアウトによってPCBを切断します。  
<img width="700" alt="PCBcut" src="https://github.com/omkbd/picture/blob/master/PCB_cut.jpg">  
手で力をかければ割れます。  

## 1 ダイオードの取付け
ダイオードの黒いほうが四角いフットプリントに合うように配置します。  
<img width="400" alt="diode" src="https://github.com/omkbd/picture/blob/master/Build_Diode.jpg">  
ダイオードと抵抗の位置を間違えないように注意してください。  
<img width="600" alt="diode" src="https://github.com/omkbd/picture/blob/master/diode_complete.jpg">  

## 2 Backlight LED用パーツの取付け[Option]
MOSFETを取り付けます。
四角で囲ってある箇所に1kΩの抵抗を取り付けます。  
<img width="400" alt="1k" src="https://github.com/omkbd/picture/blob/master/1k_FET.jpg">  

470Ω抵抗を取り付けます。  
<img width="400" alt="1k" src="https://github.com/omkbd/picture/blob/master/Resistor.jpg">  
※一部表面実装の抵抗をつけています。  

## 3 TRRSジャックの取付け
裏側に取り付けます。  
シルクに沿って取り付けます。  

## 4 リセットスイッチの取付け
裏側に取り付けます。  
promicroをつけるのと逆側に取り付けます。  

## 5 Undergrow LEDの取付け[Option]
左右どちらをマスターにするか（USBを指すほう）を決めて、はんだでジャンパします。  
左側がマスターの場合は以下のようになります。  
<img width="600" alt="1k" src="https://github.com/omkbd/picture/blob/master/Jump.jpg">  
LEDチップを取り付けます。  
マスター側は以下のように切れ込みがシルクに合うように取り付けます。スレーブ側（逆側）は逆向きに取り付けます。  
<img width="600" alt="1k" src="https://github.com/omkbd/picture/blob/master/RGB_Left.jpg">  
<img width="600" alt="1k" src="https://github.com/omkbd/picture/blob/master/RGB_Left_Finish.jpg">  

## 6 promicro用ピンヘッダの取付け
四角い枠がついているほうにピンヘッダを取り付けます。  
**この時点でPromicroを取り付けてはいけません。**  
スプリングピンヘッダを使う場合はこの工程を省けます。  

## 7 キースイッチの取付け
アクリルプレートにキースイッチをはめて取り付けします。  

## 8 Backlight LEDの取付け[Option]
スイッチの上からLEDを取り付けます。  

## 9 promicroの取付け
取り付けるまにはんだ漏れがないか確認します。

## 10 ケースの組み立て


## 11 Firmwareの書き込み
ggりましょう。


<img width="400" alt="finish" src="https://github.com/omkbd/picture/blob/master/finish.jpg">  
