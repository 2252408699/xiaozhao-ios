---
layout: default
title: 我的 iOS 学习博客
---

# 🎯 欢迎来到我的ios学习技术博客！

我是正在学习 iOS 开发的新手，这里记录我的每一步成长。

## 📚  《ios 项目模版介绍》





### 无序列表
- 学会了 Swift 基础语法
- 搭建了开发环境
- 创建了 GitHub 账号

### 有序列表
1. 安装 Xcode
2. 新建 SwiftUI 项目
3. 运行模拟器

### 代码块
我用了 `URLSession` 来请求数据。

### 多行代码块
```swift
let url = URL(string: "https://api.quotable.io/random")!
let task = URLSession.shared.dataTask(with: url) { data, _, error in
    print("收到数据")
}
task.resume()
```

### 链接
[Quotable API 文档](https://api.quotable.io)
### 图片
![App截图](https://example.com/screenshot.png)
图片可以先上传到 GitHub 仓库的 images/ 文件夹，然后用相对路径

### 强调文字
*斜体*
**粗体**
***粗斜体***


- cd 你的项目路径
- git add .   # 添加所有修改/新增文件
- git commit -m "提交说明"
- git push origin main
