# アイテム

## アクセス範囲

アイテムにはアクセス範囲を指定できる。

|名称|修飾子|アクセス範囲|
|:-|:-|:-|
|プライベート|なし|親アイテム内|
|パブリック|`pub`|すべて|

```rb
# プライベートアイテム
struct T {}

# パブリックアイテム
pub struct T {}
```

## アイテム一覧

- [構造体](./struct/index.md)
- [列挙体](./enum/index.md)
- [特性体](./trait/index.md)