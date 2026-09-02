# 附录 A. 词法


空白：空格、tab、换行。换行在 `)` `]` `}` `++` `--` 字面量、标识符之后可结束语句。

数字：`[0-9_]+`、`0x[0-9a-fA-F_]+`、`0b[01_]+`、`0o[0-7_]+`、`[0-9_]+\.[0-9_]*([eE][+-]?[0-9_]+)?`、`\.[0-9_]+([eE][+-]?[0-9_]+)?`。

标识符：`XID_Start` + `XID_Continue`，加 `_`。

运算符：

```
+ - * / % & | ^ &^ << >>
+= -= *= /= %= &= |= ^= <<= >>=
++ --
== != < <= > >=
&& || !
= :=
.
( ) [ ] { }
, : ; ...
```

`struct T : Ref` 的类型名仍是 `T`，无 `&` 前缀。`func Class.Func` 的 `.` 是方法声明，不是字段。类型名单独作表达式时类型为 `Type`；`StructName.Field`（右侧为字段）类型为 `StructField`。

```
package demo

struct Point { x int };
struct Node : Ref { v int };

func f() {
    p := Point{x: 1}
    n := Node{v: 1}
    var t Type = Point
    var m StructField = Point.x
    _ = p.x
    _ = n.v
}
```
