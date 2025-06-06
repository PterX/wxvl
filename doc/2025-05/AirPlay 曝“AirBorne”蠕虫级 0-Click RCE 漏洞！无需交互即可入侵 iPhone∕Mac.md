#  AirPlay 曝“AirBorne”蠕虫级 0-Click RCE 漏洞！无需交互即可入侵 iPhone/Mac   
原创 Hankzheng  技术修道场   2025-05-07 00:53  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_png/wWBwsDOJT4ic1pMvZT4oS46tMXyGGD2c1whPxPJcbQOcDZrgavdl31WgiaWgPv7TYIQPIHrGHyo2bKA6BrqYcWxQ/640?wx_fmt=png&from=appmsg "")  
  
紧急安全警报！如果您是苹果用户或使用任何支持苹果 AirPlay 无线投屏/音频流技术的设备，请务必关注：以色列网络安全公司 Oligo 近日披露了 AirPlay 协议中存在的一组被命名为 **“AirBorne”**  
 的严重安全漏洞。这些漏洞（现已被苹果修复）的影响范围极广，涵盖 iPhone、iPad、Mac、Apple TV、visionOS 以及大量使用了 AirPlay SDK 的第三方智能音箱、电视等设备。最危险的是，这些漏洞可被串联利用，实现**无需用户任何交互的“零点击”远程代码执行 (Zero-Click RCE)**  
，甚至具备**蠕虫般的自我传播能力**  
！  
  
**核心威胁解读：零点击 + 蠕虫 = 极端危险**  
  
AirBorne 漏洞的严重性体现在以下几个层面：  
1. **零点击远程代码执行 (Zero-Click RCE)**  
这是网络攻击的“王炸”。与需要诱骗用户点击链接或打开附件的传统攻击不同，零点击意味着攻击者**仅需与目标设备处于同一网络环境（如同一 Wi-Fi 下）**  
，无需受害者执行任何操作，即可远程注入并执行恶意代码，完全控制设备。其隐蔽性和成功率远超常规攻击。  
  
1. **蠕虫级自我传播 (Wormable)**  
研究表明，通过组合 **CVE-2025-24252**  
 和关键的   
CVE-2025-24132（栈溢出）漏洞，攻击者可以构建出具备蠕虫特性的恶意软件。这意味着：  
  
1. **自动扩散**  
一台设备被 AirBorne 漏洞感染后，当它接入**任何新的本地网络**  
（家庭、办公室、咖啡馆 Wi-Fi 等）时，它可能会**主动利用 mDNS/Bonjour 等协议发现**  
网络中其他开启 AirPlay 且存在漏洞的设备，并**自动发送利用代码尝试感染它们**  
。  
  
1. **指数级增长**  
这种自我复制能力使得攻击可以迅速、无声地在网络中蔓延，可能导致大规模设备沦陷，为部署勒索软件、组建僵尸网络或进行长期潜伏的 APT 攻击提供了绝佳途径。  
  
1. **公共 Wi-Fi 成高风险入口**  
用户设备在连接安全性未知的**公共 Wi-Fi**  
 时，最易成为 AirBorne 攻击的初始目标。一旦设备被感染，后续接入**企业内网或家庭网络**  
时，就可能充当“跳板”，将威胁引入原本相对安全的环境。  
  
**关键漏洞技术深度剖析：**  
  
AirBorne 漏洞集涉及多种底层缺陷。以下是其中最关键的几个：  
- **RCE 类漏洞 (最高危)**  
:  
  
- **CVE-2025-24132**  
存在于 **AirPlay SDK**  
（被广泛用于第三方设备）中的**基于栈的缓冲区溢出**  
漏洞。**【技术原理】**  
：栈是程序内存中用于存储函数局部变量和返回地址等信息的地方。攻击者通过发送精心构造的超长 AirPlay 数据，可以覆盖（淹没）栈上预留的缓冲区，并**精确地改写函数执行完毕后本应返回的地址，使其指向攻击者预先植入的恶意代码 (Shellcode)**  
。一旦被覆盖的函数返回，程序就会跳转执行恶意代码，导致 RCE。这是实现蠕虫传播和入侵第三方设备的关键。  
  
- **CVE-2025-24252 & CVE-2025-24206 组合**  
可在 **macOS**  
 上实现 0-Click RCE。其中 **CVE-2025-24206**  
 是**认证绕过**  
漏洞。**【利用条件】**  
：攻击者需与目标 Mac 处于同一网络，且该 Mac 的 AirPlay 接收器功能**已开启并设置为允许“同一网络上的任何人”或“所有人”连接**  
。**【风险提示】**  
：这两种宽松的 AirPlay 配置虽然方便共享，但在不受信任的网络环境中**极大增加了被攻击的风险**  
。建议用户仅在需要时开启 AirPlay 接收器，并优先选用更严格的访问权限设置（如“仅当前用户”或要求密码）。  
  
- **CVE-2025-24137**  
可直接导致任意代码执行或应用程序终止。  
  
- **Bypass 类漏洞 (辅助攻击)**  
:  
  
- **CVE-2025-24271**  
**访问控制列表 (ACL) 绕过**  
漏洞。允许同网攻击者在 Mac 已登录状态下，**无需配对即可向其发送 AirPlay 控制命令**  
。这可能被用于**信息刺探、干扰正常使用，甚至可能作为跳板触发其他漏洞**  
。  
  
- **CVE-2025-24206**  
已提及的**认证绕过**  
漏洞，用于 macOS RCE 链。  
  
- **信息泄露与 DoS 类漏洞**  
:  
  
- **CVE-2025-24270**  
可导致本地网络攻击者**泄露敏感用户信息**  
。  
  
- **CVE-2025-24251, CVE-2025-31197, CVE-2025-30445 (类型混淆), CVE-2025-31203 (整数溢出)**  
 等多个漏洞可被本地网络攻击者利用，导致 AirPlay 相关应用**意外终止或拒绝服务 (DoS)**  
。  
  
**补丁已发布！立即更新是关键！**  
  
值得庆幸的是，Oligo 公司遵循了**负责任披露 (Responsible Disclosure)**  
 原则，在公开前已将漏洞细节提交给苹果公司，使其有时间开发和发布补丁。苹果已在近期推送的软件更新中修复了 AirBorne 系列漏洞。请务必确保您的苹果设备已更新至以下**或更高版本**  
：  
- **iOS 18.4**  
- **iPadOS 18.4 / iPadOS 17.7.6**  
- **macOS Sequoia 15.4**  
- **macOS Sonoma 14.7.5**  
- **macOS Ventura 13.7.5**  
- **tvOS 18.4**  
- **visionOS 2.4**  
**对于使用 AirPlay SDK 的第三方设备（智能音箱、电视等）：**  
- 苹果已向开发者发布了修复后的 SDK 版本：**AirPlay 音频 SDK 2.7.1**  
, **AirPlay 视频 SDK 3.6.0.126**  
, **CarPlay 通信插件 R18.1**  
。  
  
- **用户需要关注并安装来自相应设备制造商（如 Sonos, Bose, LG, Samsung 等）发布的固件更新**  
请检查您设备的更新设置或访问制造商官网获取信息。**第三方设备的更新速度可能滞后于苹果官方，这是潜在的风险窗口期。**  
  
**安全建议：更新为主，防御为辅**  
  
面对 AirBorne 这种级别的威胁，**及时安装安全更新是首要且最有效的防御手段**  
。Oligo 公司强烈建议：  
1. **立即更新所有设备**  
无论是**公司配发的还是个人拥有**  
的、所有支持 AirPlay 的苹果设备及第三方设备，都应**第一时间更新**  
到已修复漏洞的最新版本。企业应确保员工了解并执行个人设备的更新。  
  
1. **审视 AirPlay 配置**  
检查 Mac、Apple TV 等设备的 AirPlay 接收设置，**避免在不需要时使用“任何人”或“所有人”的宽松配置**  
，尤其是在连接公共或访客网络时。  
  
1. **辅助防御措施**  
虽然无法完全替代补丁，但在无法立即更新或作为纵深防御的一部分，可以考虑：  
  
1. **在不需要时彻底关闭设备的 AirPlay 接收功能。**  
1. 在企业环境中，通过**网络分段**  
将支持 AirPlay 的设备（尤其是不易管理的第三方设备或 BYOD 设备）隔离在独立的网络区域，限制潜在蠕虫的传播范围。  
  
**正视 0-Click 威胁，安全更新刻不容缓**  
  
AirBorne 漏洞的发现再次敲响了警钟：看似便捷的无线协议背后可能隐藏着致命的安全缺陷。零点击和蠕虫传播能力将此类漏洞的危险性提升到了极点。请不要抱有侥幸心理，立即行动，检查并更新您身边所有可能受影响的设备。在数字世界中，保持警惕和及时响应是维护安全的基石。  
  
