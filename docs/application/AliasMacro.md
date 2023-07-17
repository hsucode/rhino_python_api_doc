# AliasMacro

返回或修改一个 Rhino 指令别名的巨集。
语法

rhinoscriptsyntax.AliasMacro (alias, macro=None)

rhinoscript.application.AliasMacro (alias, macro=None)
参数

alias
	

必须参数。字符串。现有指令别名的名称。

macro
	

可选参数。字符串。调用别名时要执行的新巨集指令。
返回值

字符串
	

如果新巨集指令没有指定，返回当前的巨集指令。

字符串
	

如果指定了新巨集指令，返回先前的巨集指令。
示例

```python

import rhinoscriptsyntax as rs

aliases = rs.AliasNames()

for alias in aliases:

    print alias, " -> ", rs.AliasMacro(alias)

 
``````
