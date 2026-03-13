# 📱 iOS LLDB 调试


### LLDB = 苹果官方自带的高性能调试器

- 配合 Xcode 使用
- 作用：暂停程序 → 查看变量 → 修改值 → 排查 bug
- 是 iOS /macOS 开发必备调试工具
- 代码断点 + LLDB 命令 = 最强调试组合

### 怎么用
- 在代码行号左边 点一下 → 出现蓝色断点
- 运行程序，触发断点后暂停
- 底部出现 (lldb) 控制台
- 直接输入命令即可

### 常用命令

1. po  打印对象
- po self.view
- po 变量名
- po "字符串"

2. p 打印基础类型
- p 100
- p self.view.frame

3. expression / e   运行代码 / 修改变量
- e self.view.alpha = 0.5
- e let a = 10 + 20

4. continue / c  继续运行程序

5. next / n  单步跳过（不进入函数）

6. step / s  单步进入（进入函数内部）

7. frame variable  查看当前所有变量

8. bt  查看函数调用栈（找崩溃原因神器）

9. p/x 数字  把数字用 十六进制 打印出来
![LLDB 进制转换](images/LLDB 进制转换.png)