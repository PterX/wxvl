#  安全热点周报：黑客利用 DoS 漏洞禁用 Palo Alto Networks 防火墙   
 奇安信 CERT   2024-12-30 09:05  
  
<table><tbody style="-webkit-tap-highlight-color: transparent;outline: 0px;visibility: visible;"><tr bgless="lighten" bglessp="20%" data-bglessp="40%" data-bgless="lighten" style="-webkit-tap-highlight-color: transparent;outline: 0px;border-bottom: 4px solid rgb(68, 117, 241);visibility: visible;"><th align="center" style="-webkit-tap-highlight-color: transparent;outline: 0px;word-break: break-all;hyphens: auto;border-width: 0px;border-style: none;border-color: initial;background-color: rgb(254, 254, 254);font-size: 20px;line-height: 1.2;visibility: visible;"><span style="-webkit-tap-highlight-color: transparent;outline: 0px;color: rgb(68, 117, 241);visibility: visible;"><strong style="-webkit-tap-highlight-color: transparent;outline: 0px;visibility: visible;"><span style="-webkit-tap-highlight-color: transparent;outline: 0px;font-size: 17px;visibility: visible;">安全资讯导视 </span></strong></span></th></tr><tr data-bcless="lighten" data-bclessp="40%" style="-webkit-tap-highlight-color: transparent;outline: 0px;border-bottom: 1px solid rgb(180, 184, 175);visibility: visible;"><td align="center" valign="middle" style="-webkit-tap-highlight-color: transparent;outline: 0px;word-break: break-all;hyphens: auto;border-width: 0px;border-style: none;border-color: initial;font-size: 14px;visibility: visible;"><p style="-webkit-tap-highlight-color: transparent;outline: 0px;visibility: visible;">• 国家金监总局发布《银行保险机构数据安全管理办法》</p></td></tr><tr data-bglessp="40%" data-bgless="lighten" data-bcless="lighten" data-bclessp="40%" style="-webkit-tap-highlight-color: transparent;outline: 0px;border-bottom: 1px solid rgb(180, 184, 175);visibility: visible;"><td align="center" valign="middle" style="-webkit-tap-highlight-color: transparent;outline: 0px;word-break: break-all;hyphens: auto;border-width: 0px;border-style: none;border-color: initial;font-size: 14px;visibility: visible;"><p style="-webkit-tap-highlight-color: transparent;outline: 0px;visibility: visible;">• 美国发布禁止敏感个人数据向中国跨境传输的最终规则</p></td></tr><tr data-bcless="lighten" data-bclessp="40%" style="-webkit-tap-highlight-color: transparent;outline: 0px;border-bottom: 1px solid rgb(180, 184, 175);visibility: visible;"><td align="center" valign="middle" style="-webkit-tap-highlight-color: transparent;outline: 0px;word-break: break-all;hyphens: auto;border-width: 0px;border-style: none;border-color: initial;font-size: 14px;visibility: visible;"><p style="-webkit-tap-highlight-color: transparent;outline: 0px;visibility: visible;">• 日本航空突遭网络攻击：航班延误 数小时后恢复</p></td></tr></tbody></table>  
  
**PART****0****1**  
  
  
**漏洞情报**  
  
  
**1.Adobe ColdFusion路径遍历漏洞安全风险通告**  
  
  
12月24日，奇安信CERT监测到官方修复Adobe ColdFusion 路径遍历漏洞(CVE-2024-53961)，Adobe ColdFusion 2023.11、2021.17 及更早版本存在路径遍历漏洞。未经身份验证的远程攻击者可以利用此漏洞访问应用程序设置的受限目录之外的文件或目录，从而导致敏感信息泄露或系统数据被操纵。鉴于此漏洞影响范围较大，建议客户尽快做好自查及防护。  
  
  
**PART****0****2**  
  
  
**新增在野利用**  
  
  
**1.****Palo Alto Networks PAN-OS 拒绝服务漏洞(CVE-2024-3393)**  
  
  
12月27日，Palo Alto Networks 警告称，黑客正在利用 CVE-2024-3393 拒绝服务漏洞，通过强制重启来禁用防火墙保护。然而，反复利用该安全问题会导致设备进入维护模式，需要人工干预才能恢复正常运行。  
  
公告中指出：“Palo Alto Networks PAN-OS 软件的 DNS 安全功能中存在拒绝服务漏洞，允许未经身份验证的攻击者通过防火墙的数据平面发送恶意数据包，从而重新启动防火墙。”Palo Alto Networks 表示，未经身份验证的攻击者可以通过向受影响的设备发送特制的恶意数据包来利用此漏洞。该问题仅影响启用“DNS 安全”日志记录的设备。  
  
该供应商确认该漏洞已被积极利用，并指出当防火墙阻止利用该漏洞的攻击者发送的恶意 DNS 数据包时，客户会遇到中断。  
  
该公司已解决 PAN-OS 10.1.14-h8、PAN-OS 10.2.10-h12、PAN-OS 11.1.5、PAN-OS 11.2.3 及后续版本中的漏洞。需要注意的是，受 CVE-2024-3393 影响的 PAN-OS 11.0 将不会收到补丁，因为该版本已于 11 月 17 日达到其生命周期终止 (EOL) 日期。  
  
   
  
参考链接：  
  
https://www.bleepingcomputer.com/news/security/hackers-exploit-dos-flaw-to-disable-palo-alto-networks-firewalls/  
  
**PART****0****3**  
  
  
**安全事件**  
  
  
**1.乌克兰国家政务数据库因网络攻击离线，众多公众基本服务全面中断**  
  
  
12月27日The Record消息，俄乌网络战持续激烈对抗，亲俄黑客组织XakNet发起了一次大规模网络攻击，导致乌克兰多个国家登记册下线，公民无法获取与其数字记录相关的基本服务。乌克兰司法部19日表示，网络基础设施出现大规模鼓掌，出于安全考虑暂停登记册访问。该部门管理的多个国家登记册因网络攻击离线，众多针对公众的基本公共服务无法使用，包括出生/婚姻/死亡登记、房产交易、征兵等在线服务，只能用纸质流程临时处理。攻击者声称删除了主备数据库，但官方表示拥有备份数据，保证称所有数据都会被恢复。  
  
  
原文链接：  
  
https://therecord.media/cyberattack-on-ukraine-state-register-disrupts-real-estate-marriages  
  
  
**2.日本航空突遭网络攻击：航班延误 数小时后恢复**  
  
  
12月26日证券时报消息，日本航空遭遇突发网络攻击。当地时间上午7时30分左右，连接该公司内部与外部的网络设备遭遇网络攻击，导致与外部通信的系统出现故障，飞行计划报告系统受影响。日本航空称，截至10时，受网络攻击影响，至少有9个日本国内航班出现延误，最长约1小时，预计影响范围可能会进一步扩大。截至14:30，官方称系统已恢复，国内国际机票销售已恢复正常。  
  
  
原文链接：  
  
https://mp.weixin.qq.com/s/AkXHszhzVvec3UQn8wTyQw  
  
  
**3.上万名村民个人信息被窃取，国家医保局严正声明**  
  
  
12月25日央视新闻消息，一些犯罪团伙盯上电子医保卡“村推”活动，将其变成了大肆套取群众个人信息的渠道。去年以来，河南有上万名农村老人在激活电子医保卡的过程中，被人私自开通了支付账号，并且这些支付账号都被倒卖给了网络赌博、洗钱等犯罪团伙，成为转账、洗钱工具。2023年6月至8月，公安机关奔赴全国多地，将这个团伙的成员抓捕归案。民警通过调取相关证据，发现该案中有近12000个公民信息被窃取。通过资金穿透，警方追查到以陈某丰、汤某为首的11名主要犯罪嫌疑人违法所得金额为380多万元。国家医保局于12月24日发表声明称，从未授权任何社会人员激活电子医保卡。请广大群众提高警惕，不要轻信陌生人以激活电子医保卡名义收集个人信息，谨防上当受骗。  
  
  
原文链接：  
  
https://mp.weixin.qq.com/s/Gd-tlUJeWS6cMNt8-cQiFw  
  
  
**4.因代运维政务数据库存在漏洞，浙江某软件厂商被罚款**  
  
  
12月24日浙江网警公众号消息，浙江台州公安机关工作中发现，浙江某软件科技公司受托搭建的数据库存在安全漏洞，数据库中承载的大量电子政务数据存在泄露风险。经查，该公司主要为政府部门提供软件开发、信息系统建设和运维等服务。在与台州当地部分政府部门合作期间，该公司未对受托维护、处理的电子政务数据履行应尽的数据安全保护义务，未依法建立全流程数据安全管理制度，导致电子政务数据存在严重泄露风险，相关行为违反了《中华人民共和国数据安全法》。台州公安机关依法对该公司和该公司负责人进行了行政罚款，并责令其依法依规履行数据安全保护义务。同时，依法约谈涉事政府部门相关负责人，通报委托处理电子政务数据活动中存在的安全问题，责令进一步加强数据安全管理和保护，严防数据泄露。  
  
  
原文链接：  
  
https://mp.weixin.qq.com/s/22z7W97zpu6tc73ZPAMLlw  
  
  
**5.英国人工智能公司Builder.ai云泄漏超1.29TB内部敏感数据**  
  
  
12月19日Silicon Angle消息，英国人工智能初创公司Builder.ai因云存储配置错误，导致1.29TB数据和超过300万条记录被曝光。该问题由安全研究员Jeremiah Fowler发现并由Website Planet披露。暴露的数据库包含个人敏感数据和公司运营数据，这可能对Builder.ai的客户以及内部运营构成风险。数据库中有300多万条记录，包含姓名、电子邮件地址、电话号码及实际地址等可识别个人身份的信息。数据库还记录了大量项目细节，包括正在进行和已完成的软件开发计划、客户互动记录及时间表。这些信息可能导致知识产权泄露，进而被恶意行为者或竞争对手利用。  
  
  
原文链接：  
  
https://siliconangle.com/2024/12/19/database-belonging-builder-ai-found-exposing-1-29tb-3m-records/  
  
  
**PART****0****4**  
  
  
**政策法规**  
  
  
**1.美国发布禁止敏感个人数据向中国跨境传输的最终规则**  
  
  
12月27日，美国司法部发布了“应对外国对手获取美国公民敏感个人数据”的最终规则。通过该规则，美国政府针对美国个人敏感数据向中国（包括香港和澳门）、古巴、伊朗、朝鲜、俄罗斯和委内瑞拉的跨境传输，设立了一个数据出境国家安全审查制度。该规则定义了六类美国人敏感数据和两类美国政府敏感数据，将禁止数据经纪公司与关注国进行敏感数据交易、限制与敏感数据相关的投资和合作协议、实施数据交易记录和审查机制。这标志着拜登政府今年2月发起的限制美国个人数据向中国跨境流动的联邦法规，在本届政府即将谢幕之际最终落地。该规定将在发布后 90 天生效，部分强制性合规义务将逐步实施，其生效日期为发布后 270 天。  
  
  
原文链接：  
  
https://www.justice.gov/opa/pr/justice-department-issues-final-rule-addressing-threat-posed-foreign-adversaries-access  
  
  
**2.国家金监总局发布《银行保险机构数据安全管理办法》**  
  
  
12月27日，国家金融监管总局发布《银行保险机构数据安全管理办法》。该文件共9章81条，包括总则、数据安全治理、数据分类分级、数据安全管理、数据安全技术保护、个人信息保护、数据安全风险监测与处置、监督管理、附则。该文件有五大主要特点，包括落实数据安全责任制、明确数据安全归口管理部门、将数据安全风险纳入全面风险管理体系、强化数据安全评估、建立数据安全保护基线。该文件要求银行保险机构应当建立与本机构业务发展目标相适应的数据安全治理体系，建立健全数据安全管理制度，构建覆盖数据全生命周期和应用场景的安全保护机制，开展数据安全风险评估、监测与处置，保障数据开发利用活动安全稳健开展。银行保险机构利用互联网等信息网络开展数据处理活动，应当在网络安全等级保护制度基础上，履行数据安全保护义务。  
  
  
原文链接：  
  
https://www.nfra.gov.cn/cn/view/pages/governmentDetail.html?docId=1192311&itemId=861&generaltype=1  
  
  
**3.工信部等三部门联合印发《制造业企业数字化转型实施指南》**  
  
  
12月25日，工业和信息化部、国务院国有资产监督管理委员会、中华全国工商业联合会等三部门联合印发《制造业企业数字化转型实施指南》。该文件专设一节，要求加强安全保障。包括健全工业企业网络安全管理制度，深入实施工业互联网安全分类分级管理，建立健全定级防护、评估评测、监测预警、信息通报、成效评价等工作机制，指导企业落实《工业控制系统网络安全防护指南》相关要求，开展重要工业控制系统识别认定，构建工控安全评估体系。督促企业落实《数据安全法》《工业和信息化领域数据安全管理办法（试行）》等法律政策要求，加强重要数据识别与备案，做好数据分类分级保护和安全风险评估，强化风险监测预警和应急处置能力，切实提升工业数据安全防护水平。  
  
  
原文链接：  
  
https://www.miit.gov.cn/cms_files/demo/pdfjs/web/viewer.html?file=/cms_files/filemanager/1226211233/attach/202412/3231769ba0884dadb5a9257e86f09442.pdf  
  
  
**4.国家数据局等五部门印发《关于促进企业数据资源开发利用的意见》**  
  
  
12月25日，国家数据局联合中央网信办、工业和信息化部、公安部、国务院国资委印发了《关于促进企业数据资源开发利用的意见》。该文件专设一节，要求提升数据安全合规治理效能。包括完善数据联管联治机制，强化部门协调和央地协同，推动包容审慎监管。针对新技术应用和新模式新业态，探索建立“沙盒监管”机制，构建鼓励创新、弹性包容的治理环境。健全政企沟通机制，稳定企业合规预期。推动制定行业数据分类分级标准，健全数据资源开发利用安全技术规范。健全数据安全管理、个人信息保护认证制度。强化行业自律建设，营造公平竞争、规范有序的市场环境。  
  
  
原文链接：  
  
https://mp.weixin.qq.com/s/JT-NM4NYssJ9K_aS5iMKuQ  
  
  
**5.联大通过《联合国打击网络犯罪公约》**  
  
  
12月24日，联合国大会以一致同意的方式通过具有法律约束力的《联合国打击网络犯罪公约》，旨在加强国际合作，预防和打击网络犯罪。联合国秘书长古特雷斯指出，这是20多年来经谈判达成的首个国际刑事司法条约，反映了会员国加强国际合作以预防和打击网络犯罪的集体意愿。该公约承认滥用信息和通信技术所带来的重大风险，认为这些技术使犯罪活动的规模、速度和范围达到前所未有的程度；强调网络犯罪可能对国家、企业、个人和社会福祉造成不利影响；认识到网络犯罪对受害者的影响日益加大，主张为弱势群体伸张正义；强调技术援助、能力建设以及各国和其他利益攸关方之间合作的必要性。公约将于2025年在越南首都河内举行的正式仪式上开放签署，并将在第40个签署国批准后90天生效。  
  
  
原文链接：  
  
https://content-static.cctvnews.cctv.com/snow-book/index.html?item_id=8320959904326981469  
  
  
**6.韩国发布人工智能隐私风险管理模型**  
  
  
12 月 19 日，韩国个人信息保护委员会发布《安全利用人工智能和数据的人工智能隐私风险管理模型》，为人工智能领域的隐私风险管理提供了重要的指导框架，旨在帮助人工智能企业根据人工智能技术的多样化特点及其具体应用场景，采取自主措施有效识别和应对隐私风险。据悉，该模型系统地梳理了人工智能全生命周期中的隐私风险管理方向、基本原则、风险类型及其对应的缓解措施，旨在应对人工智能技术发展、个人数据泄露以及新兴风险不断增加的挑战。  
  
  
原文链接：  
  
https://www.pipc.go.kr/np/cop/bbs/selectBoardArticle.do?bbsId=BS074&mCode=C020010000&nttId=10870  
  
  
**往期精彩推荐**  
  
  
[Adobe ColdFusion 路径遍历漏洞(CVE-2024-53961)安全风险通告](https://mp.weixin.qq.com/s?__biz=MzU5NDgxODU1MQ==&mid=2247502682&idx=1&sn=83e2cebbdeddd336724d291651d2bc51&token=133028405&lang=zh_CN&scene=21#wechat_redirect)  
[安全热点周报：Windows 内核漏洞现被利用来获取系统权限](https://mp.weixin.qq.com/s?__biz=MzU5NDgxODU1MQ==&mid=2247502670&idx=1&sn=479d015990e5c63cf38d46824cc7a6d5&token=133028405&lang=zh_CN&scene=21#wechat_redirect)  
  
[【已复现】Apache Tomcat 远程代码执行漏洞(CVE-2024-56337)安全风险通告](https://mp.weixin.qq.com/s?__biz=MzU5NDgxODU1MQ==&mid=2247502658&idx=1&sn=e1de6decc572e58a32c667c1ecd2ec0b&token=133028405&lang=zh_CN&scene=21#wechat_redirect)  
  
  
  
  
本期周报内容由安全内参&虎符智库&奇安信CERT联合出品！  
  
  
  
  
  
  
  
  
