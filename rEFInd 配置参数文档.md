# rEFInd 配置参数文档
<p align="right"><font color=#696968 size = 3>rEFInd Version: 0.13.3.1<br />Translater: NIXEVOK<br />Update: 2022/07/08</font></p>

## 前言

本文档是基于rEFInd 官方给出的配置解析翻译而成的，有些参数配置本人暂时没有使用到，

有些地方翻译可能不太准确，若翻译有误，请指出错误并提供正确的说明文档，本人会尽快修正。

如果您觉得我的文档对您有所帮助，欢迎 [👉捐赠👈](###捐赠)！谢谢！

## 配置代码列表

| 配置代码|中文注释| 默认值|
|-|-|-|
|[timeout](###timeout-主菜单屏幕超时秒数)                  | 主菜单屏幕超时秒数           | -                                                            |
| [shutdown_after_timeout](###shutdown_after_timeout - 超时后关机) | 超时后关机                   | true                                                         |
| [log_level](###log_level - 日志记录级别)                     | 日志记录级别                 | 0                                                            |
| [screensaver](###screensaver - 屏幕保护超时)                 | 屏幕保护程序超时             | 0                                                            |
| [icons_dir](###icons_dir  - 图标目录)                        | 图标目录                     | icons                                                        |
| [icon_size](###icon_size - 图标大小)                         | 图标大小                     | -                                                            |
| [selection Image](###selection Image - 选中时背景图像)       | 选中时背景图像               | -                                                            |
| [hideui](###hideui - 隐藏界面元素)                           | hideui                       | -                                                            |
| [banner](###banner - 背景图)                                 | 背景图                       | -                                                            |
| [banner_scale](###banner_scale - 背景图显示方式)             | 背景图显示方式               | noscale                                                      |
| [font](###font - 文本字体)                                   | 文本字体                     | rEFInd内置字体                                               |
| [textonly](###textonly - 文本模式)                           | 文本模式                     | 0                                                            |
| [textmode](###textmode - EFI文本模式)                        | EFI文本模式                  | 1024                                                         |
| [resolution](###resolution - 屏幕分辨率)                     | 屏幕分辨率                   | 0 0                                                          |
| [enable_touch](###enable_touch - 触摸屏支持)                 | 触摸屏支持                   | -                                                            |
| [enable_mouse](###enable_mouse - 鼠标支持)                   | 鼠标支持                     | -                                                            |
| [mouse_size](###mouse_size - 鼠标指针大小)                   | 鼠标指针大小                 | 16                                                           |
| [mouse_speed](###mouse_speed - 鼠标跟踪速度)                 | 鼠标跟踪速度                 | 4                                                            |
| [use_graphics_for](###use_graphics_for - 以图形模式启动指定的操作系统) | 以图形模式启动指定的操作系统 | osx                                                          |
| [showtools](###showtools - 工具行)                           | 工具行                       | 请查看配置说明                                       |
| [dont_scan_tools](###dont_scan_tools - 排除的工具)           | 排除的工具                   | -                                                            |
| [windows_recovery_files](###windows_recovery_files - Windows救援系统引导) | Windows救援系统引导          | 请查看配置说明 |
| [scan_driver_dirs](###scan_driver_dirs - 在其中搜索 EFI 驱动程序的目录) | 在其中搜索 EFI 驱动程序的目录 | - |
| [scanfor](###scanfor - 要搜索的引导加载程序类型以及显示顺序) | 要搜索的引导加载程序类型以及显示顺序 | 请查看配置说明 |
| [uefi_deep_legacy_scan](###uefi_deep_legacy_scan - 深度扫描) | 深度扫描 | - |
| [scan_delay](###scan_delay - 扫描延迟) | 扫描延迟 | 0 |
| [also_scan_dirs](###also_scan_dirs - 总是扫描目录) | 总是扫描目录 | 请查看配置说明 |
| [dont_scan_volumes](###dont_scan_volumes - 忽略扫描的分区) | 忽略扫描的分区 | LRS_ESP |
| [dont_scan_dirs](###dont_scan_dirs - 不扫描引导的目录) | 不扫描引导的目录 | - |
| [dont_scan_files](###dont_scan_files - 不扫描的引导文件) | 不扫描的引导文件 | 请查看配置说明 |
| [dont_scan_firmware](###dont_scan_firmware - 不扫描的固件) | 不扫描的固件 | - |
| [scan_all_linux_kernels](###scan_all_linux_kernels - 扫描缺少文件扩展名的Linux内核) | 扫描缺少文件扩展名的Linux内核 | true |
| [fold_linux_kernels](###fold_linux_kernels - Linux内核合并) | Linux内核合并 | true |
| [extra_kernel_version_strings](###extra_kernel_version_strings - 内核列表编号化) | 内核列表编号化 | - |
| [write_systemd_vars](###write_systemd_vars - 写入系统变量) | 写入系统变量 | false |
| [max_tags](###max_tags - 最大标签个数) | 最大标签个数 | 0 |
| [default_selection](###default_selection - 默认菜单选择) | 默认菜单选择 | 请查看配置说明 |
| [enable_and_lock_vmx](###enable_and_lock_vmx - 启用VMX位) | 启用VMX位 | false |
| [spoof_osx_version](###spoof_osx_version - MacOS启动欺骗) | MacOS启动欺骗 | - |
| [csr_values](###csr_values - 设置苹果csr值) | 设置苹果csr值 | - |
| [include](###include - 引入配置文件) | 引入配置文件 | - |
| [menuentry](###menuentry - 手动配置节点) | 手动配置节点 | 请查看[示例](###下面是几个示例引导节点配置) |



## 配置详细说明

 ### timeout - 主菜单屏幕超时秒数 ###

 - 如果设置为 0 则代表无超时,需用户手动选择需启动的系统

 - 如果设置为 -1 则立即启动到默认操作系统,
   除非在启动时有按键在缓冲区中,否则在这种情况下,按键被解释为快捷键。
     (例如 上下左右方向键等快捷键)
     如果未找到匹配的快捷方式,则 rEFInd 将显示其菜单而不会超时。

     - 例: 
       ```refind conf
       timeout 30
       ```
> [Top](##配置代码列表)



 ### shutdown_after_timeout - 超时后关机 ###

   - 通常情况下,当超时期限过后,rEFInd 会启动默认选择。 
   - 但是,如果未注释以下选项,rEFInd 将尝试关闭计算机。
   - <font color=Red>注意：许多计算机会挂起或重新启动！</font>
   - Mac 和基于 UEFI 的 PC 最有可能使用此功能。
   - 默认值为 true

     - 例:
     ```refind conf
     shutdown_after_timeout false
     ```
> [Top](##配置代码列表)



 ### log_level - 日志记录级别 ###

 - 当设置为 0 时,rEFInd 不会记录其操作。

 - 当设置为 1 或以上时,rEFInd 会创建一个名为 refind.log 的文件

 - 当设置为 1 或更高时,rEFInd 在 ESP 的主目录中创建一个名为 refind.log 的文件
   并记录有关它正在做什么的信息。 较高的值记录更多的信息,最多 4 个

 - 除调试问题外,此标记应保留为默认值 0。
     - 例: 
     
     ```refind conf
     log_level 1
     ```
> [Top](##配置代码列表)


### screensaver - 屏幕保护超时 ###

- 在没有键盘输入的指定秒数后屏幕空白。 
- 大多数按键后屏幕返回<font color=red>（注意不包括修改键,如 Shift、Control、Alt 或 Option）</font>。 
- 将值设置为"-1"会导致 rEFInd 在其屏幕保护程序处于活动状态时启动。 
- 默认值为 0 (单位：秒)，即禁用屏幕保护程序。
	
	- 例:
	
	```refind conf
	screensaver 300
	```
> [Top](##配置代码列表)



### use_nvram - NVRAM配置 ###

- 是否将 rEFInd 的 rEFInd 特定变量存储在 NVRAM（1、true 或 on）
   或磁盘上 rEFInd 目录的"vars"子目录中的文件中（0、false 或 off）。 
   
- 使用 NVRAM 适用于大多数计算机；但是，它会增加主板 NVRAM 的磨损，
   如果 EFI 有问题或 NVRAM 旧且磨损，它可能根本无法工作。
   
- 在这种情况下，或者如果您想最大程度地减少 NVRAM 的磨损，
   将变量存储在磁盘上是一种可行的选择； 
   但是，如果 rEFInd 存储在对 EFI 只读的文件系统（例如 HFS+ 卷）上，
   它将不起作用，并且会增加文件系统损坏的风险。 
   
- <font color=red> 请注意： 此选项仅影响 rEFInd 自己的变量，</font>
  
    <font color=red>例如 PreviousBoot、HiddenTags、HiddenTools 和 HiddenLegacy 变量，</font>
    
    <font color =red>它不会影响 安全启动 或 其他非 rEFInd 变量。</font>
    
- 默认值为 true

    - 例:

      ```refind conf
      use_nvram false
      ```
> [Top](##配置代码列表)



### icons_dir  - 图标目录 ###

- 设置存储图标的子目录的路径。 图标必须与标准目录中的名称相同。

- 图标目录是相对于 refind.efi 所在目录的。

- 如果在指定目录中找不到图标，则尝试从默认目录加载它；

- 因此，您可以只替换您自己目录中的一些图标，并依赖其他图标的默认值。 

- 图标文件可以是任何支持的格式:
  ICNS (*.icns)、BMP (*.bmp)、PNG (*.png) 或 JPEG (*.jpg 或 *.jpeg)； 

- <font color=red>注意: rEFInd 的 BMP 和 JPEG 实现不支持透明度，这在图标中是非常需要的。</font>

- 默认值为 "icons";

  - 例:

    ```refind conf
    icons_dir myicons
    icons_dir icons/snowy
    ```
> [Top](##配置代码列表)



### icon_size - 图标大小 

- 所有图标都是方形的，因此只指定了一个值。

- 大图标用于第一行的操作系统选择器，小图标用于第二行的工具。

- 驱动型徽章是大图标大小的 1/4，合法值为 32 及以上。

- 如果图标文件不包含适当大小的图标，则图标将缩放到指定大小。

- 小图标和大图标的默认值分别为 48 和 128。

  - 例：

    ```refind conf
    small_icon_size 96
    big_icon_size 256
    ```

> [Top](##配置代码列表)



### selection Image - 选中时背景图像

- 选中时背景的自定义图像。

- 操作系统图标有一个大的 (144 x 144)，第二行的功能图标有一个小的 (64 x 64)。
  
- 如果只给出一个小图像，则该图像也可以通过在中间拉伸来用于大图标。

- 如果只给出一个大图标，则内置默认值将用于小图标。

- 如果指定了不是最佳尺寸的图像，它将以一种可能很难看的方式缩放。

- <font color=red>注意：这些选项采用颜色深度为 24、8、4 或 1 位的未压缩 BMP、PNG、JPEG 或 ICNS 图像文件的文件名。</font>
  
- 如果您需要透明度支持（让您"透视"到全屏背景图），则需要 PNG 或 ICNS 格式。

   - 例：

      ```refind conf
      selection_big   selection-big.bmp
      selection_small selection-small.bmp
      ```

> [Top](##配置代码列表)



### hideui - 隐藏界面元素

- 隐藏用户界面元素以满足个人喜好或增加安全性。

- 参数列表：
  | 参数 | 详细 |
  |-|-|
  |  banner      | rEFInd 背景图（内置或通过 "banner" 加载） |
  |  label       | 菜单中的引导选项文本标签|
  |  singleuser  | 删除以单用户或详细模式启动 macOS 的子菜单选项；(仅影响 macOS)|
  |  safemode    | 删除以"安全模式"启动 macOS 的子菜单选项|
  |  hwtest      | 运行 Apple 硬件测试的子菜单选项|
  |  arrows      | 操作系统选择标记行上的滚动箭头|
  |  hints       | 菜单中的 简短命令 摘要|
  |  editor      | 选项编辑器（+、F2 或在引导选项菜单上插入）|
  |  badges      | 引导选项的设备类型标志|
  |  all         | 上述所有的|

- 默认 所有元素都处于活动(显示) 状态

  - 例：

    ```refind conf
    hideui label，singleuser
    ```
>[Top](##配置代码列表)



### banner - 背景图

- 使用自定义背景图

- 文件路径是相对于 refind.efi 所在目录的。

- 图像左上角的颜色用作菜单屏幕的背景颜色。

- 目前支持颜色深度为 24、8、4 或 1 位的未压缩 BMP 图像，以及 PNG 和 JPEG 图像。

- 也可以使用 ICNS 图像，但 ICNS 的局限性使其成为此目的的糟糕选择。

- PNG 和 JPEG 支持受到底层库的限制； 某些文件（例如渐进式 JPEG）将无法使用。

  - 例：

    ```refind conf
    banner icons/snowy/banner-snowy.png
    ```
> [Top](##配置代码列表)



### banner_scale - 背景图显示方式

- 指定如何处理与屏幕尺寸不完全相同的背景图。

- 选项列表：

| 选项 | 说明 |
| - | - |
| noscale | 如果太大则裁剪，如果太小则显示边框（自动缩放） |
| fillscreen | 填满屏幕（全屏） |

- 默认值为 noscale

  - 例：

    ```refind conf
    banner_scale fillscreen
    ```
> [Top](##配置代码列表)



### font - 文本字体

- 设置要用于图形模式下所有文本显示的字体。

- 为获得最佳效果，字体必须是具有 Alpha 通道透明度的 PNG 文件。 

- 它必须包含 32-126 的 ASCII 字符（通过波浪号的空格），
  包括 32-126，加上一个要显示的字形来代替此范围之外的字符，总共 96 个字形。

- 仅支持等宽字体。 字体可以是任意大小，但大字体可能会导致显示不规则。

- 默认是 rEFInd 的内置字体，Luxi Mono Regular 12 磅。

  - 例：

    ```refind conf
    font myfont.png
    ```
> [Top](##配置代码列表)



### textonly - 文本模式 

- 仅使用文本模式。 

- 启用后，此选项会强制 rEFInd 进入文本模式。

- 设置为 "0" 会使用图形模式。

- 不设置任何值或设置任何非 "0" 值都会使用文本模式。

- 默认是使用图形模式(0)。

  - 例：

    ```refind conf
    textonly 0
    ```
> [Top](##配置代码列表)



### textmode - EFI文本模式

- 设置用于文本显示的 EFI 文本模式。

- 此选项采用单个数字表示模式编号。

- 模式 0 通常是 80x25，1 有时是 80x50，更大的数字是系统特定的模式。

- 模式 1024 是一个特殊代码，告诉 rEFInd 不要设置文本模式；
     (它使用程序启动时正在使用的任何内容)。
     
- 如果你指定了一个无效的模式，rEFInd 会在启动过程中暂停以通知你有效的模式。

- <font color=red> 注意：在 VirtualBox 上，也许在某些真实计算机上，</font>
  <font color=red> 指定文本模式并取消注释“textonly”选项 而未指定分辨率可能会导致启动的操作系统中的显示不可用。</font>
  
- 默认为 1024（无变化）

     - 例：

       ```refind conf
       textmode 1024
       ```
> [Top](##配置代码列表)



### resolution - 屏幕分辨率

- 设置屏幕分辨率。

- 传递以下选项之一： 

  | 选项                    | 说明                       |
  | ----------------------- | -------------------------- |
  | 两个整数值 例：1024 768 | 对应于 X 和 Y 分辨率       |
  | 一个整数值 例：3        | 对应于 GOP (UEFI) 视频模式 |
  | 字符串“max”             | 设置最大可用分辨率         |

- 请注意，并非所有分辨率都受支持。

- 在 UEFI 系统上，传递不正确的值会导致屏幕上显示一条消息，以及支持的模式列表。

- 在 EFI 1.x 系统（例如, Macintoshes)，设置不正确的模式会静默失败。

- 在这两种类型的系统上，设置不正确的分辨率会导致使用默认分辨率。

- 1024x768 的分辨率通常有效，但较高的值通常无效。

- 默认为“0 0”（使用系统默认分辨率，通常为800x600）。

   - 例：

     ```refind conf
     resolution 1440 900
     resolution 3
     resolution max
     ```

> [Top](##配置代码列表)



### enable_touch - 触摸屏支持

- 如果激活，此功能可以使用触摸屏控件（如在平板电脑上）。

- 但是请注意，并非所有平板电脑的 EFI 都提供必要的底层支持，因此此功能可能不适合您。

- 如果它确实有效，您应该能够通过触摸它来启动操作系统或工具。

- 在子菜单中，触摸任何地方都会启动当前选择的项目； 目前，无法选择特定的子菜单项。

- <font color=red>注意：此功能与 [enable_mouse](###enable_mouse - 鼠标支持) 功能互斥；如果两者都未注释，则最近读取的优先。</font>

  - 例：

    ```refind conf
    enable_touch
    ```

> [Top](##配置代码列表)



### enable_mouse - 鼠标支持

- 如果激活，此功能可以使用计算机的鼠标。

- 但是请注意，并非所有计算机的 EFI 都提供必要的底层支持，因此此功能可能不适合您。

- 如果它确实有效，您应该能够通过用鼠标指针单击它来启动操作系统或工具。

- <font color=red>注意：此功能与 [enable_touch](###enable_touch - 触摸屏支持) 功能互斥；如果两者都未注释，则最近读取的优先。</font>

  - 例：

    ```refind conf
    enable_mouse
    ```

> [Top](##配置代码列表)



### mouse_size - 鼠标指针大小

- 鼠标指针的大小，以像素为单位。

- 默认为 16

  - 例：

    ```refind conf
    mouse_size 16
    ```

> [Top](##配置代码列表)



### mouse_speed - 鼠标跟踪速度

- 数字越大，鼠标移动越快。

- 此选项要求取消注释 [enable_mouse](###enable_mouse - 鼠标支持)。

- 合法值在 1 到 32 之间。

- 默认为 4。

  - 例：

    ```refind conf
    mouse_speed 4
    ```

> [Top](##配置代码列表)



### use_graphics_for - 以图形模式启动指定的操作系统

- 默认情况下，rEFInd 会在启动除 macOS 之外的所有操作系统时切换到文本模式并显示基本的启动前信息。

- 使用图形模式可以产生更无缝的过渡，但不显示任何信息，如果您必须调试问题，这可能会使事情变得困难。

- 另外，在至少一台已知的计算机上，使用图形模式可以防止在使用 Linux 内核的 EFI kernel 时发生崩溃。

- 您可以指定一个空列表以文本模式启动所有操作系统。

- 有效选项：

  | 参数    | 说明                             |
  | ------- | -------------------------------- |
  | osx     | macOS                            |
  | linux   | 带有 EFI kernel 的 Linux 内核    |
  | elilo   | ELILO 引导加载程序               |
  | grub    | GRUB（旧版或 GRUB2）引导加载程序 |
  | windows | Microsoft Windows                |

- 默认值： osx

  - 例

    ```refind conf
    use_graphics_for osx,linux
    ```

> [Top](##配置代码列表)



### showtools - 工具行

- 在工具行上显示哪些非引导加载程序工具，以及显示它们的顺序；

- 参数列表：

  | 参数             | 说明                                                         |
  | ---------------- | ------------------------------------------------------------ |
  | shell            | EFI shell(需要外部程序；有关详细信息，请参阅 rEFInd 文档)    |
  | memtest          | memtest86 程序，位于 EFI/tools、EFI/memtest86、EFI/memtest、EFI/tools/memtest86 或 EFI/tools/memtest |
  | gptsync          | <font color=red>（危险的）</font>gptsync.efi 实用程序（需要外部程序；有关详细信息，请参阅 rEFInd 文档） |
  | gdisk            | gdisk 分区程序                                               |
  | apple_recovery   | 启动 Apple Recovery HD 分区（如果存在）                      |
  | windows_recovery | 启动 OEM Windows 恢复工具（如果存在，另请参阅 windows_recovery_files 选项）。 |
  | mok_tool         | 提供用于安全启动系统的机器所有者密钥 (MOK) 维护工具 MokManager.efi。 |
  | csr_rotate       | 调整 Apple 系统完整性保护 (SIP) 策略。 需要设置“csr_values”。 |
  | install          | 将 rEFInd 从当前位置安装到另一个 ESP 的选项                  |
  | bootorder        | 调整 EFI（非 rEFInd）的引导顺序                              |
  | about            | “关于这个程序”选项                                           |
  | hidden_tags      | 管理隐藏标签                                                 |
  | exit             | 从 rEFInd 退出的标签                                         |
  | shutdown         | 关闭计算机，<font color=red>注意：一个错误导致这会重新启动许多 UEFI 系统</font> |
  | reboot           | 重新启动计算机的标签                                         |
  | firmware         | 将计算机重新引导到固件用户界面的标签（在旧计算机上被忽略）   |
  | fwupdate         | 用于更新固件的标签； 启动 fwupx64.efi（或类似的）程序        |
  | netboot          | 启动用于网络 (PXE) 引导的 ipxe.efi 工具                      |
- 默认值：shell,memtest,gdisk,apple_recovery,windows_recovery,mok_tool,about,hidden_tags,shutdown,reboot,firmware,fwupdate

- 要完全禁用对所有工具的扫描，请提供不带选项的 showtools 行。

  - 例：

    ```refind conf
    showtools shell, bootorder, gdisk, memtest, mok_tool, apple_recovery, windows_recovery
    ```

> [Top](##配置代码列表)





### dont_scan_tools - 排除的工具

- 要从工具行中排除的工具文件，即使在 showtools 中指定了通用类。

- 这可以修剪过多的工具，例如在安装多个 Linux 发行版后看到多个 mok_tool 条目时。

- 与 [dont_scan_files](###) 一样，您可以单独指定文件名、完整路径名或
  卷标识符（文件系统标签、分区名称或分区 GUID）和完整路径名。

- 默认为空列表（不排除任何内容）

  - 例：

    ```refind conf
    dont_scan_tools ESP2:/EFI/ubuntu/mmx64.efi,gptsync_x64.efi
    ```

> [Top](##配置代码列表)



### windows_recovery_files - Windows救援系统引导

- 可以启动 Windows 还原或紧急系统的引导加载程序。

- 这些往往是 OEM 特定的。

- 默认为 LRS_ESP:/EFI/Microsoft/Boot/LrsBootmgr.efi

  - 例：

    ```refind conf
    windows_recovery_files LRS_ESP:/EFI/Microsoft/Boot/LrsBootmgr.efi
    ```

> [Top](##配置代码列表)



### scan_driver_dirs - 在其中搜索 EFI 驱动程序的目录

- 这些驱动程序可以提供文件系统支持，允许访问插件控制器上的硬盘等。

- 在大多数情况下都不需要，但如果你添加了 EFI 驱动程序并希望 rEFInd 自动加载它们，

- 你应该在这里指定一个或多个路径。

- rEFInd 总是扫描它自己安装目录的“drivers”和“drivers_{arch}”子目录（其中“{arch}”是你的架构代码）；

- 此选项指定要扫描的其他目录。

- 默认是不扫描 EFI 驱动程序的其他目录。

  - 例：

    ```refind conf
    scan_driver_dirs EFI/tools/drivers,drivers
    ```

> [Top](##配置代码列表)



### scanfor - 要搜索的引导加载程序类型以及显示顺序

- 参数列表：

  | 参数         | 说明                                   |
  | ------------ | -------------------------------------- |
  | internal     | 基于内部 EFI 磁盘的引导加载程序        |
  | external     | 基于外部 EFI 磁盘的引导加载程序        |
  | optical      | EFI 光盘（CD、DVD 等）                 |
  | netboot      | EFI 网络 (PXE) 引导选项                |
  | hdbios       | 基于 BIOS 磁盘的引导加载程序           |
  | biosexternal | BIOS 外部引导加载程序（USB、eSATA 等） |
  | cd           | BIOS 光盘引导加载程序                  |
  | manual       | 稍后在此配置文件中使用节               |
  | firmware     | 启动固件 NVRAM 中设置的 EFI 程序       |

- <font color=red>请注意：旧版 BIOS 选项需要固件支持，但并非所有计算机都提供此支持。</font>

- netboot 选项是实验性的，依赖于 ipxe.efi 和 ipxe_discover.efi 程序文件。

- 在 UEFI PC 上，默认为 internal,external,optical,manual

- 在 Macs 上, 默认为 internal,hdbios,external,biosexternal,optical,cd,manual

  - 例：

    ```refind conf
    scanfor internal,external,optical,manual,firmware
    ```

> [Top](##配置代码列表)



### uefi_deep_legacy_scan - 深度扫描

- 默认情况下，rEFInd 依赖 UEFI 固件来检测 BIOS 模式启动设备。

- 不过，这有时不会检测到所有可用的设备。

- 对于这些情况，uefi_deep_legacy_scan 会在每次启动时强制扫描和修改 NVRAM 变量。

- 添加“0”、“off”或“false”将重置为默认值。

- 此标记对 Mac 或未通过 scanfor 设置 BIOS 模式选项时无效。

- 默认未设置（或“uefi_deep_legacy_scan false”）

  - 例：

    ```refind conf
    uefi_deep_legacy_scan true
    ```
    
> [Top](##配置代码列表)



### scan_delay - 扫描延迟

- 在扫描磁盘之前延迟指定的秒数。

- 这可以帮助一些用户发现他们的某些磁盘（通常是外部或光盘）最初没有被检测到，但在按 Esc 后被检测到。

- 默认为 0

  - 例：

    ```refind conf
    scan_delay 5
    ```
    
> [Top](##配置代码列表)



### also_scan_dirs - 总是扫描目录

- 在为 EFI 引导加载程序扫描卷时，
  rEFInd 总是在其正常位置查找 macOS 和 Microsoft Windows 的引导加载程序，
  并扫描 /EFI 目录的根目录和每个子目录以查找其他引导加载程序，但它不会递归到 这些目录。
  
- also_scan_dirs 标记将更多目录添加到扫描列表中。

- 目录是相对于卷的根目录指定的。

- 此选项适用于 rEFInd 扫描的所有卷，除非您在目录名之前包含卷名和冒号，
  如在“myvol:/somedir”中仅扫描名为 myvol 的文件系统上的 somedir 目录。

- 如果指定的目录不存在，则忽略它（没有错误条件结果）。

- 默认是扫描“boot”目录以及各种硬编码目录。

  - 例：

    ```refind conf
    also_scan_dirs boot,ESP2:EFI/linux/kernels
    ```

[Top](##配置代码列表)



### dont_scan_volumes - 不扫描引导的分区

- 从扫描中忽略的分区（或整个磁盘，用于传统模式引导）。

- 对于 EFI 模式扫描，您通常通过其标签指定卷，
  您可以在 EFI shell 中通过键入“vol”、在 Linux 中通过键入“blkid /dev/{devicename}”
  或通过在各种操作系统的文件浏览器中检查磁盘的标签来获得该卷。

- 也可以通过其唯一的 GUID（在 Linux 用语中称为“PARTUUID”）来识别分区。<font color=red>（请注意，这不是分区类型代码 GUID) </font>

- 此标识符可以通过 Linux 中的“blkid”或 macOS 中的“diskutil info {partition-id}”获取。

- 对于传统模式扫描，您可以指定在 rEFInd 中突出显示该选项时显示的引导加载程序描述的任何子集。

- 默认为“LRS_ESP”

  - 例：

    ```refind conf
    dont_scan_volumes "Recovery HD"
    ```

> [Top](##配置代码列表)



### dont_scan_dirs - 不扫描引导的目录

- 默认情况下，rEFInd 不扫描自己的目录，EFI/tools 目录，EFI/memtest 目录，
  EFI/memtest86 目录，com.apple.recovery.boot 目录。

- 使用 dont_scan_dirs 选项可以将其他目录“列入黑名单”；

- 但如果要继续将现有目录列入黑名单，请务必使用“+”作为第一个元素。

- 如果 EFI/boot/bootx64.efi 是另一个引导加载程序的副本，

- 或者排除包含硬件制造商提供的驱动程序或非引导加载程序实用程序的目录，
  您可以使用此标记将 EFI/boot/bootx64.efi 排除在菜单之外。

- 如果一个目录在此处和also_scan_dirs 中都列出，则dont_scan_dirs 优先。

- <font color=red>请注意，此黑名单适用于 rEFInd 扫描的所有文件系统，而不仅仅是 ESP，</font>
  <font color=red>除非您在目录名称前加上文件系统名称或分区唯一 GUID，</font>
  <font color=red>如在“myvol:EFI/somedir”中排除 EFI/somedir扫描 myvol 卷，但不扫描其他卷。</font>
  
  - 例：
  
    ```refind conf
    dont_scan_dirs ESP:/EFI/boot,EFI/Dell,EFI/memtest86
    ```

> [Top](##配置代码列表)



### dont_scan_files - 不扫描的引导文件

- 不应作为 EFI 引导加载程序包含的文件（在显示的第一行）。

- 如果您使用的引导加载程序依赖于与主二进制文件一起安装的支持程序或驱动程序，
  或者如果您想按名称而不是位置将某些加载程序“列入黑名单”，请使用此选项。
  
- <font color=red>请注意，这不会阻止某些二进制文件出现在第二行工具集中。</font>

- 最值得注意的是，此列表中存在各种安全启动和恢复工具，但可能显示为第二行项目。

- 文件可以指定为裸名（例如，“notme.efi”）、完整的路径名（例如，“/EFI/somedir/notme.efi”）
  或带有卷的完整路径名（例如，“ SOMEDISK:/EFI/somedir/notme.efi" 
  或 2C17D5ED-850D-4F76-BA31-47A561740082:/EFI/somedir/notme.efi")。
  
- 通过 rEFInd 菜单中的 Delete 或“-”键隐藏的操作系统标签将添加到此列表中，但存储在 NVRAM 中。

- 默认为 shim.efi,shim-fedora.efi,shimx64.efi,PreLoader.efi,
  TextMode.efi,ebounce.efi,GraphicsConsole.efi,MokManager.efi,HashTool.efi,
  HashTool-signed.efi,bootmgr.efi,fb{arch}.efi（其中“{arch}”是架构代码，如“x64”）。
  
- 如果要保留这些默认值但要添加它们，请务必将“+”指定为新列表中的第一项； 

- 如果您不这样做，则可能会出现默认列表中的项目。

  - 例：

    ```refind conf
    dont_scan_files shim.efi,MokManager.efi
    ```

> [Top](##配置代码列表)



### dont_scan_firmware - 不扫描的固件

- EFI NVRAM Boot#### 
  当“固件(firmware)”是“扫描(scanfor)”选项时不应作为加载程序出现的变量
  
- 此处显示的逗号分隔列表包含与描述字段匹配的字符串——

- 如果此处的值是引导选项描述的子字符串(不区分大小写)，则它将被排除在引导列表之外。

- 要指定包含空格的字符串，请将其括在引号中。

- 指定“shell”将抵消内置 EFI shell 的自动包含。

  - 例：

    ```refind conf
    dont_scan_firmware HARDDISK,shell,"Removable Device"
    ```


> [Top](##配置代码列表)





### scan_all_linux_kernels - 扫描缺少文件扩展名的Linux内核

- 扫描缺少“.efi”文件扩展名的 Linux 内核。

- 这对于更好地与为内核提供 EFI 存根加载程序但不为那些
  内核提供以“.efi”结尾的文件名的 Linux 发行版集成很有用，
  特别是如果内核存储在 EFI 可以读取的文件系统上。

- 当设置为“1”、“true”或“on”时，此选项会导致扫描
  目录中名称以“vmlinuz”、“bzImage”或“kernel”开头的所有
  文件作为加载程序包含在内，即使 他们缺少“.efi”扩展名。

- 传递这个选项“0”、“false”或“off”值会导致不扫描没有“.efi”扩展名的内核。

- 默认为“true”——扫描没有“.efi”扩展名的内核。

  - 例：

    ```refind conf
    scan_all_linux_kernels false
    ```

> [Top](##配置代码列表)



### fold_linux_kernels - Linux内核合并

- 将给定目录中的所有 Linux 内核合并到一个条目中。

- 这样设置后，默认启动具有最新时间戳的内核，其文件名将出现在条目的描述中。

- 要启动其他内核，用户必须按 F2 或 Insert； 然后备用内核作为选项出现在子菜单上。

- 默认为“true”——内核被“折叠”到单个菜单项中。

  - 例：

    ```refind conf
    fold_linux_kernels false
    ```

> [Top](##配置代码列表)



### extra_kernel_version_strings - 内核列表编号化

- 以逗号分隔的字符串列表，将它们视为数字，以便检测内核版本号。

- 这些字符串在第一次找到的基础上匹配；

- 也就是说，如果要将“linux-lts”和“linux”都视为版本字符串，则必须将它们指定为“linux-lts,linux”，
  因为如果以另一种方式指定，vmlinuz-linux 和 vmlinuz -linux-lts 将返回“linux”作为“版本字符串”，这不是您想要的。
  
- 此外，如果内核或 initrd 文件包含指定的字符串和数字，则“版本字符串”包含两者。

- 例如，“vmlinuz-linux-4.8”会产生一个版本字符串“linux-4.8”。

- 此选项适用于 Arch 和其他在其内核文件名中不包含版本号的发行版，但可能会为多个内核提供其他唯一标识字符串。

- 如果此功能导致问题（例如，如果您的内核文件名包含“linux”但 initrd 文件名不包含），
  请确保将其设置为空字符串（extra_kernel_version_strings“”）或注释掉禁用它的选项。
  
- 默认是没有额外的版本字符串。

  - 例：

    ```refind conf
    extra_kernel_version_strings linux-lts,linux
    ```

> [Top](##配置代码列表)



### write_systemd_vars - 写入系统变量

- 通过 EFI 存根加载程序、ELILO 或 GRUB 启动 Linux 时，
  写入 systemd EFI 变量（当前只有 LoaderDevicePartUUID）。
  
- 这个变量，当存在时，会导致 systemd 将 ESP 挂载到 /boot 或 /efi *IF* 任一目录为空，
  并且没有其他任何东西挂载在那里。
  
- 默认为“false”

  - 例：

    ```refind conf
    write_systemd_vars true
    ```

> [Top](##配置代码列表)



### max_tags - 最大标签个数

- 设置屏幕上随时可以显示的最大标签个数。

- 如果发现的加载器比这个值多，rEFInd 会在滚动列表中显示一个子集。

- 如果此值设置得太高，屏幕无法处理，则将其降低到屏幕可以管理的值。

- 如果此值设置为 0（默认值），则将其调整为屏幕可以处理的数字。

- 默认值为 0

  - 例：

    ```refind conf
    max_tags 0
    ```

>[Top](##配置代码列表)



### default_selection - 默认菜单选择

- 可用的参数与 rEFInd 中可用的键盘加速键相匹配。

- 你可以使用:.

  - 1 到 9 之间的数字，在这种情况下，菜单中的第 N 个加载程序将是默认值。

  - “+”符号开头的字符串，表示最近启动的加载程序。

  - 任何与加载程序标题的一部分相对应的子字符串
  （通常是操作系统的名称、引导加载程序的路径，或者卷或文件系统的标题）。

- 你也可以指定多个选择器，用逗号分隔它们并用引号将列表括起来。

- （“+”选项仅在此上下文中有意义。）

- 如果您按照选择器两次，以 24 小时格式，默认将仅在这些时间之间应用。

- 时间是主板的时间标准，无论是UTC还是当地时间，所以如果你使用UTC，你需要手动从当地时间调整。

- 时间可能跨越午夜，如“23:30 00:30”，适用于晚上 11:30 到凌晨 12:30。

- 你可以指定多个 default_selection 行，在这种情况下，最后一个匹配的优先。

- 因此，您可以设置一个不带时间的主选项，后跟一个或多个包含时间的选项，
  以便为一天中的不同时间设置不同的默认值。

- 默认行为是启动先前(最后一次)启动的操作系统。

  - 例：

    ```refind conf
    default_selection 1
    default_selection Microsoft
    default_selection "+,bzImage,vmlinuz"
    default_selection Maintenance 23:30 2:00
    default_selection "Maintenance,macOS" 1:00 2:30
    ```

> [Top](##配置代码列表)



### enable_and_lock_vmx - 启用VMX位

- 启用 VMX 位，如果解锁则锁定 CPU MSR。

- 在某些 Intel Apple 计算机上，固件不会锁定 MSR 0x3A。

- Windows 上的症状是 Hyper-V 无法正常工作，即使 CPU 满足
  最低要求（硬件辅助虚拟化和 SLAT），请勿在支持 VMX 的 INTEL CPU 上设置此设置！ 

- 有关此主题的更多信息，请参阅 [此处](http://www.thomas-krenn.com/en/wiki/Activating_the_Intel_VT_Virtualization_Feature)。

- 默认为false：不要尝试启用和锁定MSR。

  - 例：

    ```refind conf
    enable_and_lock_vmx false
    ```

> [Top](##配置代码列表)



### spoof_osx_version - MacOS启动欺骗

- 告诉 Mac 的 EFI macOS 即将启动，即使它还没有启动。

- 此选项会导致某些 Mac 初始化其硬件的方式与正常启动第三方操作系统时不同。

- 在某些情况下（特别是在具有多个视频卡的 Mac 上），
  使用此选项可能会导致硬件正常工作，否则将无法正常工作。

- 另一方面，在没有必要时使用此选项可能会导致硬件（例如键盘和鼠标）变得不可访问。

- 因此，如果您的非 Apple 操作系统正常工作，
  则不应启用此选项； 仅当您对某些硬件设备有问题时才启用它。

- 需要时，“10.9”的值通常有效，但您可以尝试其他值。

- <font color=red>注意：此功能对非苹果电脑无效。</font>

- 默认为非活动状态（不进行 macOS 欺骗）。

  - 例：

    ```refind conf
    spoof_osx_version 10.9
    ```

> [Top](##配置代码列表)



### csr_values - 设置苹果csr值

- 设置 Apple 的系统完整性保护 (SIP) 功能的 CSR 值。

- 值是两字节（四个字符）的十六进制数。

- 这些值定义启用了哪些特定的安全功能。

- 下面是值含义的代码，将它们相加（十六进制）以设置新值。

- 参数列表：
  | 参数                                 | 值     |
  | ------------------------------------ | ------ |
  | CSR_ALLOW_UNTRUSTED_KEXTS            | 0x0001 |
  | CSR_ALLOW_UNRESTRICTED_FS            | 0x0002 |
  | CSR_ALLOW_TASK_FOR_PID               | 0x0004 |
  | CSR_ALLOW_KERNEL_DEBUGGER            | 0x0008 |
  | CSR_ALLOW_APPLE_INTERNAL             | 0x0010 |
  | CSR_ALLOW_UNRESTRICTED_DTRACE        | 0x0020 |
  | CSR_ALLOW_UNRESTRICTED_NVRAM         | 0x0040 |
  | CSR_ALLOW_DEVICE_CONFIGURATION       | 0x0080 |
  | CSR_ALLOW_ANY_RECOVERY_OS            | 0x0100 |
  | CSR_ALLOW_UNAPPROVED_KEXTS           | 0x0200 |
  | CSR_ALLOW_EXECUTABLE_POLICY_OVERRIDE | 0x0400 |
  | CSR_ALLOW_UNAUTHENTICATED_ROOT       | 0x0800 |

- Apple 的“csrutil enable”和“csrutil disable”命令分别设置值 10 和 877。

- 在 OS 11 之前，使用的是 77 而不是 877；OS 11 需要 877，并且应该也适用于 OS X 10.x。

  - 例：

    ```refind conf
    csr_values 10,877
    ```

> [Top](##配置代码列表)



### include - 引入配置文件

- 在这个文件中引入一个辅助配置文件。

- 这个辅助文件被加载，就好像它的选项出现在“包含”标记本身一样，

- 所以如果你想覆盖主文件中的设置，辅助文件必须在你想要覆盖的设置之后引用。

- <font color=red>请注意，辅助文件可能不会加载第三文件。</font>

  - 例：

    ```refind conf
    include manual.conf
    ```

> [Top](##配置代码列表)



### menuentry - 手动配置节点

- 每个都以“menuentry”关键字开头，后跟一个出现在菜单中的名称
- （如果您希望名称包含空格，请使用引号）和一个大括号（“{”），
- 每个条目都以大括号（“}”）结尾。
- 每个节中的常用关键字包括：
<table>
    <tr>
        <th>参数</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>volume</td>
        <td>
            标识从中加载后续文件的文件系统。您可以通过文件系统标签、
            <br />
            分区标签或分区 GUID 号（但还不能通过文件系统 UUID 号）指定卷。
        </td>
    </tr>
    <tr>
        <td>loader</td>
        <td>
            标识引导加载程序文件
        </td>
    </tr>
	<tr>
    	<td>initrd</td>
        <td>
            指定初始 RAM 磁盘文件
        </td>
    </tr>
	<tr><td>icon</td>
        <td>
            指定自定义引导加载程序图标
        </td>
    </tr>
	<tr>
        <td>ostype</td>
        <td>
            OS 类型代码以确定可用的引导选项，方法是按 Insert。
            <br />
            有效值为“MacOS”、“Linux”、“Windows”和“XOM”。 区分大小写。
        </td>
    </tr>
	<tr>
        <td>graphics</td>
        <td>
            设置为“on”以启用图形模式启动（主要用于 MacOS）或“off”用于文本模式启动。
            <br />
            默认是从加载器文件名中自动检测到的。
        </td>
    </tr>
	<tr>
        <td>options</td>
        <td>
            设置要传递给引导加载程序的选项； 
            <br />
            如果应该传递多个选项或任何选项使用可能
            <br />
            被 rEFInd 解析过程更改的字符（=、/、- 或制表符(tab)），请使用引号。
        </td>
    </tr>
	<tr>
        <td>disabled</td>
        <td>
            单独使用或设置为“是”以禁用此条目。
        </td>
    </tr>
</table>
- <font color=red>请注意，您可以使用 DOS/Windows/EFI 样式的反斜杠 (\) 或 Unix 样式的正斜杠 (/) 作为目录分隔符。</font>

- 无论哪种方式，所有文件引用都在启动 rEFInd 的 ESP 上。

- 在参数周围使用引号会导致它们被解释为一个关键字，并禁用特殊字符（空格、=、/ 和-）的解析。

- 这主要与“options”关键字一起使用。

- 在指定文件名的参数周围使用引号是允许的，但是您必须使用反斜杠而不是斜杠，
  除非您必须将正斜杠传递给加载程序，例如将 root= 选项传递给 Linux 内核。

> [Top](##配置代码列表)





 - ####  下面是几个示例引导节点配置

 - 默认全部禁用。

- 找到一个和你需要的相似的，复制它，
  去掉“disabled”那一行，然后调整条目以适应你的需要。

- 在 GUID 为 904404F8-B481-440C-A1E3-11A5A954E601 的分区上
  支持 EFI 引导存根的 Linux 3.13 内核的示例条目。

- 此条目包括特定于 Linux 的引导选项和初始 RAM 磁盘的规范。

- <font color=red>注意 Linux 风格的正斜杠的使用。</font>

- <font color=red>另请注意，文件规范中的前导斜杠是可选的。</font>

  ```refind conf
  menuentry Linux {
      icon EFI/refind/icons/os_linux.png
      volume 904404F8-B481-440C-A1E3-11A5A954E601
      loader bzImage-3.3.0-rc7
      initrd initrd-3.3.0.img
      options "ro root=UUID=5f96cafa-e0a7-4057-b18f-fa709db5b837"
      disabled
  }
  ```

> [Top](##配置代码列表)



- 下面是一个更复杂的 Linux 示例，专门针对 Arch Linux。

- 此示例必须针对您的特定安装进行修改； 如果不出意外，必须为您的磁盘更改 PARTUUID 代码。

- 因为 Arch Linux 在其内核和 initrd 文件名中不包含版本号，
  所以在使用备用 initrd 或多个带有 Arch 的内核时，您可能需要使用手动引导节。

- 这个例子是根据 [rEFInd](https://wiki.archlinux.org/index.php/rEFInd) 上的 Arch wiki 页面中的一个修改的。

  ```refind conf
  menuentry "Arch Linux" {
      icon     /EFI/refind/icons/os_arch.png
      volume   "Arch Linux"
      loader   /boot/vmlinuz-linux
      initrd   /boot/initramfs-linux.img
      options  "root=PARTUUID=5028fa50-0079-4c40-b240-abfaf28693ea rw add_efi_memmap"
      submenuentry "Boot using fallback initramfs" {
          initrd /boot/initramfs-linux-fallback.img
      }
      submenuentry "Boot to terminal" {
          add_options "systemd.unit=multi-user.target"
      }
      disabled
  }
  ```

> [Top](##配置代码列表)



- 使用其 GRUB 2 引导加载程序的标准名称加载 Ubuntu 的示例条目。

- <font color=red>注意 Linux 风格的正斜杠的使用。</font>

  ```refind conf
  menuentry Ubuntu {
      loader /EFI/ubuntu/grubx64.efi
      icon /EFI/refind/icons/os_linux.png
      disabled
  }
  ```


> [Top](##配置代码列表)



- 一个最简的 ELILO 条目，它可能没有提供任何自动检测无法完成的功能。

  ```refind conf
  menuentry "ELILO" {
      loader \EFI\elilo\elilo.efi
      disabled
  }
  ```

> [Top](##配置代码列表)




- 就像 ELILO 条目一样，这个条目没有提供任何自动检测不能做的事情； 

- 但如果您想禁用自动检测但仍启动 Windows，则可以使用它...

  ```refind conf
  menuentry "Windows 7" {
      loader \EFI\Microsoft\Boot\bootmgfw.efi
      disabled
  }
  ```


> [Top](##配置代码列表)




- EFI shell 是类似于引导加载程序的程序，并且可以以相同的方式启动。

- 你可以将要在“选项”行上运行的脚本的名称传递给 shell。

- 该脚本可以初始化硬件然后启动操作系统，或者它可以做一些完全不同的事情。

  ```refind conf
  menuentry "Windows via shell script" {
      icon \EFI\refind\icons\os_win.png
      loader \EFI\tools\shell.efi
      options "fs0:\EFI\tools\launch_windows.nsh"
      disabled
  }
  ```

> [Top](##配置代码列表)



- MacOS正常检测并自动运行； 但是，
  如果您想做一些不寻常的事情，手动引导节可能是一种方法。

- 这个并没有什么不寻常的地方，但它可以作为一个起点。

- <font color=red>请注意，您几乎肯定需要更改“volume”行才能使此示例正常工作。</font>

  ```refind conf
  menuentry "My macOS" {
      icon \EFI\refind\icons\os_mac.png
      volume "macOS boot"
      loader \System\Library\CoreServices\boot.efi
      disabled
  }
  ```

> [Top](##配置代码列表)



- firmware_bootnum 令牌采用 HEXADECIMAL 值作为选项，
  并使用 EFI 的 BootNext 变量设置该值，然后重新启动计算机。

- 这会导致使用此 EFI 引导选项一次性引导计算机。

- 它可以用于各种目的，但一些 rEFInd 用户可能会感兴趣的是，
  一些带有 HiDPI 显示器的 Mac 在通过 rEFInd 引导时产生的桌面分辨率低

- 于通过 Apple 自己的引导管理器引导时的桌面分辨率。

- 使用firmware_bootnum 选项引导会产生更好的分辨率。

- <font color=red>请注意，在这种类型的配置中没有使用加载器选项。</font>

  ```refind conf
  menuentry "macOS via BootNext" {
      icon /EFI/refind/icons/os_mac.png
      firmware_bootnum 80
      disabled
  }
  ```


> [Top](##配置代码列表)



### 捐赠



