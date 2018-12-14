# ErgoDash Build Guide
**読まなくてもいいけどPro Micro取付け時だけは注意!!!!!!**

## 概要
<img width="700" alt="assembly" src="https://github.com/omkbd/picture/blob/master/assembly.png">  

## 0 準備
組みたいレイアウトによってPCBを切断します。  
<img width="700" alt="PCBcut" src="https://github.com/omkbd/picture/blob/master/PCB_cut.jpg">  
手で力をかければ割れます。  

**以降の番号の3～6と10は基本的に基板の裏側に取り付けます。**  

## 1 ダイオードの取付け
ダイオードの黒いほうが四角いフットプリントに合うように配置します。  
<img width="400" alt="diode" src="https://github.com/omkbd/picture/blob/master/Build_Diode.jpg">  
ダイオードと抵抗の位置を間違えないように注意してください。  
<img width="700" alt="diode" src="https://github.com/omkbd/picture/blob/master/diode_complete.jpg">  

## 2 Backlight LED用パーツの取付け[Option]
MOSFETを取り付けます。
シルクで四角で囲ってある箇所に1kΩの抵抗を取り付けます。  
<img width="400" alt="1k" src="https://github.com/omkbd/picture/blob/master/1k_FET.jpg">  

470Ω抵抗を取り付けます。  
<img width="700" alt="470" src="https://github.com/omkbd/picture/blob/master/Resistor.jpg">  
※一部表面実装の抵抗をつけています。  
**※Pro Microの裏に取り付ける抵抗は表面側に取り付けるか表面実装の抵抗を推奨。(Pro Microの種類によってはPro Microと干渉します。)  **  

## 3 TRRSジャックの取付け  
シルクに沿って取り付けます。  

## 4 リセットスイッチの取付け  
Pro Microをつけるのと逆側に取り付けます。  

## 5 Undergrow LEDの取付け[Option]
左右どちらをマスターにするか（USBを指すほう）を決めて、はんだでジャンパします。  
左側がマスターの場合は以下のようになります。  
<img width="700" alt="jump" src="https://github.com/omkbd/picture/blob/master/Jump.jpg">  
LEDチップを取り付けます。  
マスター側は以下のように切れ込みがシルクに合うように取り付けます。スレーブ側（逆側）は逆向きに取り付けます。  
テープ等で固定してはんだ付けをするとやりやすいです。  
<img width="400" alt="RGB_Left" src="https://github.com/omkbd/picture/blob/master/RGB_Left.jpg">  
<img width="700" alt="RGB_Left_Finish" src="https://github.com/omkbd/picture/blob/master/RGB_Left_Finish.jpg">  

## 6 Pro Micro用ピンヘッダの取付け
白い四角い枠がついているほうにピンヘッダを取り付けます。  
**この時点でPro Microを取り付けてはいけません。**  
スプリングピンヘッダを使う場合は基板側のはんだ付けは不要です。  
<img width="700" alt="pin" src="https://github.com/omkbd/picture/blob/master/pin.jpg">  

## 7 スタビライザーの取付け[Option]

2uのキーキャップを使用する場合には必要に応じてアクリルプレートとキースイッチを取り付ける前にスタビライザーを取り付けます。

## 8 キースイッチの取付け
スイッチを取り付ける前に部品の取付けやはんだ付けができているか確認します。  
アクリルプレートにキースイッチをはめて取り付けします。
<img width="700" alt="switch" src="https://github.com/omkbd/picture/blob/master/switch.jpg">  
<img width="700" alt="switch_complete" src="https://github.com/omkbd/picture/blob/master/switch_complete.jpg">  

## 9 Backlight LEDの取付け[Option]
スイッチの上からLEDを取り付けます。  
丸い穴がアノード（＋）で四角い穴がカソード（-）です。  

## 10 Pro Microの取付け
**作業前にPro MicroをUSBでPCと繋げて動作を確認しておきましょう。**  
取り付ける前にはんだ忘れがないか確認します。  
Pro Microと基板のTX0が合うか確認して取り付けます。  
両手とも裏側に取り付けられるようになります。  
スプリングヘッダを使う場合はPro Micro側ははんだ付けします。
取り付けたときにPro Microの浮きがないか確認し、浮きがあればPro Micro下のスイッチの足を少しカットします。

## 11 ケースの組み立て
5mmのねじと6mmのスペーサーを取り付けます。  
<img width="700" alt="spacer" src="https://github.com/omkbd/picture/blob/master/spacer.jpg">  
5mmのねじと8mmのねじを取り付けます。  
<img width="700" alt="case" src="https://github.com/omkbd/picture/blob/master/case.jpg">  
ゴム足を取り付けます。  
<img width="700" alt="gom" src="https://github.com/omkbd/picture/blob/master/gom.jpg">  

## 12 Firmwareの書き込み
以下を参考にやってください。  
https://docs.qmk.fm/#/getting_started_build_tools  
ErgoDashのFirmwareは以下にあります。  
https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodash

キーキャップをつけて完成!!!!!  
<img width="700" alt="finish" src="https://github.com/omkbd/picture/blob/master/finish.jpg">  
