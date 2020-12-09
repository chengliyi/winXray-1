# winXray 
本软件源码已贡献到公共领域并放弃版权，源码可使用 [aardio（开发环境仅6.5MB）](http://www.aardio.com) 编译生成单文件绿色EXE( 不需要.Net等任何外部运行库 ），**[点这里下载](https://raw.githubusercontent.com/winXray/winXray/master/release/winXray.7z)** （ [64位版本](https://raw.githubusercontent.com/winXray/winXray/master/release/winXray.7z) / [32位版本](https://raw.githubusercontent.com/winXray/winXray/master/release/winXray32.7z) ），解压即可直接使用( 仅  **[5.0MB](https://raw.githubusercontent.com/winXray/winXray/master/release/winXray.7z)** - 已自带 Xray-core）。

winXray[:loud_sound:](http://dict.youdao.com/dictvoice?audio=winxray&type=2) 是一个简洁稳定的 [Xray/V2Ray(vmess/vless/xtls)、Shadowsocks、Trojan](https://github.com/XTLS/Xray-core) 通用客户端（Windows系统），可自动检测并连接访问速度最快的代理服务器。服务器连接异常时可以自动更换代理服务器 - 再也不用担心服务器抽风了。winXray 也提供一键安装 XRay(V2Ray、Shadowsocks、Trojan) 服务器工具。  
  
这里说明一下，简洁不等于功能弱。一般人只是为了上个网加个速用不上太复杂的小众功能。太复杂同时就会带来不稳定、且不必要的占用资源并同时降低性能，所以 winXray 做了大量的优化、精简，但是并没有减少主要的、必要的代理服务器功能。  
  
<details>  <summary>最新公益服务器列表</summary>  <pre>
vless://bf4a6c2b-db1b-57de-f45a-364aa254d1f7@z.vulvpstech.xyz:443/?flow=xtls-rprx-direct&host=z.vulvpstech.xyz&tls=xtls#%E7%BE%8E%E5%9B%BD%E8%A5%BF%E9%9B%85%E5%9B%BE_XTLS%2FDirect
vless://904da8f7-a5af-3c34-3f3d-c3b2ea59bde8@q.vulvpstech.xyz:443/?host=q.vulvpstech.xyz&tls=xtls#%E7%BE%8E%E5%9B%BD%E6%B4%9B%E6%9D%89%E7%9F%B6_XTLS%2FDirect
</pre></details>    

之前我用过很多代理客户端，经常用一会就挂掉了，有些测试很久才找到下一个可用的服务器，有时怎么切换都不行，一定要把整个软件退出重启才能恢复。而且在WIN10上都有相同的BUG:PAC代理用一段时间就会卡死( winXray已经通过自行实现PAC服务器解决了这个问题 )，其实这些软件里提供的很多功能我并不需要，我只想愉快地用下 google 找点技术资料提升工作效率。但是在网上找了很久都没找到适合的软件，于是决定自己动手写一个，还好用 aardio 写软件的速度很快 - 大概用了几个小时就完成了 winXray 的主要代码，改进了几个版本以后就很稳定了，**我自己用了 winXray  几个月再也没有遇到 google 抽风访问不了的问题**。    


![winXray](./screenshots/winXray.png)

winXray支持批量导入 vless、vmess、ss、trojan、trojan-go …… 等格式的分享链接，  
也可以导入通用订阅链接，以及 base 64、json …… 等不同格式的服务器配置。

![服务器配置](./screenshots/config.json.png)
**小技巧: JSON里点击任意字段都会显示该字段的用法说明。**

可选在 ["/xray-core/winXray-default-servers.json"](./xray-core/winXray-default-servers.json) 文件中添加默认服务器配置（生成EXE后默认配置自动嵌入到EXE文件，可选删除该文件,也可以继续使用该文件覆盖EXE自带的默认服务器列表）。

![PAC配置](./screenshots/pac.png)
**小技巧: PAC编辑器里点击任意域名都会自动关联到单选框，可以直接切换代理或直连。**

软件首次运行时会在当前目录查找 "./xray-core/xray.exe"   
发行文件仅需要 "./winXray.exe"，可选带上 "./xray-core/" 目录（ 如果没有找到会自动到v2ray官网下载，不过没有代理服务器下载有时候非常慢 )。

![端口配置](./screenshots/config.advanced.png)
