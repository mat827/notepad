# PHPで半角数字で直して、数字であるかチェックするプログラム


```
<?php
  $age= ２０;  //全角数字

  $age= mb_convert_kana($age, 'n', 'UTF-8');　　//①
  if(is_numeric($age)){　　　　//②
    print($age . '歳');
  }else{
    print('＊年齢が数字ではありません');
  }
  ?>
```


①`mb_convert_kana`(様々なカナ文字を変換するfunction)で、もし$ageが全角数字であれば半角数字に変換されて$ageに再代入される

＊今回はkana文字に変換したが他にもいろんな文字に設定ができる

②`is_numeric`(functionの種類)はパラメーターが数字かどうかを判断してくれるfunction



## 正規表現で様々な書式を設定するプログラム

メールアドレスや郵便番号、電話番号などを書式を設定したい場合に使うプログラム。今回は郵便番号を正規化して書式を設定していく

例）郵便番号
```
<?php
  $zip ='765-６７８９';

  $zip = mb_convert_kana($zip, 'a', 'UTF-8');  //①
  if(preg_match("/\A\d{3}[-]\d{4}\z/",$zip)){　//②
    print('郵便番号：〒' . $zip);
  }else{
    print('＊郵便番号は123-4567の形式でご記入ください');
  }
?>
```

①`mb_convert_kana`で数字を半角数字な直している

②`preg_match`でパラメーターの中の書式が正規表現でマッチしているかを見ている。
```
("/\A\d{3}[-]\d{4}\z/",$zip)     //パラメーター（書式）

d・・・decimal(数字)を意味している
A・・・文章の頭である事
z・・・文章の終わりである事
[-]・・・ハイフンで結ぶ

*今回の設定
文章の先頭から数字が3回続く事、ハイフンで結び数字が4回続き、文章が終わる
```










