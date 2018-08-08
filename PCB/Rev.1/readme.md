# ErgoDash PCB

このPCBデータはQMK Fimware上のRev.2に対応しています。  

![ErgoDash PCB](https://github.com/omkbd/picture/blob/master/ergodash_pcb3.png)  

### ① pro micro
2か所のうちのどちらか一方に取り付けます。  
シルクが印刷されているほうに取り付けると、コネクタの高さ分ケースを薄くできます。  
### ② MJTP1117 :Reset switch
①で取り付けた位置と逆に取り付けます。  
### ③TRRS jack
シルクに合わせて実装します。
### ④Cherry MX 互換スイッチ  
### ⑤Diode
向きがあるので注意しましょう。  
　　●　　Anode（アノード）  
　　｜  
　　■　　Anode（アノード）SMD用  
　　▽  
　　■　　Cathode（カソード）SMD用  
　　｜  
　　■　　Cathode（カソード）  
### ⑥470Ω resistor（抵抗）  
　　●  
　　｜  
　　■  
　　／  
　　■  
　　｜  
　　●  
### ⑦LED
向きがあるので注意しましょう。  
　　●　　Anode（アノード）  
　　■　　Cathode（カソード）  
### ⑧1kΩ resistor（抵抗）
この一か所のみです。  
　　●  
　　｜  
　　■  
　　／  
　　■  
　　｜  
　　●  
### ⑨NchMOSFET IRLML6344TRPbF
　　■  
　　　　■  
　　■  
### ⑩LED WS2812B
向きがあるので注意しましょう。  
シルクの斜め線はMaster時のものです。Slaveは反対向きに実装します。  
　　■　■  

　　■　■  

### ⑪LED WS2812B用ジャンパ
Master、Slaveによってジャンパする箇所が異なります。  
　　■■■  
　　■■■  
### ⑫RGB LEDテープ用配線取り出しパット
### ⑬I2C用
未検証
### ⑭基板カット位置
レイアウトによりカットします。
### ⑮スペーサ取付穴
