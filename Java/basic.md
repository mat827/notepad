# if文による条件式

// if文による条件分岐
```
public class Main {
  public static void main(String[] args) {
      if(条件式){
         //条件式が成立した時の処理
      }
  }
}
```
例）
```
public class Main {
  public static void main(String[] args) {
    int number = 1;
    if (number == 1) {
      System.out.println("スキ！");    // 条件式が成立したときの処理
    } else {
      System.out.println("キライ");    // 条件式が成立しなかったときの処理
    }
  }
}
```
// if文による条件分岐　else if
```
public class Main {
    public static void main(String[] args) {
        int number = 1;
        if (条件式1) {
            // 条件式1が成立したときの処理
        } else if (条件式2) {
            // 条件式2が成立したときの処理
        } else {
            // 条件式がどれも成立しなかったときの処理
        }
    }
}
```

例）
// if文による条件分岐　else if
```
public class Main {
  public static void main(String[] args) {
    int number = 2;
    if (number == 1) {
      System.out.println("スキ！");    // 条件式が成立したときの処理
    }else if (number==2){
        System.out.println("どちらでもない");//  条件式２が成立した時の処理
    } else {
      System.out.println("キライ");    // 条件式が成立しなかったときの処理
    }
  }
}
```
# 主なデータの種類
- 数値： 1, 2, 3
- 文字列： "hello","123"
- 論理： true, false





// whileによるループ処理
```
public class Main {
    public static void main(String[] args) {
        // カウンタ変数の初期化
        while (条件式) {
            // 繰り返し処理
            // カウンタ変数の更新
        }
    }
}

```

// forによるループ処理
```
public class Main {
    public static void main(String[] args) {
        for(カウンタ変数の初期化; 条件式; カウンタ変数の更新) {
             // 繰り返し処理
        }
    }
}
```
// forによるループ処理
```
public class Main {
    public static void main(String[] args) {
        for(int i = 0; i<=2; i++) {
             System.out.println("hello wold");
        }
    }
}
```
//拡張for文による配列のループ処理
```
String[] team = {"勇者", "戦士", "魔法使い", "忍者"};
for (String member : team) {
    System.out.println(member);
}
```
