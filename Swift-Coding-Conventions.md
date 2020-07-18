# Swiftコーディング規約

# Swiftコーディング規約について
Swiftにおけるコーディング規約を独自に作成。様々なコーディング規約を参考に随時更新していく。なお、本コーディング規約を利用して問題が発生した場合、我々は一切責任を負わない。


# 命名規則

## 定数
全て大文字  
PI

## グローバル変数
極力実装しない  
g_str_morning_time

## ローカル変数
スネーク  
str_user_name

cls_User = User()  
sct_BloodType = BloodType()  
int_number = 5 
flt_number = 1.4 
dbl_number = 1.2 
dic_car = ["hoge": "huga"]  
arr_car = ["hoge", "huga"]
set_car = ["hoge", "huga"] 



## クラス名 
パスカル  
User  
保留
クラス名の後ろにClassをつけるかどうか

## 構造体
パスカル  
BloodType  
クラス名の後ろにStructをつけるかどうか


## メンバ変数
スネーク  
str_user_name

## 関数
キャメル  
getUserName


## その他ルール

・カンマの後は空白を入れる  
[1, 2, 3]  

・特に文字数は決めないが、一行が長くなりすぎないよう適度な文字数で改行を加え、折り返す。  

・不等号は左向きのみ使用  
0 < v && v <= 10  

・タブキー使用時はスペース4文字に変換するよう設定  
Xcode>Preference>Text Editing から設定  





