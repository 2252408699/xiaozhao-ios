# 📱 iOS Bundle 相关代码（获取应用配置信息）

以下代码用于获取 iOS 应用的核心配置信息（如应用名称、版本号、Bundle ID 等），可直接复制到 Swift 项目中使用，注释清晰易懂。

```swift
// 1. 获得当前程序可执行文件所在目录（主Bundle）
let mainBundle = Bundle.main

// 2. 获取应用的识别标识符（Bundle ID，如：com.xxx.app）
let identifier = mainBundle.bundleIdentifier

// 3. 获取应用的所有配置信息（info.plist 中的全部内容），存储在字典对象中
let info = mainBundle.infoDictionary

// 4. 获取应用名称（对应 info.plist 中的 CFBundleName）
let bundleId = mainBundle.object(forInfoDictionaryKey: "CFBundleName")

// 5. 获取应用版本号（对应 info.plist 中的 CFBundleShortVersionString，如：1.0.0）
let version = mainBundle.object(forInfoDictionaryKey: "CFBundleShortVersionString")

// 6. 打印获取到的所有配置信息（强制解包，仅用于调试，正式开发需做非空判断）
print("identifier:\(identifier!)")  // 打印 Bundle ID
print("info:\(info!)")              // 打印所有配置信息
print("bundleId:\(bundleId!)")      // 打印应用名称
print("version:\(version!)")        // 打印应用版本号
```

### 关键说明（补充笔记）

- `Bundle.main`：获取当前应用的主Bundle，是访问应用资源、配置信息的核心入口。

- `bundleIdentifier`：应用的唯一标识（Bundle ID），上架App Store必须唯一。

- `infoDictionary`：对应项目中的 `info.plist` 文件，包含所有应用配置。

- 代码中使用 `!` 强制解包，仅适合调试；正式开发需用 `if let` 或 `guard let` 做非空安全判断，避免崩溃。

### 正式开发安全写法（补充）

```swift
let mainBundle = Bundle.main
// 非空安全判断，避免崩溃
if let identifier = mainBundle.bundleIdentifier,
   let info = mainBundle.infoDictionary,
   let bundleName = mainBundle.object(forInfoDictionaryKey: "CFBundleName") as? String,
   let version = mainBundle.object(forInfoDictionaryKey: "CFBundleShortVersionString") as? String {
    print("identifier:\(identifier)")
    print("info:\(info)")
    print("bundleName:\(bundleName)")
    print("version:\(version)")
}
```