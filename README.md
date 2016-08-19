zaifapi
======================
zaifが公開しているAPIを簡単に呼べる用にしました。
ご利用は自己責任でご自由にどうぞ

使い方
------
１．pipコマンドを実行し、モジュールをダウンロードしてください

    pip install zaifapi

２．クラスをインポートし、下記例の用に使用してください

    from zaifapi.impl import ZaifPublicApi, ZaifPrivateApi
    zaif = ZaifPublicApi()
    print(zaif.last_price('btc_jpy'))
    
    zaif = ZaifPrivateApi(key, secret)
    print(zaif.get_info())


機能紹介
------
### ZaifPublicApi
#### Zaifが公開している認証情報が要らないAPIを実行するクラスです
***
last_price(currency_pair):
ticker(currency_pair):
trades(currency_pair):
depth(currency_pair):
streaming(currency_pair):

| 名前 | 必須 | 説明 | デフォルト値 | 
|:-----------|:------------:|:-----------|:-----------| 
| currency_pair | ◯ | 取得する通貨ペア | - | 
戻り値：json
currency_pairはbtc_jpy、xem_jpy、mona_jpy、mona_btcが指定可能です

last_price : 終値
ticker : ティッカー
trades : 全ての取引履歴
depth : 板情報
streaming : websocketを利用したリアルタイム板情報と終値

[参考](https://corp.zaif.jp/api-docs/)
***

### ZaifPrivateApi
#### Zaifが公開している認証情報が必要なAPIを実行するクラスです
***
インスタンス生成時に、zaifで発行出来るkeyとsecretの文字列を指定してください。
その際、権限にご注意ください。

実行出来るメソッド名やパラメータは下記参考ページそのままなので、そこをご覧ください。
[参考](https://corp.zaif.jp/api-docs/trade-api/)
ただし、fromパラメータはfrom_numと指定してください。

戻り値はすべてjsonとなっています。
***
  
関連情報
--------
1. [ググレカス(ブログ)](http://gugurekasu.blogspot.jp/)
2. [LinkedIn](https://jp.linkedin.com/in/akirataniguchi1)
 
ライセンス
----------
Distributed under the [MIT License][mit].
[MIT]: http://www.opensource.org/licenses/mit-license.php
