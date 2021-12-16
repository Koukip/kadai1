# LED_Device_Driver

2021年度のロボットシステム学の課題1で作成して改良を加えたデバイスドライバです。

実行することによってLEDにいろいろな光り方をさせたりブザーを鳴らしたりすることができます。

## 動作環境

・Raspberry Pi 3 Model B
 
  ・OS:ubuntu 20.04 server
  
## 使用したもの

  ・Raspberry Pi 3 Model B × 1
 
  ・ブレッドボード × 1
  
  ・LED × 3
  
  ・ブザー × 1
  
  ・抵抗220Ω × 4
  
  ・ジャンパー線 (オス-メス) × 8
 
## 回路

・回路図

<img width="430" alt="image" src="https://user-images.githubusercontent.com/93635163/146329865-40e55445-5514-4200-91a0-0d1b4636df6e.png">　　　fritzingで作成しました。


・配線画像
  ![image](https://user-images.githubusercontent.com/93635163/146193856-701b8f7e-5bda-4630-a57e-6fdadeaed780.png)
  
 ## 使用方法
 
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
  
      $ echo 1 > /dev/myled0;
  
#####  LED(青)を点灯させる
  
      $ echo 2 > /dev/myled0;
  
#####  LED(赤)を点灯させる
  
      $ echo 3 > /dev/myled0;
  
#####  ブザーを鳴らす
  
      $ echo 4 > dev/myled0;
  
#####  すべてのLEDを同時に点滅させる
  
       $ echo 5 > dev/myled0;
  
#####  すべてのLEDをばらばらに点滅させる
  
       $ echo 6 > dev/myled0;
  
#####  警告を鳴らす
  
      $ echo 7 > dev/myled0;
  
#####  すべての動作をやめさせる
  
       $ echo 0 > dev/myled0;
  
 ## デモ動画
 
 https://youtu.be/OYKB-o0yEW
 
 
 ## コントリビューション
 
 itukiuenoさんにdelayの意味と使い方を教わりました。
 
 そのdelayを使って少し工夫をした使い方をして様々な所に活用しました。
 
 工夫した点
 
 ・赤色のLEDを持っていたので赤色のLEDの点滅とブザーを同時に鳴らすことでサイレンのようなものを作ってみた。
 
・     $ delay(5 * 1000 * 1000);　の5の部分を変更することで点滅のスピードを変えることができるので一つ一つのLEDをばらばらに光らせ、イルミネーションを再現してみた。
 

 ## ライセンス
 
 GNU General Public License v3.0
 
 https://github.com/Koukip/kadai1/blob/ce6aaf1d59c2121a03dd7edbf3b952bee4f549ae/COPYING
 
 
 
 
 

