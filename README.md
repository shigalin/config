# Config
* 无聊建了个频道 https://t.me/useConfig
* 收集并修改的配置文件
* **[Quantumult.conf](https://raw.githubusercontent.com/lhie1/Surge/master/Quantumult.conf)**（带Filter Action）：主要是同步lhie1_Shadowrocket.conf 配置，根据Filter Action添加相关服务服务器选择，如Apple，Netflix
* **[Quantumult_URL.conf](https://raw.githubusercontent.com/lhie1/Surge/master/Quantumult_URL.conf)**：同步lhie1.Hostname.conf + lhie1.URL_REJECT.conf配置
* **[Quantumult_Lite.conf](https://raw.githubusercontent.com/shigalin/Config/master/Quantumult_Lite.conf)**（不带Filter Action）：主要是同步lhie1_Shadowrocket.conf 配置，尽量简化广告规则
* **[Quantumult_gfwlist.conf](https://raw.githubusercontent.com/shigalin/Config/master/Quantumult_gfwlist.conf)**（带Filter Action）：Quantumult规则gfwlist版，默认直连
* **[banAD.acl](https://raw.githubusercontent.com/shigalin/Config/master/banAD.acl)**：适用Android上SSR的规则，默认代理，屏蔽广告
* **[fullgfwlist.acl](https://raw.githubusercontent.com/shigalin/Config/master/fullgfwlist.acl)**：适用Android上SSR、影梭的规则，gfwlist版

# Quantumult规则使用：
1. 进入Settings — Favorites
2. 选择右上角添加，Server（服务器订阅），Filter（TCP规则订阅），Rejection（URL规则订阅）
3. 选择 Filter ，Name随意，URL填入 https://raw.githubusercontent.com/lhie1/Surge/master/Quantumult.conf  ，勾选Filter Action
4. 如果开启了HTTPS解密进入第5步
5. 选择 Rejection ，Name随意 ，URL填入 https://raw.githubusercontent.com/lhie1/Surge/master/Quantumult_URL.conf , 勾选Including Host Names
6. **规则生效或者更新规则**：在Favorites的Filter订阅和Rejection订阅多了订阅的选项，**左滑选项，选择Replace替换，选择相应的服务器或者Policy**
7. 在Filter替换过程中，注意选择**Apple、PayPal服务**是选择直连或者代理，包含iCloud服务和App Store下载等。其他如果不需要默认选项即可

# Quantumult的几个配置REJECT规则的区别
* Quantumult.conf广告屏蔽的规则最多最全，即lhie1大佬的规则
* Quantumult_Lite.conf已删除所有IP-CIDR的REJECT规则，未来同步lhie1删除其他REJECT规则，一般情况只删除REJECT规则不增加
* Quantumult_gfwlist.conf只屏蔽了谷歌分析和360分析的域名

