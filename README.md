##line-bot-sdk-python
===================

|Build Status| |PyPI version| |Documentation Status|

SDK of the LINE Messaging API for Python.

##About the LINE Messaging API
----------------------------

See the official API documentation for more information.

English: https://devdocs.line.me/en/

# line-bot-Tutorial

 教你建立自己的 line-bot 使用 python flask 📝

 line-bot-tutorial use python flask


## 首先安裝line官方 line-bot-sdk-python

https://github.com/line/line-bot-sdk-python

直接git clone https://github.com/line/line-bot-sdk-python.git

再來cd進入line-bot-sdk-python 

## install 

::

    $ pip install line-bot-sdk


First install for development.

::

    $ pip install -r requirements.txt

## 教學

請先到 [https://business.line.me/zh-hant/](https://business.line.me/zh-hant/) 這裡登入自己

原本的 line 帳號，然後點選 Messaging API

![alt tag](http://i.imgur.com/KIzExmQ.jpg)

接下來你會看到 **開始使用Messaging API** 以及 **開始使用Developer Trial**

在這裡我們選 **開始使用Messaging API**

![alt tag](http://i.imgur.com/graLPrj.jpg)

這兩個差別在哪裡呢? 可以到同一個頁面的下方觀看，基本上就只是方案不同而已

![alt tag](http://i.imgur.com/bERbTGz.jpg)

接著就是一些設定，點選 選擇公司/經營者

![alt tag](http://i.imgur.com/d1pVdx9.jpg)

點選 新增公司/經營者

![alt tag](http://i.imgur.com/of23y7W.jpg)

填寫一些資料

![alt tag](http://i.imgur.com/7L9nulI.jpg)

line bot 的 大頭貼 以及 名稱 設定

![alt tag](http://i.imgur.com/7483ljT.jpg)

![alt tag](http://i.imgur.com/a4Mf3Rl.jpg)

設定完後，請選擇 申請

![alt tag](http://i.imgur.com/Q6q8zGA.jpg)

以上設定應該不會有什麼問題

請選擇 開始使用 API

![alt tag](http://i.imgur.com/DOEjH0F.jpg)

請選擇 確認

![alt tag](http://i.imgur.com/pKWBvsj.jpg)

這些請注意，  選擇 **允許** ，然後記得 **儲存**

![alt tag](http://i.imgur.com/Ofm9SeJ.jpg)

點選 **Line Developers**

![alt tag](http://i.imgur.com/cW9713h.jpg)

你會進入下面這個畫面，在這個畫面中，有兩個東西很重要，分別是

* Channel Secret

* Channel Access Token

***Channel Secret***

![alt tag](http://i.imgur.com/jpIEMh4.jpg)

***Channel Access Token***

如果你看到的是空的，請點選 **ISSUE** 就會顯示了

![alt tag](http://i.imgur.com/PcCEL4P.jpg)

請將你的 **Channel Secret** 以及 **Channel Access Token**

貼到 [config.ini](https://github.com/twtrubiks/line-bot-tutorial/blob/master/config.ini) 底下 ( 如不了解 .ini 的使用方法，可參考 [configparser_tutorial](https://github.com/twtrubiks/python-notes/tree/master/configparser_tutorial) )

```ini
[line_bot]
Channel_Access_Token = YOUR_CHANNEL_SECRET
Channel_Secret = YOUR_CHANNEL_SECRET
```

佈署

![alt tag](http://i.imgur.com/kseRgxr.jpg)

如上圖，我的網址是 [https://python-ine-bot.herokuapp.com/](https://python-ine-bot.herokuapp.com/)

接著我們要加入 Webhook URL ，請點選 EDIT ，並且加入你自己的網址，網址格式

```python
https://{你的網址}/callback
```

舉例，我的網址就是

```python
https://python-ine-bot.herokuapp.com/callback
```

![alt tag](http://i.imgur.com/5ckn24T.jpg)

![alt tag](http://i.imgur.com/TIjIM9W.jpg)

輸入完之後，可以按 VERIFY ，如果你的 CODE 正確無誤，就會顯示 Success

![alt tag](http://i.imgur.com/Mey5FKF.jpg)

不過我使用 [line-bot-sdk-python](https://github.com/line/line-bot-sdk-python)當我按下 VERIFY，卻出現錯誤，不過是可以正常運作，所以暫時先不管他。

![alt tag](http://i.imgur.com/wb0Qw5W.jpg)

關於上述這個問題，可以到 [issues 2](https://github.com/twtrubiks/line-bot-tutorial/issues/2)
以及 [issues 3](https://github.com/twtrubiks/line-bot-tutorial/issues/3) 觀看說明。( 感謝熱心的網友 )

基本上到這裡就是完成了，趕快去加入自己的 line bot 玩玩看吧~

只要我有新的想法，我會同步更新在這篇文章， line bot 還有很多好玩的地方

## 使用 imgur 官方 api

透過 imgur 官方 api  [imgurpython](https://github.com/Imgur/imgurpython) ,

從自己的相簿隨機回傳一張正妹照片，

請到下方獲取自己的 CLIENT_ID ,  CLIENT_SECRET  , 以及自己相簿的 album_id

![alt tag](http://i.imgur.com/nQNQVD7.jpg)

並將自己的資料輸入在下方程式碼

```python
client_id = 'YOUR_IMGUR_CLIENT_ID'
client_secret = 'YOUR_IMGUR__CLIENT_SECRET'
album_id = 'YOUR_IMGUR_ALBUM_ID'
```

## 執行環境

* Python 2.7

## License

MIT license
