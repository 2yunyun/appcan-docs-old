# uexPopTipsView
  气泡菜单插件

## 方法：
### open 打开气泡菜单
### close 关闭气泡菜单

## 监听方法：
### onItemSelected 元素被点击的监听方法

### open
  打开气泡菜单
```
uexPopTipsView.open(json)
```
### 参数：
```
var json = {
    centerX:,//(必选) 气泡菜单箭头点的x坐标
    centerY:,//(必选) 气泡菜单箭头点的y坐标
    bgColor:,//(可选) 气泡菜单背景色，默认“#90000000”
    textNColor:,//(可选) 字体正常颜色，默认“#ffffff”
    textHColor:,//(可选) 字体高亮颜色，默认“#0000C6”
    textSize:,//(可选) 字体大小，单位px，默认15
    dividerColor:,//(可选) 分割线颜色，默认“#636363”
    labels:[]//(必选) //选项数组
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：

示例1:
```
    var param1 = {
        centerX:400,
        centerY:1000,
        labels:["复制","粘贴","删除"]
    };
    var data1 = JSON.stringify(param1);
    uexPopTipsView.open(data1);
```
运行效果：
![](http://i.imgur.com/DXoWut3.png)

示例2:
```
    var param1 = {
        centerX:500,
        centerY:1000,
        bgColor:"#d0ff0000",
        textNColor:"#FFFFFF",
        textHColor:"#BBBBBB",
        textSize:20,
        dividerColor:"#b0cccccc",
        labels:["复制","粘贴","回到首页","发消息"]
    };
    var data1 = JSON.stringify(param1);
    uexPopTipsView.open(data1);
```
运行效果：
![](http://i.imgur.com/QgSQ7zY.png)

### close
  关闭气泡菜单
```
uexPopTipsView.close()
```
### 参数：
```
无
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：

```
    uexPopTipsView.close();
```

### onItemSelected
元素被点击的监听方法
```
uexPopTipsView.onItemSelected(json);
```
### 参数：
```
var json = {
    index://被点击的元素的索引
}
```
### 平台支持：
```
Android 2.2+
iOS 6.0+
```
### 版本支持：
```
Android 3.0.0+
iOS 3.0.0+
```
### 示例：
```
    uexPopTipsView.onItemSelected = function(data){
        var index = JSON.parse(data).index;
        alert("点击了第" + (index + 1) + "个元素");
    }
```