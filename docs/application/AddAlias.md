# AddAlias


为 Rhino 添加一个新的指令别名。指令别名可以在 Rhino 的 选项 菜单别名面板中进行修改。获取更多信息请参考 Rhino 帮助文件中关于 “别名选项” 的部分。
语法

rhinoscriptsyntax.AddAlias ( alias, macro )

rhinoscript.application.AddAlias ( alias, macro )
参数

alias
	

必须参数。字符串。新建指令别名的名称。名称不能和现有的指令别名相同。

macro
	

必须参数。字符串。调用别名时要执行的巨集指令。
返回值

布尔值
	

True 或 False 表示计算完成或失败。
示例

```python
import rhinoscriptsyntax as rs

rs.AddAlias("OriginLine", "!_Line 0,0,0")
```

