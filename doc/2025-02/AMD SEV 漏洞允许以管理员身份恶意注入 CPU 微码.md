#  AMD SEV 漏洞允许以管理员身份恶意注入 CPU 微码   
 汇能云安全   2025-02-06 02:34  
  
![](https://mmbiz.qpic.cn/mmbiz_jpg/NSXvotEG4JwA6iae234BZTcVibeERibUSXzttuenqy0uqXaibgAMn7OYStWpYibu9FtY50n2OM56ic8s2MkedCnvqOCQ/640?wx_fmt=jpeg&from=appmsg "")  
  
**2****月****6****日，星期四****，您好！中科汇能与您分享信息安全快讯：**  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/NSXvotEG4JyBOe54aTWQ1mrh5EWP9lYoQ3n95XuYHfs0Oa38HhqbBYUj92WFPlDhzu6uznL5nvwwRr5t5y2iaCw/640?wx_fmt=gif&from=appmsg "")  
  
**01**  
  
  
**PlushDaemon APT 在供应链攻击中以韩国 VPN 提供商为目标**  
  
  
根据 ESET 的新调查结果，一个以前未记录的与中国结盟的高级持续威胁 （APT） 组织 PlushDaemon 与 2023 年针对韩国虚拟专用网络 （VPN） 提供商的供应链攻击有关。  
  
“攻击者用一个还部署了该组织的签名植入物的安装程序替换了合法的安装程序，我们将其命名为 SlowStepper——一个功能丰富的后门，带有一个包含 30 多个组件的工具包，”ESET 研究员 Facundo Muñoz 在与 The Hacker News 分享的技术报告中说。  
  
PlushDaemon 被评估为一个与中国有联系的团体，至少自 2019 年以来一直在运营，针对中国大陆、台湾、香港、韩国、美国和新西兰的个人和实体。  
  
其操作的核心是一个名为 SlowStepper 的定制后门，它被描述为一个由大约 30 个模块组成的大型工具包，使用 C++、Python 和 Go 编程。  
  
其攻击的另一个关键方面是劫持合法的软件更新渠道和利用 Web 服务器中的漏洞来获得对目标网络的初始访问权限。  
  
**这家斯洛伐克网络安全公司表示，它在 2024 年 5 月注意到 Windows 的 NSIS 安装程序中嵌入了恶意代码，这些代码是从名为 IPany 的 VPN 软件提供商的网站下载的（“ipany[.]kr/download/IPanyVPNsetup.zip”）。**  
  
**安装程序的流氓版本已从网站上删除，旨在删除合法软件以及 SlowStepper 后门。目前尚不清楚供应链攻击的确切目标是谁，尽管任何下载诱杀 ZIP 档案的个人或实体都可能面临风险。**  
  
ESET 收集的遥测数据显示，多个用户试图在与韩国的一家半导体公司和一家身份不明的软件开发公司相关的网络中安装特洛伊木马软件。2023 年 11 月和 12 月记录到的最年长的受害者分别来自日本和嘉。  
  
攻击链从安装程序（“IPanyVPNsetup.exe”）的执行开始，安装程序在两次重启之间继续在主机上建立持久性，并启动一个加载程序（“AutoMsg.dll”），该加载程序反过来负责运行加载另一个 DLL （“EncMgr.pkg”） 的 shellcode。  
  
ESET 表示，它还在远程代码存储库中发现了几个用 Golang 编写的软件程序，这些程序提供反向代理和下载功能。  
  
Muñoz 说：“这个后门以其使用 DNS 的多级 C&C 协议以及下载和执行数十个具有间谍功能的其他 Python 模块的能力而著称。  
  
“PlushDaemon 工具集中的众多组件及其丰富的版本历史记录表明，虽然以前不为人知，但这个与中国结盟的 APT 组织一直在努力开发各种工具，使其成为值得关注的重大威胁。”  
  
**02**  
  
**Oracle 发布 2025 年 1 月补丁以解决主要产品中的 318 个缺陷**  
  
  
Oracle 敦促客户应用其 2025 年 1 月的关键补丁更新 （CPU） 来解决其产品和服务中的 318 个新安全漏洞。  
  
最严重的缺陷是 Oracle Agile Product Lifecycle Management （PLM） 框架中的一个错误（CVE-2025-21556，CVSS 评分：9.9），该漏洞可能允许攻击者控制易受攻击的实例。  
  
“易于利用的漏洞允许低权限攻击者通过 HTTP 进行网络访问，从而破坏 Oracle Agile PLM Framework，”根据 NIST 国家漏洞数据库 （NVD） 中对安全漏洞的描述。  
  
值得注意的是，Oracle 在 2024 年 11 月警告称，有人会主动尝试利用同一产品中的另一个缺陷（CVE-2024-21287，CVSS 评分：7.5）。这两个漏洞都影响 Oracle Agile PLM Framework 版本 9.3.6。  
  
甲骨文公司安全保障副总裁 Eric Maurice 表示：“强烈建议客户应用 2025 年 1 月的 Oracle Agile PLM Framework 关键补丁更新，因为它包括 [CVE-2024-21287] 补丁以及其他补丁。  
  
CVE-2025-21535 也类似于 CVE-2020-2883（CVSS 评分：9.8），后者是 Oracle WebLogic Server 中的另一个关键安全漏洞，未经身份验证的攻击者可能会利用该漏洞通过 IIOP 或 T3 进行网络访问。  
  
本**月早些时候，美国网络安全和基础设施安全局 （CISA） 将 CVE-2020-2883 添加到其已知利用漏洞 （KEV） 目录中，并引用了在野外积极利用的证据。**  
  
**Oracle 还解决了 CVE-2024-37371（CVSS 分数：9.1），这是一个关键的 Kerberos 5 缺陷，影响其通信计费和收入管理，可能允许攻击者“通过发送具有无效长度字段的消息令牌来造成无效的内存读取”。**  
  
建议用户应用必要的补丁，以保持其系统为最新版本并避免潜在的安全风险。  
  
**03**  
  
**AMD SEV 漏洞允许以管理员身份恶意注入 CPU 微码**  
  
  
**AMD 在其安全加密虚拟化 （SEV） 技术中披露了一个高严重性漏洞 （CVE-2024-56161），该漏洞可能允许具有管理权限的攻击者注入恶意 CPU 微码。**  
  
**此缺陷损害了受 SEV-SNP 保护的虚拟机 （VM） 的机密性和完整性，SEV-SNP 是一种旨在保护虚拟化环境中敏感工作负载的安全功能。**  
  
此问题源于 AMD CPU ROM 微码补丁加载程序中的签名验证不正确。  
  
具体来说，用于验证微码更新的不安全哈希函数使具有本地管理员权限的攻击者能够绕过签名检查并加载未经授权的微码。  
  
“AMD CPU ROM 微码补丁加载程序中不正确的签名验证可能允许具有本地管理员权限的攻击者加载恶意 CPU 微码，从而导致在 AMD SEV-SNP 下运行的机密客户机的机密性和可靠性丧失”，公告中写道。  
  
AMD SEV-SNP（安全嵌套分页）是一项高级安全功能，旨在将虚拟机与虚拟机监控程序隔离，并防止内存重新映射和侧信道攻击。  
  
通过使用唯一密钥加密 VM 内存并实施内存完整性检查，SEV-SNP 为敏感数据处理创建了可信的执行环境。  
  
但是，CVE-2024-56161 允许恶意微码纵 CPU 功能，从而可能暴露加密的 VM 数据或启用权限提升，从而破坏了这些保护措施。  
  
此缺陷影响多代 AMD 处理器，包括 Zen 1 到 Zen 4 架构，这些架构为全球数据中心使用的 EPYC™ 服务器 CPU 提供支持。  
  
它的 CVSS 得分为 7.2（高），反映了它对机密计算工作负载的重大潜在影响。  
  
AMD 感谢 Google 研究人员 Josh Eads、Kristoffer Janke、Eduardo Vela Nava、Tavis Ormandy 和 Matteo Rizzo 发现了这一关键缺陷。  
  
AMD 已通过其 AGESA™ 平台初始化包发布了固件更新以解决该问题。  
  
**04**  
  
**朝鲜黑客通过 macOS 上的虚假求职面试部署 FERRET 恶意软件**  
  
  
据观察，传染性面试活动背后的朝鲜威胁行为者提供了一组名为 FERRET 的 Apple macOS 恶意软件菌株，作为所谓的求职面试过程的一部分。  
  
**“通常要求目标通过一个链接与面试官进行交流，该链接会引发错误消息，并要求安装或更新一些所需的软件，例如 VCam 或 CameraAccess，用于虚拟会议，”SentinelOne 研究人员 Phil Stokes 和 Tom Hegel 在一份新报告中说。**  
  
传染性访谈于 2023 年底首次被发现，是黑客团队持续进行的一项努力，通过伪造的 npm 包和伪装成视频会议软件的原生应用程序向潜在目标提供恶意软件。它也被跟踪为 DeceptiveDevelopment 和 DEV#POPPER。  
  
这些攻击链旨在丢弃一种称为 BeaverTail 的基于 JavaScript 的恶意软件，该恶意软件除了从 Web 浏览器和加密钱包收集敏感数据外，还能够提供名为 InvisibleFerret 的 Python 后门。  
  
2024 年 12 月，日本网络安全公司 NTT Security Holdings 透露，JavaScript 恶意软件也被配置为获取和执行另一种称为 OtterCookie 的恶意软件。  
  
FERRET 恶意软件家族的发现于 2024 年底首次被发现，这表明威胁行为者正在积极磨练他们的策略以逃避检测。  
  
这包括采用 ClickFix 风格的方法来诱骗用户通过终端应用程序在其 Apple macOS 系统上复制和执行恶意命令，以解决通过 Web 浏览器访问摄像头和麦克风的问题。  
  
根据用户名为 @tayvano_ 的安全研究员 Taylor Monahan 的说法，这些攻击起源于攻击者通过冒充招募人员并敦促他们完成视频评估来接近 LinkedIn 上的目标。最终目标是放置一个基于 Golang 的后门和窃取程序，该程序旨在耗尽受害者的 MetaMask 钱包并在主机上运行命令。  
  
斯托克斯说，虽然 FlexibleFerret 样本以 Apple 安装程序包的形式提供，但目前尚不清楚采用了什么诱饵技术来诱使目标运行恶意软件。也就是说，有证据表明，该恶意软件是通过在合法的 GitHub 存储库上打开虚假问题来传播的，这再次表明其攻击方法的多样化。  
  
研究人员说：“这表明威胁行为者乐于将他们传播恶意软件的媒介扩展到更普遍的开发人员的特定目标之外。  
  
在披露这一消息的几天前，供应链安全公司 Socket 详细介绍了一个名为 postcss-optimizer 的恶意 npm 包，其中包含 BeaverTail 恶意软件。在撰写本文时，该库仍可从 npm 注册表下载。  
  
“通过冒充下载量超过 160 亿次的合法 postcss 库，威胁行为者旨在通过跨 Windows、macOS 和 Linux 系统的凭据窃取和数据泄露功能感染开发人员的系统，”安全研究人员 Kirill Boychenko 和 Peter van der Zee 说。  
  
该发展还是在发现与朝鲜结盟的 APT37（又名 ScarCruft）威胁行为者发起的一项新活动之后进行的，该活动涉及通过鱼叉式网络钓鱼活动分发诱杀文件，以部署 RokRAT 恶意软件，并通过 K Messenger 平台通过群聊将它们传播给其他目标来自受感染用户的计算机。  
  
**05**  
  
**恶意 Go 程序包利用模块镜像缓存进行持久远程访问**  
  
  
**网络安全研究人员提请注意针对 Go 生态系统的软件供应链攻击，该攻击涉及一个恶意包，该包能够让对手远程访问受感染的系统。**  
  
**该软件包名为 github.com/boltdb-go/bolt，是每个 Socket 的合法 BoltDB 数据库模块 （github.com/boltdb/bolt） 的拼写错误。恶意版本 （1.3.1） 于 2021 年 11 月发布到 GitHub，随后由 Go Module Mirror 服务无限期缓存。**  
  
“安装后门包后，威胁行为者可以远程访问受感染的系统，允许他们执行任意命令，”安全研究员 Kirill Boychenko 在一份分析中说。  
  
Socket 表示，这一发展标志着恶意行为者滥用 Go Module Mirror 的无限期模块缓存来诱骗用户下载该包的最早实例之一。随后，据说攻击者修改了源存储库中的 Git 标记，以便将它们重定向到良性版本。  
  
在与 The Hacker News 分享的一份声明中，该公司指出，更改是在 GitHub 存储库中进行的，该存储库是合法 BoltDB 工具的分叉版本，威胁行为者在其中重写了 v1.3.1 的 Git 标签，以指向干净的提交，而不是原始的恶意版本。  
  
“这是可能的，因为除非明确保护，否则 Git 标签是可变的，”Socket 说。“仓库所有者可以随时删除标签并将其重新分配给不同的提交。但是，Go Module Proxy 已经缓存了原始恶意版本，该版本从未更新或从代理中删除，从而允许攻击持续存在。  
  
这种欺骗性方法确保了对 GitHub 存储库的手动审计不会发现任何恶意内容，而缓存机制意味着毫无戒心的开发人员使用 go CLI 安装包会继续下载后门变体。  
  
“一旦模块版本被缓存，即使后来修改了原始源，它仍然可以通过 Go Module Proxy 访问，”Boychenko 说。“虽然这种设计有利于合法用例，但威胁行为者利用它来持续分发恶意代码，尽管随后对存储库进行了更改。”  
  
“由于不可变模块既提供安全优势又提供潜在的滥用媒介，开发人员和安全团队应该监控利用缓存模块版本逃避检测的攻击。”  
  
在开发过程中，Cycode 详细介绍了三个恶意 npm 包——serve-static-corell、openssl-node 和 next-refresh-token——它们包含混淆代码，用于收集系统元数据并运行远程服务器发出的任意命令（“8.152.163[.]60“） 的 60 英寸。  
  
**06**  
  
**微软宣布停止支持Microsoft Defender应用中的隐私保护VPN功能**  
  
  
微软近日通知用户，将于 2025 年2 月28 日停止对 Microsoft Defender 应用中的隐私保护 VPN 功能的支持。该功能的移除并不影响设备的其他保护措施，包括恶意软件扫描、身份盗窃监测和信用监测等，这些服务仍将继续提供，尤其是在美国市场。Microsoft Defender 能够检查下载和安装的文件或应用程序是否存在恶意软件，并对系统中已有文件进行扫描，此外，它还可以与第三方反恶意软件解决方案协同工作。  
  
**微软表示，取消 VPN 功能的决定旨在使公司能够投资于更符合客户需求的新领域。尽管更新文档未提供详细信息，但强调了公司定期评估功能有效性的做法。对于 Windows 、iOS 和macOS 用户而言，此次变更无需采取任何行动。然而，Android 用户需要手动移除 Defender VPN 配置文件，以确保设备的正常使用。**  
  
微软建议，尽管不移除 Defender VPN 配置文件不会对设备产生影响，但为了避免不必要的困扰，建议用户将其删除。具体操作步骤如下：打开设置应用，搜索“VPN”，如果用户曾启用隐私保护，列表中将显示“Microsoft Defender” VPN 配置文件。用户只需点击“信息”图标并移除该配置文件即可。  
  
此举反映了微软在网络安全领域的持续调整与优化，以更好地满足用户的需求和市场变化。  
  
**07**  
  
**俄罗斯网络犯罪集团利用 7 拉链漏洞绕过 Windows MotW 保护**  
  
  
最近修补的 7-Zip 存档工具中的安全漏洞被在野外利用来传播 SmokeLoader 恶意软件。  
  
该漏洞 CVE-2025-0411（CVSS 评分：7.0）允许远程攻击者绕过 mark-of-the-web （MotW） 保护，并在当前用户的上下文中执行任意代码。7-Zip 于 2024 年 11 月在 24.09 版中解决了这个问题。  
  
**“俄罗斯网络犯罪集团通过鱼叉式网络钓鱼活动积极利用该漏洞，使用同形文字攻击来欺骗文档扩展名并诱骗用户和 Windows作系统执行恶意文件，”趋势科技安全研究员 Peter Girnus 说。**  
  
**据怀疑，CVE-2025-0411 可能被武器化，以乌克兰的政府和非政府组织为目标，作为在持续的俄乌冲突背景下开展的网络间谍活动的一部分。**  
  
MotW 是 Microsoft 在 Windows 中实施的一项安全功能，用于防止自动执行从 Internet 下载的文件，而无需通过 Microsoft Defender SmartScreen 执行进一步检查。  
  
CVE-2025-0411 通过使用 7-Zip 对内容进行双重归档来绕过 MotW，即先创建一个归档，然后再创建一个归档，以隐藏恶意负载。  
  
“CVE-2025-0411 的根本原因是，在 24.09 版本之前，7-Zip 没有正确地将 MotW 保护传播到双重封装档案的内容，”Girnus 解释说。“这允许威胁行为者制作包含恶意脚本或可执行文件的档案，这些脚本或可执行文件不会受到 MotW 保护，使 Windows 用户容易受到攻击。”  
  
利用该漏洞作为零日漏洞的攻击于 2024 年 9 月 25 日首次在野外检测到，感染序列导致 SmokeLoader，这是一种被反复用于针对乌克兰的加载程序恶意软件。  
  
首先是一封网络钓鱼电子邮件，其中包含一个特制的存档文件，该文件反过来利用同形文字攻击将内部 ZIP 存档作为 Microsoft Word 文档文件传递，从而有效地触发该漏洞。  
  
根据 Trend Micro 的说法，网络钓鱼消息是从与乌克兰管理机构和企业账户相关的电子邮件地址发送到市政组织和企业，这表明之前存在泄露。  
  
“使用这些受感染的电子邮件帐户为发送给目标的电子邮件增添了真实性，纵潜在受害者信任内容及其发件人，”Girnus 指出。  
  
此方法会导致执行 Internet 快捷方式 （.URL） 文件，这指向攻击者控制的服务器托管另一个 ZIP 文件。新下载的 ZIP 包含伪装成 PDF 文档的 SmokeLoader 可执行文件。  
  
至少有 9 个乌克兰政府实体和其他组织被评估为受到该活动的影响，包括司法部、基辅公共交通服务、基辅供水公司和市议会。  
  
“这些组织通常承受着巨大的网络压力，但往往被忽视，对网络的了解较少，并且缺乏大型政府组织所拥有的全面网络战略的资源。这些较小的组织可以成为威胁行为者转向大型政府组织的宝贵支点。  
  
**08**  
  
  
**ValleyRAT 使用新的交付技术攻击 Org 的会计部门**  
  
  
研究人员在最近的网络安全警报中揭示了一种复杂的恶意软件活动，该警报涉及 ValleyRAT，这是一种远程访问木马 （RAT），经常与 Silver Fox APT 组织相关联。  
  
这种威胁随着新的交付技术而演变，针对组织内的关键角色，尤其是财务和会计部门。  
  
攻击者利用合法软件中的漏洞，并使用高级策略来逃避检测。  
  
ValleyRAT 是一种基于 C++ 的 RAT，它提供基本 RAT 的典型功能，包括捕获输入和注入作。  
  
Morphisec Labs 分析师指出，它挂接了 、 等功能，并绕过了 AMSI 和 ETW 等安全机制，使其保持不被发现。  
  
**当用户从网络钓鱼网站（例如 ）下载虚假的 Chrome 浏览器时，感染就开始了。另一个网络钓鱼网站 冒充一家名为“Karlos”的中国电信公司。用户被诱骗下载一个包含 的文件，该文件在执行时请求管理员权限。ValleyRAT 通过在“Software\Microsoft\Windows\CurrentVersion\Run”下添加注册表项来实现持久性。它还检查 VMware 环境以逃避虚拟机中的检测。**如果未在 VM 中运行，它将尝试连接到 以进行网络通信检查。ValleyRAT 在其代码中初始化 C2 IP 地址和端口。命令包括插件清理、进程列表检索和执行 DLL。  
  
为了防范 ValleyRAT，组织应采用主动的网络安全措施，通过防止利用而不是仅仅依赖检测来帮助在早期阶段阻止攻击。  
  
组织必须保持警惕并调整其防御措施来应对复杂的恶意软件攻击。  
  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/NSXvotEG4JyBOe54aTWQ1mrh5EWP9lYoHzbQHfNHSU62zp3ZjTTgm1VicL7VTMwan7mLsv1SiaBzG6Mw67rpF5dQ/640?wx_fmt=gif&from=appmsg "")  
  
信息来源：人民网 国家计算机网络应急技术处理协调中心 国家信息安全漏洞库 今日头条 360威胁情报中心 中科汇能GT攻防实验室 安全牛 E安全 安全客 NOSEC安全讯息平台 火绒安全 亚信安全 奇安信威胁情报中心 MACFEESy mantec白帽汇安全研究院 安全帮  卡巴斯基 安全内参 安全学习那些事 安全圈 黑客新闻 蚁景网安实验室 IT之家IT资讯 黑客新闻国外 天际友盟  
  
![](https://mmbiz.qpic.cn/mmbiz_png/NSXvotEG4Jy8LNPtUFy94c9CGG0ASQqK4WcEDppBOWoymg5KyMOPPy14tftLVEgIibMlwuvsTjffaicjlVtficB2A/640?wx_fmt=png "")  
  
本文版权归原作者所有，如有侵权请联系我们及时删除  
  
