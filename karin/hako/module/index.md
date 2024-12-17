# モジュール

モジュール構造はディレクトリ構成で表現する。

karin ファイルを配置することで自動的にモジュールファイルとして認識される。サブフォルダに karin ファイルを配置することでサブモジュールとして認識される。同名の karin ファイルとモジュールフォルダの配置は許容される。

## 構造例

```rb
# ディレクトリ構成
<root>
  | mod.karin
  | mod/
    | submod2.karin
    | submod2/
      | submod2_1

# モジュール構成
mod
mod.submod2
mod.submod2.submod2_1
```
