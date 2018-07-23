YYKit YYKit is a collection of iOS components. Its so huge that I split it into several independent components: YYModel — High performance model framework for iOS. YYCache — High performance cache framework for iOS. YYImage — Image framework for iOS to display/encode/decode animated WebP, APNG, GIF. YYWebImage — Asynchronous image loading framework. YYText — Powerful rich text component for iOS. YYKeyboardManager — Access keyboard view and track keyboard animation. YYDispatchQueuePool — iOS utility class to manage global dispatch queue. YYAsyncLayer — iOS utility classes for asynchronous rendering and display. YYCategories — A set of useful categories for Foundation and UIKit. Demo Project See Demo/YYKitDemo.xcodeproj Installation CocoaPods Add pod YYKit to your Podfile. Run pod install or pod update. Import \<YYKit/YYKit.h>. Carthage Add github "ibireme/YYKit" to your Cartfile. Run carthage update --platform ios and add the framework to your project. Import \<YYKit/YYKit.h>. Notice: carthage framework doesnt include webp component, if you want to support webp, use CocoaPods or install manually. Manually Download all the files in the YYKit subdirectory. Add the source files to your Xcode project. Add -fno-objc-arc compiler flag to NSObject+YYAddForARC.m and NSThread+YYAdd.m. Link with required frameworks: UIKit CoreFoundation CoreText CoreGraphics CoreImage QuartzCore ImageIO AssetsLibrary Accelerate MobileCoreServices SystemConfiguration sqlite3 libz Add Vendor/WebP.framework(static library) to your Xcode project if you want to support WebP. Import YYKit.h. Documentation Full API documentation is available on CocoaDocs. You can also install documentation locally using appledoc. Requirements This library requires iOS 6.0+ and Xcode 8.0+. Notice I want to use the APIs as if it was provided by system, and I dont add prefix in these categories. I do not recommend using the YYKit directly, you should try the separated components first. License YYKit is provided under the MIT license. See LICENSE file for details. 中文介绍 YYKit 是一组功能丰富的 iOS 组件。 为了尽量复用代码，这个项目中的某些组件之间有比较强的依赖关系。为了方便其他开发者使用，我从中拆分出以下独立组件： YYModel — 高性能的 iOS JSON 模型框架。 YYCache — 高性能的 iOS 缓存框架。 YYImage — 功能强大的 iOS 图像框架。 YYWebImage — 高性能的 iOS 异步图像加载框架。 YYText — 功能强大的 iOS 富文本框架。 YYKeyboardManager — iOS 键盘监听管理工具。 YYDispatchQueuePool — iOS 全局并发队列管理工具。 YYAsyncLayer — iOS 异步绘制与显示的工具。 YYCategories — 功能丰富的 Category 类型工具库。 演示项目 查看并运行 Demo/YYKitDemo.xcodeproj 安装 CocoaPods 在 Podfile 中添加 pod YYKit。 执行 pod install 或 pod update。 导入 \<YYKit/YYKit.h>。 Carthage 在 Cartfile 中添加 github "ibireme/YYKit"。 执行 carthage update --platform ios 并将生成的 framework 添加到你的工程。 导入 \<YYKit/YYKit.h>。 注意: carthage framework 并没有包含 webp 组件。如果你需要支持 webp，可以用 CocoaPods 安装，或者手动安装。 手动安装 下载 YYKit 文件夹内的所有内容。 将 YYKit 内的源文件添加(拖放)到你的工程。 为 NSObject+YYAddForARC.m 和 NSThread+YYAdd.m 添加编译参数 -fno-objc-arc。 链接以下 frameworks: UIKit CoreFoundation CoreText CoreGraphics CoreImage QuartzCore ImageIO AssetsLibrary Accelerate MobileCoreServices SystemConfiguration sqlite3 libz 如果你需要支持 WebP，可以将 Vendor/WebP.framework(静态库) 加入你的工程。 导入 YYKit.h。 文档 你可以在 CocoaDocs 查看在线 API 文档，也可以用 appledoc 本地生成文档。 系统要求 该项目最低支持 iOS 6.0 和 Xcode 8.0。 注意 我希望调用 API 时，有着和调用系统自带 API 一样的体验，所以我并没有为 Category 方法添加前缀。我已经用工具扫描过这个项目中的 API，确保没有对系统 API 产生影响，但即使这样没有前缀的 Category 也可能会带来其他麻烦。因此我不太推荐直接使用 YYKit 这个库，你应该先尝试一下上面那些拆分出来的独立组件。 许可证 YYKit 使用 MIT 许可证，详情见 LICENSE 文件。 相关文章 iOS 保持界面流畅的技巧