#  CNNVD | 关于Fortinet多款产品安全漏洞的通报   
 中国信息安全   2025-05-15 11:30  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_gif/1brjUjbpg5xVLE4piaHgL1UBHc3xeTc4FDPWFRJ5oOKovSjA91wI83jc1BXGUEOicicj0LOE62rj2jQG2u5r0Nxmg/640?wx_fmt=gif&from=appmsg "")  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_png/1brjUjbpg5xVLE4piaHgL1UBHc3xeTc4FJmfkaDNSfgIQ8NrSFpvhVILEUElJObJFUicfjf4TLX5YlX2wWQ39J2w/640?wx_fmt=png&from=appmsg "")  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_gif/1brjUjbpg5xVLE4piaHgL1UBHc3xeTc4FDPWFRJ5oOKovSjA91wI83jc1BXGUEOicicj0LOE62rj2jQG2u5r0Nxmg/640?wx_fmt=gif&from=appmsg "")  
  
**扫码订阅《中国信息安全》**  
  
  
邮发代号 2-786  
  
征订热线：010-82341063  
  
  
  
**漏洞情况**  
  
近日，国家信息安全漏洞库（CNNVD）收到关于Fortinet多款产品安全漏洞（CNNVD-202505-1780、CVE-2025-32756）情况的报送。未经身份验证的远程攻击者可以通过发送特制的HTTP请求触发漏洞，进而执行任意代码。Fortinet多款产品均受此漏洞影响。目前，Fortinet官方已发布新版本修复了漏洞，建议用户及时确认产品版本，尽快采取修补措施。  
  
## 一漏洞介绍  
  
  
Fortinet FortiRecorder、Fortinet FortiMail等都是美国飞塔（Fortinet）公司的产品。Fortinet FortiVoice是一个统一通信和协作服务系统，Fortinet FortiRecorder是一套基于Web的网络视频录像机管理系统。Fortinet FortiMail是一套电子邮件安全网关产品。FortiNDR 是一套网络检测与响应系统，FortiCamera是一套视频监控系统。  
  
Fortinet多款产品存在安全漏洞，漏洞源于产品在处理特定 HTTP 请求时，未对请求中的hashcookie进行充分边界检查，导致远程未授权攻击者可发送特制的HTTP请求触发栈缓冲区溢出，进而执行任意代码。  
  
## 二危害影响  
  
  
Fortinet FortiVoice 7.2.0版本、7.0.0至7.0.6版本、6.4.0至6.4.10版本、FortiRecorder 7.2.0至7.2.3版本、7.0.0至7.0.5版本、6.4.0至6.4.5版本、FortiMail 7.6.0至7.6.2版本、7.4.0至7.4.4版本、7.2.0至7.2.7版本、7.0.0至7.0.8版本、FortiNDR 7.6.0版本、7.4.0至7.4.7版本、7.2.0至7.2.4版本、7.0.0至7.0.6版本、FortiCamera 2.1.0至2.1.3版本、2.0所有版本、1.1所有版本均受漏洞影响。  
  
## 三修复建议  
  
  
目前，Fortinet官方已发布升级补丁修复了该漏洞，建议用户及时确认产品版本，尽快采取修补措施。官方参考链接如下：  
  
https://fortiguard.fortinet.com/psirt/FG-IR-25-254  
  
本通报由CNNVD技术支撑单位——奇安信网神信息技术（北京）股份有限公司、北京天下信安技术有限公司等技术支撑单位提供支持。  
  
CNNVD将继续跟踪上述漏洞的相关情况，及时发布相关信息。如有需要，可与CNNVD联系。联系方式: cnnvd@itsec.gov.cn  
  
（来源：CNNVD）  
  
  
  
**分享网络安全知识 强化网络安全意识**  
  
**欢迎关注《中国信息安全》杂志官方抖音号**  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_jpg/1brjUjbpg5xVLE4piaHgL1UBHc3xeTc4FgI0wp9RZ7d7zut9LjVvqMicDenPhfKQZ4WznB1ZyJNKmmuTckHDNfrA/640?wx_fmt=jpeg&from=appmsg "")  
  
  
**《中国信息安全》杂志倾力推荐**  
  
**“企业成长计划”**  
  
  
**点击下图 了解详情**  
  
  
  
[](https://mp.weixin.qq.com/s?__biz=MzA5MzE5MDAzOA==&mid=2664162643&idx=1&sn=fcc4f3a6047a0c2f4e4cc0181243ee18&scene=21#wechat_redirect)  
  
  
