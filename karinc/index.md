# karinc

コンパイラのコア処理

|工程|モジュール|処理内容|データ変換形式|
|:-|:-|:-|:-|
|字句解析|lexer|トークン分割|Karin コード → トークン列|
|構文解析|parser|AST 生成, AST 最適化|トークン列 → AST|
|HIR 変換|hir|HIR 生成|AST → HIR|
|型テーブル生成|typesys|型テーブル生成|HIR → 型テーブル|
|Core IR 変換|cir|Core IR 生成|HIR, 型テーブル → Core IR|
