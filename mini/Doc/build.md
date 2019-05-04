# ErgoDash mini Build Guide

**基本的にErgoDashと同じなので、省略して書いています。**  
必要に応じて以下のページを参照してください。  
https://github.com/omkbd/ErgoDash/blob/master/Doc/build.md

<img width="600" alt="PCB" src="https://github.com/omkbd/picture/blob/master/miniPCB.png">  

## 0 準備
組みたいレイアウトによってPCBを切断します。  
手で力をかければ割れます。  

**以降の番号の3～6と10は基本的に基板の裏側に取り付けます。**  

## 1 ダイオードの取付け
ダイオードの黒いほうが四角いフットプリントに合うように配置します。  
ダイオードと抵抗の位置を間違えないように注意してください。  

## 2 Backlight LED用パーツの取付け[Option]
MOSFETを取り付けます。
シルクでBL1kと書かれている四角で囲ってある箇所に1kΩの抵抗を取り付けます。  
470Ω抵抗を取り付けます。  
※Pro Microの裏に取り付ける抵抗は表面側に取り付けるか表面実装を推奨。(Pro Microの種類によってはPro Microと干渉します。)  

## 3 TRRSジャックの取付け  
シルクに沿って取り付けます。  

## 4 リセットスイッチの取付け  
Pro Microをつけるのと逆側に取り付けます。  

## 5 Undergrow LEDの取付け[Option]
左右どちらをマスターにするか（USBを指すほう）を決めて、はんだでジャンパします。  
左側がマスターの場合は以下のようになります。  
LEDチップを取り付けます。  
マスター側は以下のように切れ込みがシルクに合うように取り付けます。  
**スレーブ側（逆側）は逆向きに取り付けます。**  
テープ等で固定してはんだ付けをするとやりやすいです。  

**最新のファームウェアでは以下のようにします。（2019/5/4時点では未実装）**  
マスターを決める必要はありません。  
以下のようにジャンパします。  
<img width="700" alt="jump" src="https://github.com/omkbd/picture/blob/master/Jump2.jpg">  
マスタースレーブに関わらず、シルクに従ってLEDチップを取り付けます。  


## 6 Pro Micro用ピンヘッダの取付け
白い四角い枠がついているほうにピンヘッダを取り付けます。  
**この時点でPro Microを取り付けてはいけません。**  
※スプリングピンヘッダを使う場合は基板側のはんだ付けは不要です。  （この工程でははんだ付けしません。）  

## 7 スタビライザーの取付け[option]
2Uのキーキャップを使用する場合はスイッチを取り付ける前にスタビライザーを取り付けます。(必ずしもつける必要はありません。)  
**スイッチを付けるとスタビライザーは取り付けられなくなります。**  
以下のように組み立てて取り付けます。  
<img width="400" alt="assembly" src="https://github.com/omkbd/picture/blob/master/Stabilizer.png">  
スタビライザーの音が気になる場合はグリスを塗布します。（キットには付属していません。）  

## 8 キースイッチの取付け
**スイッチを取り付ける前に部品の取付けやはんだ付けができているか確認します。**  
（TRRSジャックとリセットスイッチは特に注意が必要です。）  
アクリルプレートにキースイッチをはめて取り付けします。  
**スタビライザーをつけている場合はスイッチと基板が浮きやすいので注意しましょう。**  

※スプリングピンヘッダを使用する場合は10と12の工程を先に行い、動作確認をすると失敗する可能性が減ります。

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

※スプリングヘッダを使う場合はPro Micro側のみをはんだ付けします。  
スプリングピンヘッダの使い方は下記ページをご参照ください。  
https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_jp.md#pro-micro  

## 11 ケースの組み立て
表面に5mmのねじと6mmのスペーサーを取り付けます。  
裏面に5mmのねじと8mmのねじを取り付けます。  
ゴム足を取り付けます。  

## 12 Firmwareの書き込み
以下を参考に書き込んでください。または、QMKで検索すると書き込み方がすぐに出てくるはずです。  
https://docs.qmk.fm/#/getting_started_build_tools  
ErgoDashのFirmwareは以下にあります。  
https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodash

右手側をマスターにした場合はqmkのconfig.hファイルで
`MASTER_RIGHT`を指定してファームウェアをビルドする必要があります。
https://docs.qmk.fm/#/config_options?id=defines-for-handedness

BacklightとUnderglowを点けるにはキーマップ内のrules.mkに以下を追記します。  
`BACKLIGHT_ENABLE = yes`  
`RGBLIGHT_ENABLE = yes  `

**5の工程でマスターを決めて取り付けた場合はrev1/config.h内の以下の行をコメントアウトしてください。（2019/5/4時点では未実装）**  
`#define RGBLIGHT_SPLIT`  
`#define RGBLED_SPLIT { 12, 12 } `

初めての方は以下のツールを使うことをお勧めします。（これらを使用する場合LED系は点灯しません。）  
https://config.qmk.fm/#/ergodash/rev2/LAYOUT  
https://github.com/qmk/qmk_toolbox

キーキャップをつけて完成!!!!!  
