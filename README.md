# Orbit Propagator
### スペースデブリの軌道計算プログラム
---
### **概要**
本プログラムは地球低軌道を周回する物体の軌道を計算するシミュレータ。
採用する地球環境モデルは必要に応じて切り替え可能。

### **使用方法**
https://github.com/Keisuke-ekusieK/Orbit_Propagator/issues/1#issue-768777996

1. Makefileで採用する地球環境モデル・計算の精度・出力するパラメータと形式を指定する。
2. makeコマンドにてコンパイルを行い、作成される実行ファイルを実行する。

### **注意点**
GitHubにアップロードしているプログラムファイルは計算の主要部分のみで、計算に必要となる地球環境のデータがないため計算の実行はできません。
地球環境のデータ(地球の磁場環境データ・大気密度の実測データ・月や太陽の位置データ)などは容量が大きすぎるためです。

### **地球環境モデル**
  計算方法自体を切り替える必要のあるものについてはモデルの切り替えをMakefileで指定する。
  大気密度モデル：Exponentialモデル、Jacchia-Robertsモデル、NLRMSISE00モデル
  地球の影のモデル：円筒モデル、Conicalモデル
  地球磁場モデル：ダイポール磁場モデル、傾斜ダイポール磁場モデル、IGRFモデル
  共回転電場モデル：考慮に入れるか否か
  対流電場モデル：考慮に入れるか否か

計算方法自体は変更なく、計算の精度を切り替える項目については入力ファイルにて指定する。
  地球重力ポテンシャルの展開係数

### **参考文献**
計算方法、および、地球周辺環境のモデルの詳細は下記論文参照。
Akari, Keisuke, Kento Hoshi, and Hiroshi Yamakawa. "Lorentz Force Effects on Orbit and Lifetime of Micrometer-Size Space Debris." Journal of Spacecraft and Rockets 56.4 (2019): 1248-1258.
