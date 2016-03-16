# Python関連書き捨てコード集

あれこれ貯めていきますバイ

### isBinary.py バイナリ判定

簡易バイナリ判定を行います。  

MIMEタイプを取得して判断します。
* imageやofficeの場合はTrue(=Binary)。   
* textやcsv(application/vnd.ms-excel)の場合はFalse(=Not Binary)  

MIMEが取得できない場合(L21〜L37)は、  
* ファイルの中身でエンコードが取得しエンコードが不明の場合はBinary
* ファイルの中身に00H〜08Hの文字があればBinary

※エンコードのconfidence（信頼性）の値は見てない(今のところ)
