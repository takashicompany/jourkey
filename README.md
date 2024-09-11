# Jourkey

## 入手する前に当ビルドガイドをご一読ください。

入手する前・組み立てる前にこのビルドガイドの全てを一読ください。  
頭の中で実際の作業工程をイメージして読み進めると、実際の作業の際に滞ることが少なくなります。  
不明点などがありましたら、XやBoothのメッセージ等にてお気軽にご質問ください。  

## 組み立てに必要な部品

キットに含まれていないものはご自身でご用意ください。  

以下は必須の項目の説明です。
|記号|説明|
|:--|:--|
|◯|無いと動作しません。キットに含まれていないものはご自身でご用意ください。|
|△|無くても動作させられますが、用意すると組み立てさやメンテナンス性が向上します。初心者の方はご用意頂くのが確実です。|
|?|使用スタイルに併せて、選択可能です。|

|画像|部品名|個数|必須|備考|
|:--|:--|:--|:--|:--|
||Jourkey PCB|1|◯||
||ケース|1|◯||
||M2ネジ 20mm|5|◯||
||M2ナット|5|◯||
||スイッチソケット(MX用)|13|◯|無くてもPCBに直にハンダ付けできますが、**メンテナンス性や組み立てやすさの観点で取り付けを強く推奨します。** 当ビルドガイドではスイッチソケットを使用した組み立て方のみを紹介しております。||
||[Pro Micro](https://shop.yushakobo.jp/products/21)|1|◯|キーボードの頭脳部分を司る部品です。ピン数は2列12穴です。どれを買っていいか分からない場合は[コンスルー付きのセット](https://shop.yushakobo.jp/products/21)の購入を推奨します。|
|<img src = "https://github.com/takashicompany/rookey/raw/master/images/build/IMG_6635.jpg?raw=true" width = "1200px" />|[タクトスイッチ](https://shop.yushakobo.jp/products/a0800ts-01-1)|1|△|キーボードにファームウェアを書き込む際に利用するスイッチです。取り付けなくともピンセットを用いることでファームウェアを書き込めます。詳細は[こちら](https://github.com/takashicompany/rookey/blob/master/README.md#5-%E3%83%AA%E3%82%BB%E3%83%83%E3%83%88%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)。|
|<img src = "https://github.com/takashicompany/rookey/assets/4215759/131d8bc9-4716-4d8d-8934-5a90197babb9" width = "1200px" />|[コンスルー](https://shop.yushakobo.jp/products/31)|2|◯|回路プレートとPro Microを接続する端子です。Pro Microに付属するピンヘッダでの取り付けも可能ですが、作業ミスや故障した際の取り替えが容易になりますので、**コンスルーの使用を強く推奨します。ピンヘッダでの取り付けは当キーボードと当ビルドガイドではサポートしません。** コンスルーの必要な高さはPro Microによって異なりますので、販売元にご確認ください。コンスルーについての詳細な説明は[こちら](https://scrapbox.io/self-made-kbds-ja/%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC)をご一読ください。併せて[取り付け方の説明](https://yushakobo.zendesk.com/hc/ja/articles/360044233974-%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC-%E3%82%B9%E3%83%97%E3%83%AA%E3%83%B3%E3%82%B0%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80-%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91%E6%96%B9%E3%82%92%E6%95%99%E3%81%88%E3%81%A6%E4%B8%8B%E3%81%95%E3%81%84)も目を通しておくと作業がスムーズに進められます。|
|<img src = "https://github.com/takashicompany/rookey/blob/master/images/build/IMG_6653.jpg?raw=true" width = "1200px" />|[MX互換キースイッチ](https://shop.yushakobo.jp/collections/all-switches)|9|◯|キーの動作部品です。キーの押下を電気信号でPro Microに伝えます。ホットスワップに非対応ですので、一度ハンダ付けすると取り外しの際にはハンダ吸い取り線などを用いる必要があります。|
|<img src = "https://github.com/takashicompany/rookey/assets/4215759/eafcac57-31fe-4c3a-829c-3cbf697e00ff" width = "1200px" />|[MX互換キーキャップ](https://shop.yushakobo.jp/collections/keycaps)|9|◯|指がキーに触れる部品です。ISO Enterキーを用いる場合は他に1Uが9個、1.5uが1個、1.75uが1個が必要です。ISOエンターキーを使わない場合は、代わりに1.5uをさらに1個、1.25uが1個必要になります。|
|<img src = "https://github.com/takashicompany/rookey/raw/master/images/build/IMG_6672.jpg?raw=true" width = "1200px" />|[ウレタンクッション](https://shop.yushakobo.jp/products/a0800ur-01-6)|4|△|底面に貼り付けることでキーを押した時に滑らなくなります。100均ショップなどで購入したものでも代用可能です。|
|<img src = "https://github.com/takashicompany/rookey/raw/master/images/build/IMG_6666.jpg?raw=true" width = "1200px" /> |[ロータリーエンコーダ](https://shop.yushakobo.jp/collections/all-keyboard-parts/Encorder)|1|?|ノブを指で回すことでの入力が可能です。スクロール操作などに適しています。Pro Microの手前側のキースイッチをロータリーエンコーダに変更することが可能です。**不要な方は用意する必要はありません。**|

## 組み立てに必要な道具

何を用意してよいか分からない方は、[こちら](https://shop.yushakobo.jp/products/a9900to)を購入するのが確実です。

|道具|備考|
|:--|:--|
|ハンダごて|おすすめは[HAKKO FX-600](https://www.hakko.com/japan/products/hakko_fx600.html)です。[こて台](https://www.hakko.com/japan/products/hakko_kote_board.html)もあると、より作業をスムーズに進められます。|
|ハンダ|[こちら](https://www.goot.jp/products/detail/se_06008)などを使う方が多いようです。|
|ピンセット|100均などで手に入るものでも充分利用できるかと思います。|
|ニッパー|100均などで手に入るものでも充分利用できるかと思いますが、1000円程度ものを買っても損では無いかと思います。|

## あるとさらに完成度が高くなる道具
|道具|備考|
|:--|:--|
|棒ヤスリ|基板の縁にあるバリを削るのに使います。|
|サインペン|基板の縁を塗るとより美しくなります。|
|マスキングテープ|キースイッチをハンダ付けする際に役立ちます。|

## 組み立て方

### 1. PCBの表裏を確認する

表  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9962.jpg?raw=true" width = "600px" />

裏  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9963.jpg?raw=true" width = "600px" />

### 2. スイッチソケットのハンダ付け

キースイッチを取り付けるためのソケットをハンダ付けします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9964.jpg?raw=true" width = "600px" />

ソケットはPCBの裏面に取り付けます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9965.jpg?raw=true" width = "600px" />

ソケット取付箇所の片側にハンダを溶かして載せます(予備ハンダ)。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9966.jpg?raw=true" width = "600px" />

ピンセットでソケットを持ちながら予備ハンダを溶かしながらソケットをハンダ付けします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9967.jpg?raw=true" width = "600px" />

もう片方の取付箇所もハンダ付けします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9974.jpg?raw=true" width = "600px" />

ISOエンターキーを取り付ける際はPro Micro取付箇所から対角線の位置にはソケットを一つだけつけてください。
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9971.jpg?raw=true" width = "600px" />

ISOエンターキーを取り付けない場合はソケットを2つ取り付けてください。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9969.jpg?raw=true" width = "600px" />

全部で12個か13個のソケットを取り付けます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9975.jpg?raw=true" width = "600px" />

### 3. Pro Microの取り付け

Pro Microはキーボードの頭脳部分です。キースイッチの入力をPCなどに伝達します。  
取り付けにはコンスルーを用いることを強く推奨します。  
コンスルーを用いることでメンテナンス性の向上や組み立て時の失敗を減らすことができます。慣れてない方はぜひご利用ください。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9977.jpg?raw=true" width = "600px" />

コンスルーをPro Microに取り付けます。  
取り付けの際は[こちら](https://yushakobo.zendesk.com/hc/ja/articles/360044233974-%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC-%E3%82%B9%E3%83%97%E3%83%AA%E3%83%B3%E3%82%B0%E3%83%94%E3%83%B3%E3%83%98%E3%83%83%E3%83%80-%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91%E6%96%B9%E3%82%92%E6%95%99%E3%81%88%E3%81%A6%E4%B8%8B%E3%81%95%E3%81%84)の説明を併読することをオススメします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9979.jpg?raw=true" width = "600px" />

PCBの裏面にコンスルーを挿します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9982.jpg?raw=true" width = "600px" />

コンスルーにPCBを挿します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9984.jpg?raw=true" width = "600px" />

コンスルーとPro Microをハンダ付けします。**PCBとコンスルーは絶対にハンダ付けしないでください。**  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9986.jpg?raw=true" width = "600px" />

### 4. リセットスイッチの取り付け

リセットスイッチはPro Microにファームウェアを書き込む際に使用します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9988.jpg?raw=true" width = "600px" />

リセットスイッチはPCB裏側の「RESET」と書かれたところに取り付けます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9989.jpg?raw=true" width = "600px" />

リセットスイッチの足をPCBの裏側から挿します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9991.jpg?raw=true" width = "600px" />

PCBの表側からリセットスイッチの足が出ていることを確認します。こちらの足をハンダ付けします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9993.jpg?raw=true" width = "600px" />

### 5. ファームウェアの書き込み

以下は別キーボードでの説明を流用したものです。画像などに差異はありますが手順は同じです。

---

[Remap](https://remap-keys.app/catalog/QSD7jKLB0Ax5J4y8wJ8s/firmware)にてWebブラウザからファームウェアの書き込みを行います。  

ファームウェアを選んで、Flashをクリックします。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/933fc14a-2d65-425c-a00f-eb79a82bd547" width = "600px" />

Bootloderが「Caterina」になっていることを確認してFlashをクリックします。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/20aba117-0d60-4539-b655-5dea8084d733" width = "600px" />

[リセットスイッチを押して](https://github.com/takashicompany/rookey/blob/master/README.md#5-%E3%83%AA%E3%82%BB%E3%83%83%E3%83%88%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%81%AE%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)、Pro Microが選択肢に出てくるかと思いますので、「接続」をクリックするとファームウェアの書き込みが開始されます。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/d6f071fb-7d2b-4449-9b6e-1283e31dd44e" width = "600px" />

以下のような表示になれば、書き込み完了です。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/ce1170f6-8766-49af-a0e7-9ee7ca0c43e6" width = "600px" />

### 6. ロータリーエンコーダの取り付け

Jourkeyの右奥のキー取り付け位置にロータリーエンコーダを取り付けることが可能です。  
必要ない方は読み飛ばして構いません。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9995.jpg?raw=true" width = "600px" />

PCB表面からロータリーエンコーダを取り付けます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9998.jpg?raw=true" width = "600px" />

PCBの裏面からロータリーエンコーダの足が出ていることを確認してハンダ付けします。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_9999.jpg?raw=true" width = "600px" />

### 7. スイッチプレートとキースイッチの取り付け

キースイッチをPCBの取り付けつつスイッチプレートを固定します。  
スイッチプレートに保護シートが付いている場合は両面とも剥がしてください。  
剥がれづらい場合は水を極少量つけると剥がれやすくなることがあります。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0003.jpg?raw=true" width = "600px" />

ISOエンターキーを用いる場合はスタビライザーを用意してPCBに取り付けると、エンターキーが安定します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0009.jpg?raw=true" width = "600px" />

スタビライザーはPCBの表面から取り付けます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0011.jpg?raw=true" width = "600px" />

下図のように取り付けられれば完了です。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0013.jpg?raw=true" width = "600px" />

PCBの表面にスイッチプレートを置きます。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0004.jpg?raw=true" width = "600px" />

キースイッチをお好みで用意します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0007.jpg?raw=true" width = "600px" />

スイッチプレートの穴にキースイッチを挿した後にキースイッチの足をソケットに挿します。下図のようになれば完了です。キースイッチの足が折れないようにソケットの穴に入れることを心がけてください。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0014.jpg?raw=true" width = "600px" />

### 8. キースイッチの動作確認

以下は別キーボードでの説明を流用したものです。画像などに差異はありますが手順は同じです。

---

[Remap](https://remap-keys.app/configure)でキースイッチが正しく動作するかを確認します。  
+Keyboardをクリックします。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/a635e8ac-e815-4261-99cc-3e8d57467dde" width = "600px" />

上述のVIAファームウェアを書き込むと、Rookeyが選択肢に表示されますので選択して接続します。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/7ac86720-3263-4d83-8efb-286ffaef6fa3" width = "600px" />

Rookeyの設定画面が表示されます。右下の三点リーダーをクリックするとメニューが表示されますので、「Test Matrix mode」をクリックします。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/4d9cae0f-64ad-4d40-9e02-4224ae53e4d5" width = "600px" />

「Test Matrixｌでは入力したキーが着彩されますので、全てのキーが動作(着彩)されるかを確認します。  
<img src = "https://github.com/takashicompany/rookey/assets/4215759/1b82239b-2322-4212-b655-943db4f30ca4" width = "600px" />

もし入力されないキーがありましたら、キースイッチのハンダ付けに不備がないか、Pro Microのコンスルーのハンダ付けや差し込みを確認してください。

### 9. トッププレート・サイドプレート・ボトムプレートの取り付け

トッププレート、スイッチプレート、サイドプレート、ボトムプレートをネジとナットで固定します。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0016.jpg?raw=true" width = "600px" />

下図のようになれば完了です。  
<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0017.jpg?raw=true" width = "600px" />

### 10. ゴム足シールの取り付け

底面に滑り止めとしてゴム足シールや[ウレタンクッション](https://shop.yushakobo.jp/products/a0800ur-01-6)などを取り付けます。  
<img src = "https://github.com/takashicompany/rookey/blob/master/images/build/IMG_6672.jpg?raw=true" width = "600px" />

### 11. キーキャップを取り付ける

キーキャップを取り付けて完成です。  

<img src = "https://github.com/takashicompany/jourkey/blob/master/images/build/IMG_0021_2.jpg?raw=true" width = "600px" />

### 12. 完成した後の楽しみ方

完成しましたら、ぜひSNSなどに写真を投稿頂ければと思います。
Twitterのハッシュタグは [`#Jourkey #自作キーボード`](https://twitter.com/search?q=%23%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%20%23Jourkey&src=typed_query) を付けていただけると幸いです。
キットを組み立てた感想や、キーボードを使った所感などをお待ちしております！

また、毎週日曜日の１9時より実施されている[#KEEP_PD](https://twitter.com/hashtag/KEEB_PD?f=live)に投稿頂くこともオススメです。  
開催の告知は[@KEEB_PD](https://twitter.com/KEEB_PD)にて行われております。

ご不明な点などございましたら、[@takashicompany](https://twitter.com/takashicompany)にメンションやDM頂ければ回答できるかと思います。

