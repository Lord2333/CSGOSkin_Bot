# CSGOSkin_Bot

一个基于OPQ-Bot的CSGO饰品价格追踪Bot，使用Flask+Sqlite作为后端运行。

支持的平台：

| 平台     | 价格 | 在售状态 |
| -------- | ---- | -------- |
| Buff     | √    | √        |
| 悠悠有品 | √    | √        |
| IGXE     | √    | √        |
| 小黑盒   | √    | √        |
| TBD...   | ...  | ...      |

ToDo

- [ ] 网页端删除皮肤
- [ ] 检测间隔动态调整（凌晨1点到早上7点降低检测频率，下午3点到8点提高检测频率）
- [ ] 一键部署检测程序并接入现有机器人（通过Deta平台部署检测程序，并接入已有的机器人，减少部署机器人的时间成本和金钱）
- [ ] 欢迎提Issue~

> 注：由于我本人从来没用过C5、身边的朋友们也没有这个需求，且C5平台APP不支持直接分享链接，考虑到运行速度与效率，就暂时不支持对C5平台的饰品进行追踪。其他的平台可以提Issue，只要能**有分享链接**基本上就都可以支持。

## 0x00 使用

如果只是想使用功能的话，可以直接添加QQ：`1107459688`，或访问项目官网：https://skin.laosepi.cool/

使用方法如下：

**新增饰品**：`饰品添加+分享链接`，例如：饰品添加https://h5.youpin898.com/goodsInfo.html?id=17867828 ，发送后机器人将解析饰品信息（大概需要半分钟左右），请不要连续发送命令。如果发送命令后一分钟后机器人仍未响应，则有可能是机器人宕掉了；如果发送信息后机器人回复的是机器人使用说明，则说明命令**有误**（看看分享链接是否正确）

![](https://s2.loli.net/2022/09/28/436cqtdnlLSANsg.png)

**主动删除饰品**：`饰品删除+分享链接`，例如：饰品删除https://h5.youpin898.com/goodsInfo.html?id=17867828

![](https://s2.loli.net/2022/09/28/YBMWI9hVQvgpiJ1.png)

**查看全部关注饰品**：`饰品查询`，发送后机器人将会返回一个有效期为半小时的链接，可查看全部关注饰品

![](https://s2.loli.net/2022/09/28/vAStIVsELmH8lRx.png)

> 注意：对于Buff和xhh平台，他们的分享链接中的参数会随着时间发生一些变化（这一点在下面会进行分析），如果需要删除某个饰品请使用`饰品查询`功能，进入管理页面复制链接后，再使用`饰品删除`命令进行操作（网页版删改的功能还在写）。

## 0x01 项目详情

篇幅较长，请见[help.md](help.md)

单独部署本项目[0x01 安装](help.md#0x01-安装)

