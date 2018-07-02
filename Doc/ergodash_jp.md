# ErgoDashについて

![ErgoDash](https://github.com/omkbd/picture/blob/master/IMG_20180630_1702141.jpg)

## 特徴
・左右分離型  
・Column staggered layout  
・66～70キー（最下段をカスタマイズ可能、最大64パターン?）  
・Cherry MX 互換スイッチ対応  
・Backlight LED対応  
・RGB Underglow対応  
・QMK Firmware 対応  
・格子配列用のキーキャップでだいたいいける?  

## キー配列

![layout](https://github.com/omkbd/picture/blob/master/ergodash-layout.png)  
上の図が可能な配列です。（わかりにくくてすみません。）  
片手で8パターン、両手で64パターンの配列が選択可能です。  
※両手を同じ配列にする必要はありません。

## パーツ

[ErgoDash PCB](https://github.com/omkbd/ErgoDash/tree/master/PCB)
 × 2  
[ErgoDash Case](https://github.com/omkbd/ErgoDash/tree/master/Case)
 × 2  
Cherry MX 互換 スイッチ × 66～70  
Keycap × 66～70 (基本的に1uのみで構成可、配列によって2uに変更)  
1N4148 ダイオード × 66～70 (表面実装は未検証)  
Arduino Pro Micro × 2  
TRRS jack MJ-4PP-9 × 2  
MJTP1117 switch × 2  
TRRS cable × 1 (RGB Underglowを使用する場合4極が必要)  
Micro USB cable × 1  
M2 ねじ × 24(長さはケースにより異なります。)  
M2 スペーサー × 12(長さはケースにより異なります。最短で6mmです。)  

------Option------  
スプリングピンヘッダ12P × 4 ([Helix](https://github.com/MakotoKurauchi/helix)で使用されているものです。)  
---Backlight---  
LED 3mm × 66～70  
470Ω resistor × 66～70 (表面実装は未検証)  
1kΩ resistor × 2 (表面実装は未検証)  
NchMOSFET IRLML6344TRPbF × 2  
---RGB Underglow---  
LED WS2812B × 24  

PCBとケース以外は基本的に国内サイトで入手可能です。  
GB等は未定です。PCBとケースだけでもやるかもしれません。


## ファームウェア

![QMK_logo](https://qmk.fm/qmk_icon_48.png)  
QMK Firmwareで動作します。
[QMK - ErgoDash directory](https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodash)
.  
