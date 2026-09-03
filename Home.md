# QLang 语法

默认值传递。`struct T : Ref` 为 RC，类型名仍是 `T`。接口同 Go。`any` 是预声明空接口。多返回值无名字。类型名可作值（类型 `Type`）；`Struct.Field` 可作值（类型 `StructField`）。类型断言：`typeof(x) == T`。可比：`Eq`。`Map` 为普通结构体，删键用 `Delete`。`string` 为 UTF-8。全静态编译。

源文件后缀 `.q`。语句无分号。`struct` / `interface` 声明以 `};` 结束。

类型一律 `name : Type`。`type Count = int` 是新类型，互转须显式。类型参数 `<T: Interface>`，使用处显式写：`A<T>{}`、`f<T>()`。可重载 `+ - * / []` 等。

无：裸指针、`&`/`*` 类型、`const`/`iota`、结构体内嵌、命名返回值、元组、`++`/`--`、三元、并发、泛型接口、`init`、解释执行。
