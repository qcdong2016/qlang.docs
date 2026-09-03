# QLang 语法

默认值传递。`struct T : Ref` 为 RC，类型名仍是 `T`。接口同 Go。多返回值同 Go。类型名可作值（类型 `Type`）；`Struct.Field` 可作值（类型 `StructField`）。类型断言：`typeof(x) == T`。可比：`Eq`。`Map` 为普通结构体，删键用 `Delete`。`string` 为 UTF-8。

源文件后缀 `.q`。语句无分号。`struct` / `interface` 声明以 `};` 结束。无元组、无 `++`/`--`。

语法按章节写在左侧目录。
