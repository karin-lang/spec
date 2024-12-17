# Type IR

## モジュール

- `constraint` ... 型制約テーブルを定義する
    - `lower` ... 型解析を実行する
- `log` ... ログを定義する

## 型解析手法

型制約テーブルを生成する

例えばこのような代入の場合

```rb
let i = 0
let j = i
```

型制約テーブルに順に制約を追加する

```rb
# 型注釈なしの数値代入のため i を number に制約する
i = number

↓-----↓

# 代入のため j を i の型に制約する
i = number
j = i

↓-----↓

# i の型を j に伝播する
i = number
j = number

↓-----↓

# 最終的に型注釈のない number は usize と認識する
i = usize
j = usize
```

この際に型の不一致などがあれば型エラーとして出力する

## 型の種類

|名称|英語名|説明|
|:-|:-|:-|
|推論型?|Inferable Type?|`number` などの他の型に推論可能な型|
|アイテム型|Item|構造型や列挙型など|
|基本型|Primitive Type|基本型|
|関数型|Function Type|関数の引数と返却値を定義した型|
|不明型|Unknown|未解決もしくは解決不可能な型|

## 制約テーブルに対する操作の種類

### 型の付与 (constrain by type)

### 他要素による制約の付与 (constraint by )


メモ：lowerのfinalize()でunknown型のエラーログを出す
