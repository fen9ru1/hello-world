1.見出し
# 見出しh1
## 見出しh2
### 見出しh3
***
2.コードの挿入


```
function hello(){
　return "hello world!";
}
```
***
3.リンクの挿入、画像の埋め込み

リンクの挿入は、
[リンクテキスト](URL)と書きます。
[Qiita](http://qiita.com/)




画像の挿入は、![代替テキスト](画像URL)と書きます。

![Qiita](http://cdn.qiita.com/assets/siteid-reverse-6044901aace6435306ebd1fac6b7858c.png)
のように書くと




4.引用

>引用文です
>>ネストです


5.文字の修飾(イタリック、太字)

_イタリック_

*イタリック*

__太字__
**太字**

6.リスト
順序なしリスト
文頭に「*」「+」「-」のいずれかを入れる。

+ 順序なしリスト
- 順序なしリスト
順序つきリスト
文頭に「数字.」を入れる。
見た目はほぼ変わりません。

リスト1
リスト2
7. 水平線
「*」か「-」を3つ以上一行に書く。
以下は全て水平線となる。

***
* * *
---
- - -

全部以下の水平線

8. テーブル
以下のようにテーブルを組みます。
基本は「|」でくくっていくことです。
2行目がポイントで、2行目のコロンの位置によってセル内の文字の配置が変わります。

|左揃え|中央揃え|右揃え|
|:---|:---:|--:|
|align-left|align-center|align-right|
|セルの左揃えです|セルの中央揃えです|セルの右揃えです|

左揃え	中央揃え	右揃え
align-left	align-center	align-right
セルの左揃えです	セルの中央揃えです	セルの右揃えです
9. マークダウンのエスケープ
「\」をMarkdownの前につけることでMarkdownを無効化出来ます。
この記事ではこれを多用しました。

\#見出しh1
とすると
#見出しh1
となります。

10. 補足:ページをMarkdownで見る
Qiitaを見ていると「これはどんな記法で書いてあるんだろう」ときになることがあるかもしれません。
そんな時はMarkdown記法で見たいURLの最後に.mdをつければ見ることが出来ます。

* 多言語化要件の整理
    pfのどの機能に対して、多言語化する必要があるかを洗い出す
    e.g.アラート通知機能
    e.g. 多言語化は製品ごとで考える？
            FPS対応言語: en, ja
            WAE対応言語: en, zh
* 言語化対応するためのpf構成の設計     
    多言語設定情報の持たせ方の設計     
        //platformなにをもって言語切り替えかを検討 
        //人(通知先の人のmail adr)に結びつく
        //通知アドバイスとsetで設定する？
        //DBスキーマ調整、//gen-dev環境作成済み
        //設定GUI(IM との連携)機能要件の検討       
    テンプレートの多言語化の検討        
* 実装
    lambdaロジックの修正
    route テンプレート修正
* テスト


QRコードの内容は以下５項目です
    卒回	
    氏名
    フリガナ
    支部
    個人番号

img_name="Input_test_shift-jis"
img_dir='/content/'+img_name+'.png'
img_position = "F6"

#Excelファイル名
ExcelName = "EEEE.xlsx"

#  """ 02 Excelファイル作成 """
workbook = openpyxl.Workbook(ExcelName)
workbook.save(ExcelName)


# Excelファイル読込
workbook = openpyxl.load_workbook(ExcelName)
sheet = workbook.active

# 画像を選択 & 挿入
img_to_excel = openpyxl.drawing.image.Image(img_dir)
sheet.add_image(img_to_excel, img_position)

#保存
workbook.save(ExcelName)


5001 MC030235
5001 DA023001

IM UAT feedback対応結果の 再確認

お疲れ様です
この間、山崎さん、岸田さんご協力のもと、
IM UATのfeedbackはできました。ありがとうございます
現在、IM teamはマスタメンテの修正を行ったため、再度確認を実施しようと考えています
前回と同じ形で進めようかと思います

目標
    前回feedbackで指摘して部分について、修正できたかを確認
進め方（前回同様）
　　山崎さん：Local PCからHitz LanにアクセスしてIM画面開き、
　　　　　　　Local PC画面をteams上で共有
  　岸田さん、郭： teams経由で、協同確認、

付きまして、日程調整をさせていただきます
○ or ✗で返事していただきたい

3/28（月)  10:30~12:00
3/28（月） 13:00~14:30　
3/29(火)  15:30 ~17:00