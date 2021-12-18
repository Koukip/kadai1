## Robot Systems Studies Issue 1

授業で作成したデバイスドライバに簡単な改良を加えました。

## Demo video

## circuit

#### circuit diagram

<img width="537" alt="image" src="https://user-images.githubusercontent.com/93635163/146634878-c7e725a5-cbb8-4ada-a18c-b00f0ee15705.png">


#### Pin information

<img width="445" alt="image" src="https://user-images.githubusercontent.com/93635163/146634724-6ab11f8a-d45d-4fd2-a36d-2ab32e63be78.png">




## How to use

1.  $ git clone git@github.com:Koukip/kadai1.git

2.  $ cd myled

3.  $ make

4.  $ sudo insmod myled.ko

5.  $ sudo chmod 666 /dev/myled0　　を順番に入力していく。

#### Operation check

1.  $ echo 1 > /dev/myled0    →　LED(黄色)が点灯する。
2.  $ echo 2 > /dev/myled0    →　LED(青色)が点灯する。
3.  $ echo 3 > /dev/myled0    →　LED(赤色)が点灯する。
4.  $ echo 4 > /dev/myled0    →　すべてのLEDが点灯する。
5.  $ echo 0 > /dev/myled0    →　すべてのLEDを消灯する。


#### License

GNU General Public License v3.0




 
 
 
 
 

