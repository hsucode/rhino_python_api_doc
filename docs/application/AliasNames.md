
# AliasNames

返回指令别名的列表。
语法

rhinoscriptsyntax.aliasNames ()

rhinoscript.application.aliasNames ()
参数

空值。
返回值

列表
	

由指令别名字符串构成的列表。
示例

```python


import rhinoscriptsyntax as rs

aliases = rs.AliasNames()

for alias in aliases: print alias

``````
