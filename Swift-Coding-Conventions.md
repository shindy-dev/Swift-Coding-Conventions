# Swiftコーディング規約

# Swiftコーディング規約について
Swiftにおけるコーディング規約を独自に作成。様々なコーディング規約を参考に随時更新していく。なお、本コーディング規約を利用して問題が発生した場合、我々は一切責任を負わない。


## 命名規則
### 前提
命名規則で代表的に用いられるケースを以下にまとめる

|ケース名|説明 |例   |
|:---|:---|:---|
|キャメルケース |連結する際に単語の始めを大文字にして連結 |strUserName |
|パスカルケース |先頭の単語を含め、単語の始めを大文字にして連結 |StrUserName |
|スネークケース | 単語間をアンダースコア「_」で連結| str_user_name |
|アッパースネークケース |全て大文字で単語間をアンダースコア「_」で連結 |USER_NAME |


### 変数名
- 使用ケース  
  スネークケース（*snake_case*）  

- 補足  
  変数名には可読性を向上させるため、先頭に型名の略称を記述する（略称は下記参照）

    |型名 |略称 |例 |
    |:---|:---|:---|
    |Int(Int8, Int16等含む) |int |int_hoge |
    |UInt(Uint8, UInt16等含む) |unt |unt_hoge |
    |Float |flt |flt_hoge |
    |Double |dbl |dbl_hoge |
    |Bool |bln |bln_hoge |
    |Character |chr |chr_hoge |
    |String |str |str_hoge |
    |Array |arr |arr_hoge |
    |Dictonary |dic |dic_hoge |
    |Set |set | set_hoge |

- 例
    ```
    int_number: Int = 5 
    flt_number: Float = 1.4 
    dbl_number: Double = 1.2 
    arr_car: [String] = ["hoge", "huga"]
    dic_car: [String: String] = ["hoge": "huga"]
    set_car: Set<String> = ["hoge", "huga"]
    ```


#### グローバル変数名
  極力実装しないことが望まれるが、やむを得ない場合は先頭に「g_」を加える

- 例  
    ```
    g_str_encode_type = "utf-8"
    ```


### 定数名
- 使用ケース  
  アッパースネークケース（*UPPER_SNAKE_CASE*）  

- 補足  
  基本的に定数名に型名は不要

- 例  
    ```
    // 良い例
    PI = 3.14159265359
    FILE_PATH = "/a/b/c/Documents/README.md"

    // 悪い例(基本的に先頭の型名は不要)
    DBL_PI = 3.14159265359
    STR_FILE_PATH = "/a/b/c/Documents/README.md"
    ```

### 関数名
- 使用ケース  
  キャメルケース(*camelCase*)

    ```
    func getUserName() {}
    ```


### クラス名、構造体名 
- 使用ケース  
  パスカルケース(*PascalCase*)

- 例
    ```
    class User {}
    struct HogeHuga {}
    ```


## その他ルール

- カンマの後は空白を入れる  
    ```
    [1, 2, 3]  
    ```

- 特に文字数は決めないが、一行が長くなりすぎないよう適度な文字数で改行を加え、折り返す。  

- 不等号は左向きのみ使用  
    ```
    0 < v && v <= 10  
    ```

- タブキー使用時はスペース4文字に変換するよう設定  
Xcode>Preference>Text Editing から設定  

- 型推論禁止  
Swiftでは型推論が可能なため、変数宣言時に必ずしも型宣言を行う必要はないが、コンパイル時間や可読性を考慮し、型宣言は必須とする。




