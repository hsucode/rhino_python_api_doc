
# AppearanceColor

返回或修改一个程序外观条目的颜色。
语法

rhinoscriptsyntax.AppearanceColor (item, color=None)

rhinoscript.application.AppearanceColor (item, color=None)
参数

item
	

必须参数。数字。要查询或修改的条目对应的数字条目如下：

    
    值
    	
    
    描述
    
    0
    	
    
    视图背景
    
    1
    	
    
    主格线
    
    2
    	
    
    子格线
    
    3
    	
    
    X 轴
    
    4
    	
    
    Y 轴
    
    5
    	
    
    选取的物件
    
    6
    	
    
    锁定的物件
    
    7
    	
    
    新图层
    
    8
    	
    
    反馈图形
    
    9
    	
    
    轨迹线
    
    10
    	
    
    十字线
    
    11
    	
    
    文本
    
    12
    	
    
    文本背景
    
    13
    	
    
    Text hover
    


color
	

可选参数。新的颜色值。如果省略，返回当前条目颜色。
返回值

数字
	

如果没有指定 color 参数，返回条目当前的颜色。

数字
	

如果指定了 color 参数，返回条目先前的颜色。
示例

```python



import rhinoscriptsyntax as rs

oldColor = rs.AppearanceColor(0)

newColor = rs.GetColor(oldColor)

if newColor is not None:

    rs.AppearanceColor(0, newColor)

    rs.Redraw()

``````