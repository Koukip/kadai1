# LED_Device_Driver

2021年度のロボットシステム学の課題1で作成して改良を加えたデバイスドライバです。

# 動作環境

・Raspberry Pi 3 Model B
 
  ・OS:ubuntu 20.04 server
  
# 使用したもの

  ・Raspberry Pi 3 Model B × 1
 
  ・ブレッドボード × 1
  
  ・LED × 3
  
  ・ブザー × 1
  
  ・抵抗220Ω × 4
  
  ・ジャンパー線 (オス-メス) × 8
 
# 回路

・配線画像
  ![image](https://user-images.githubusercontent.com/93635163/146193856-701b8f7e-5bda-4630-a57e-6fdadeaed780.png)
  
 # 使用方法
 
  #### [インストール]
  
  以下のコマンドを実行してください。
  
       $ git clone git@github.com:Koukip/kadai1.git
   
       $ cd myled
   
       $ make
   
       $ sudo insmod myled.ko
   
       $ sudo chmod 666 /dev/myled0
   
 #### [アンインストール」
  
  以下のコマンドを実行して下さい。
  
   $ sudo rmmod myled
   
   $ make clean
   
 #### [実行]
  
 ##### LED(黄色)を点灯させる
  
  $ echo 1 > /dev/myled0
  
#####  LED(青)を点灯させる
  
  $ echo 2 > /dev/myled0
  
#####  LED(赤)を点灯させる
  
  $ echo 3 > /dev/myled0
  
#####  ブザーを鳴らす
  
  $ echo 4 > dev/myled0
  
#####  すべてのLEDを同時に点滅させる
  
  $ echo 5 > dev/myled0
  
#####  すべてのLEDをばらばらに点滅させる
  
  $ echo 6 > dev/myled0
  
#####  警告を鳴らす
  
  $ echo 7 > dev/myled0
  
#####  すべての動作をやめさせる
  
  $ echo 0 > dev/myled0
  
 # デモ動画
 
 
 # ライセンス
 

