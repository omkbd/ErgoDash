# ErgoDash miniについて

![ErgoDash mini](https://github.com/omkbd/picture/blob/master/Ergodashmini.jpg)

## 特徴
・左右分離型  
・Column staggered layout  
・52～56キー（最下段をカスタマイズ可能、最大100パターン）  
・Cherry MX 互換スイッチ対応  
・Backlight LED対応  
・RGB Underglow対応  
・QMK Firmware 対応  

## キー配列

![layout](https://github.com/omkbd/picture/blob/master/ergodashmini-layout.png)  
上の図が可能な配列です。（わかりにくくてすみません。）  
片手で10パターン、両手で100パターンの配列が選択可能です。  
※両手を同じ配列にする必要はありません。

## パーツ

[ErgoDash mini PCB](https://github.com/omkbd/ErgoDash/tree/master/mini/PCB)
 × 2  
[ErgoDash mini Case](https://github.com/omkbd/ErgoDash/tree/master/mini/Case)
 × 2  
Cherry MX 互換 スイッチ × 56  
Keycap × 56 (基本的に1uのみで構成可、配列によって2uに変更)  
1N4148 ダイオード × 56  
Pro Micro × 2  
TRRS jack MJ-4PP-9 × 2  
MJTP1117 switch × 2  
TRRS cable × 1 (RGB Underglowを使用する場合4極が必要)  
Micro USB cable × 1  
M2×5mm ねじ × 22  
M2×8mm ねじ × 6  
M2×6mm スペーサー × 14  
ゴム足 × 8  

------Option------  
スプリングピンヘッダ12P × 4 ([Helix](https://github.com/MakotoKurauchi/helix)で使用されているものです。)  
---Backlight---  
LED 3mm × 56  
470Ω resistor × 56  
1kΩ resistor × 2  
NchMOSFET IRLML6344TRPbF × 2  
---RGB Underglow---  
LED WS2812B × 20  
又は  
LEDテープ × 2

PCBとケース以外は基本的に国内サイトで入手可能です。  
[ここ](https://dashkbd.booth.pm/items/1011978)
で基本セットを販売しています。(準備中)

## ファームウェア

QMK Firmwareで動作します。
[QMK - ErgoDash mini directory](https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodash/mini)
.  

## 組み立て方

[ここ](https://github.com/omkbd/ErgoDash/blob/master/mini/Doc/build.md)
を見てください。
