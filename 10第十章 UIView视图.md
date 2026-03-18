# iOS UIView 视图

## 📱 iOS UIView视图示例

以下是创建一个简单UIView视图的完整代码，包含视图位置、大小、背景色设置及添加到父视图的操作。

```swift
// 1. 定义视图的位置和大小（CGRect矩形区域）
// x: 距离父视图左侧30pt，y: 距离父视图顶部50pt
// width: 视图宽度250pt，height: 视图高度250pt
let rect1 = CGRect(x: 30, y: 50, width: 250, height: 250) 

// 2. 创建UIView实例，通过frame设置其位置和大小
// 注意：frame的坐标原点（x:0, y:0）对应父视图的左上角
// 此处若self.view为父视图，则对应屏幕左上角
let view1 = UIView(frame: rect1) 

// 3. 设置视图的背景颜色（棕色）
view1.backgroundColor = UIColor.brown 

// 4. 将创建的view1添加到当前控制器的根视图（self.view）上
// 只有添加到父视图后，view1才会在屏幕上显示
self.view.addSubview(view1)
```

### 关键说明

- CGRect：用于定义视图的位置（x,y）和尺寸（width,height），是iOS中设置视图布局的基础。

- frame：UIView的核心属性，决定视图在父视图中的位置和大小，坐标原点默认对应父视图左上角。

- addSubview：将子视图添加到父视图的方法，子视图会显示在父视图的上层，未添加则不会在屏幕上呈现。

- UIColor：用于设置视图背景色，可替换为系统自带颜色（如.red、.blue）或自定义颜色。