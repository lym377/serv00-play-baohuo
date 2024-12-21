# serv00-play 配套保活

感谢[饭奇骏大佬的serv00-play项目](https://github.com/frankiejun).  [serv00-play项目地址](https://github.com/frankiejun/serv00-play).

感谢[vfhky大佬的nz项目](https://github.com/vfhky).    [serv00_ct8_nezha项目地址](https://github.com/vfhky/serv00_ct8_nezha).
- **serv00ql 是青龙面板保活脚本**

![undefined](https://jpg.jzccc.us.kg/api/cfile/AgACAgUAAxkDAAMRZ2bQVnmN3Z_WgLItlwdkKobOfjAAAkHCMRv26zhXVr8iewLtpP4BAAMCAAN4AAM2BA)
## ql面板环境变量配置
使用变量名存储服务器信息，每个服务器用一个变量，例如：
| 环境变量        | 说明                                      | 默认值 | 示例值                |
|-----------------|-----------------------------------------|--------|-----------------------|
| `SERVERS`       | 服务器信息列表，格式为 `user:pass:host`，多个服务器使用逗号分隔 | 无     | `user1:password1:host1, user2:password2:host2` |
| `BOT_TOKEN`     | Telegram Bot Token，用于发送消息通知     | 无     | `123456789:ABCDEFghijklmnopqrstuvwxyz` |
| `CHAT_ID`       | 接收 Telegram 消息的聊天 ID             | 无     | `123456789`           |
| `SINGBOX`       | 是否启用 singbox 服务                    | 1      | `1`（启用）或 `2`（不启用） |
| `NEZHA_DASHBOARD` | 是否启用 nezha-dashboard 服务            | 2      | `1`（启用）或 `2`（不启用） |
| `NEZHA_AGENT`   | 是否启用 nezha-agent 服务               | 2      | `1`（启用）或 `2`（不启用） |
| `SUN_PANEL`     | 是否启用 sun-panel 服务                  | 2      | `1`（启用）或 `2`（不启用） |
| `WEB_SSH`       | 是否启用 webssh 服务                     | 2      | `1`（启用）或 `2`（不启用） |
| `services_started` | 记录当前启用的服务，用于显示和发送通知 | 无     | 自动填充              |

示例：
![undefined](https://jpg.jzccc.us.kg/api/cfile/AgACAgUAAxkDAAMSZ2bRUg3zy1IQvmG98Z4EZls4VjIAAkPCMRv26zhXWE9Dy0_GKO4BAAMCAAN5AAM2BA)

- **serv00vps 是vps保活脚本**
## JSON配置
注意:务必将`serv00.json` 文件存入私库或其他支持直链的云盘，避免信息泄露。git私库文件可用CM的私库项目获取可访问的直链
```
{
  "TELEGRAM_CONFIG": {
    "BOT_TOKEN": "",
    "CHAT_ID": ""
  },
  "SERVERS": [
    {
      "HOST": "cache14.serv00.com",
      "SSH_USER": "用户名",
      "SSH_PASS": "密码"
    },
    {
      "HOST": "cache14.serv00.com",
      "SSH_USER": "",
      "SSH_PASS": ""
    },
    {
      "HOST": "cache14.serv00.com",
      "SSH_USER": "",
      "SSH_PASS": ""
    },
    {
      "HOST": "cache14.serv00.com",
      "SSH_USER": "",
      "SSH_PASS": ""
    }
  ],
  "FEATURES": {
    "SINGBOX": 1,
    "NEZHA_DASHBOARD": 2,
    "NEZHA_AGENT": 2,
    "SUN_PANEL": 2,
    "WEB_SSH": 2
  }
}
```
**1开 2关**
# 注意
**必须将变量修改为你自己的信息,自行修改脚本内容。在52行** 
**必须将变量修改为你自己的信息,自行修改脚本内容。在52行**
**必须将变量修改为你自己的信息,自行修改脚本内容。在52行**

示例:
![undefined](https://jpg.jzccc.us.kg/api/cfile/AgACAgUAAxkDAAMTZ2bRaRyygvCxNaGSypYKd83Qp3gAAkXCMRv26zhXAjgdTBPw_yIBAAMCAAN4AAM2BA)

### 后续可自行添加 
- 1 切换到 nezha_dashboard 目录并启动 哪吒V1_dashboard 进程

```
cd /home/$SSH_USER/nezha_app/agent || exit
nohup sh nezha-agent.sh > nezha-agent.log 2>&1 &
```
- 2 切换到 nezha_agent 目录并启动 哪吒V1_agent 进程
```
cd /home/用户名/nezha_app/agent || exit
nohup sh nezha-agent.sh > nezha-agent.log 2>&1 &
```
-3 切换到另一个目录并启动 sun-panel 进程
```
cd /home/用户名/serv00-play/sunpanel || exit
nohup ./sun-panel > sunpanel.log 2>&1 &
```
- 4 切换到另一个目录并启动 webssh 进程
```
cd /home/用户名/serv00-play/webssh || exit
nohup ./wssh > webssh.log 2>&1 &
```
等等。。。  
