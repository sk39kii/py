# Python関連書き捨てコード集

あれこれ貯めていきますバイ

## isBinary.py バイナリ判定

簡易バイナリ判定を行います。  

<!-- more -->

### 使い方

```python
python isBinary.py [TargetFile]
```

### 内容
MIMEタイプを取得して判断します。
* imageやofficeの場合はTrue(=Binary)。   
* textやcsv(application/vnd.ms-excel)の場合はFalse(=Not Binary)  

MIMEが取得できない場合(L21〜L37)は以下で判定してます。
(使うシーンに合わせて変えてください)  
* ファイルの中身でエンコードが取得しエンコードが不明の場合はBinary
* ファイルの中身にASCIIコードの00H-08Hの文字があればBinary

※エンコードのconfidence（信頼性）の値はとくに見てません
