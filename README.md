# gitlabTransfer
gitlab迁移自动迁移工具

### 下载
```bash
https://raw.githubusercontent.com/hanpenggit/gitlabTransfer/main/gitlabTransfer.exe
```

<p>参数中cookie的值可以用你的账户登录gitlab，随便发一个请求，找到 Request Headers 中的Cookie值，找到其中的 _gitlab_session即可 </p>


编辑 `./config.json`, 可以配置，内容如下：

```bash
{
  "source_ip": "192.168.1.60",
  "source_port": 80,
  "source_cookie": "_gitlab_session=28d32bebb3e48458dcd4802f3cdb3f1b",
  "target_ip": "192.168.1.80",
  "target_port": 80,
  "autoClone": false,
  "path": "D:/newClone"
}
```

|  参数  | 备注  |
|  ----  | ----  |
| source_ip  | 要克隆得仓库的ip |
| source_port  | 要克隆得仓库的端口 |
| source_cookie  | 要克隆得仓库的sessionid |
| target_ip  | 要推送的目标仓库的ip |
| target_port  | 要推送的目标仓库的端口 |
| autoClone  | 是否自动克隆，默认为false，如果为true，则会自动执行 git clone --bare命令|
| path  | 克隆之后文件放在那个目录下 |

<p>执行过后，会在每一个组或者子群组中生成对应的clone.bat和push.bat，手动执行即可 </p>
