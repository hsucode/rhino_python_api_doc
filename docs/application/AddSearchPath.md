
# AddSearchPath

添加一个新路径到 Rhino 搜索路径列表。搜索路径可以在 Rhino 的 选项 菜单文件面板中进行修改。获取更多信息请参考 Rhino 帮助文件中关于 “文件选项” 的部分。
语法

rhinoscriptsyntax.AddSearchPath( folder, index=-1 )

rhinoscript.application.AddSearchPath( folder, index=-1 )
参数

folder
	

必须参数。字符串。要添加的文件夹或路径。

index
	

可选参数。数字。要插入路径列表的位置序号，序号从 0 开始计算。如果省略，路径将被添加到搜索路径列表的末尾。
返回值

数字
	

新搜索路径在列表中的位置序号。如果序号小于 0，说明搜索路径没有成功添加到列表中。
示例

```python
import rhinoscriptsyntax as rs

rs.AddSearchPath("C:\\My Python Scripts")
```
