

# ExtendCurveLength

按照指定的距离通过直线、圆弧或顺滑的过渡延伸一个未闭合的曲线物件。

语法

rhinoscriptsyntax.ExtendCurveLength (curve_id, extension_type, side, length)

rhinoscript.curve.ExtendCurveLength (curve_id, extension_type, side, length)
参数

curve_id
	

必须参数。字符串或 Guid。物件的 ID 。

extension_type
	

必须参数。数字。延伸的类型。

值
	

描述

0
	

直线 - 创建一个与原始曲线相切的直线延伸。

1
	

圆弧 - 创建一个与原始曲线相切的圆弧延伸。

2
	

顺滑 - 创建一个与原始曲线曲率连续光滑曲线。

side
	

必须参数。数字。延伸方向。

值
	

描述

0
	

从曲线起点开始延伸。

1
	

从曲线终点开始延伸。

2
	

从曲线起点和终点两个方向延伸。

length
	

必须参数。数字。曲线延伸的距离。
返回值

Guid
	

执行成功，返回延伸物件的ID。

None
	

如果执行不成功或出错，返回空值。
示例

```python

import rhinoscriptsyntax as rs

curve = rs.GetObject("Select curve to extend", rs.filter.curve)

if curve:

    length = rs.GetReal("Length to extend", 3.0)

    if length: rs.ExtendCurveLength( curve, 2, 2, length )
```