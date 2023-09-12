```
 __    __     __  __     ______     ______   ______     ______     __
/\ "-./  \   /\ \_\ \   /\  ___\   /\__  _\ /\  __ \   /\  __ \   /\ \
\ \ \-./\ \  \ \____ \  \ \___  \  \/_/\ \/ \ \ \/\ \  \ \ \/\ \  \ \ \____
 \ \_\ \ \_\  \/\_____\  \/\_____\    \ \_\  \ \_____\  \ \_____\  \ \_____\
  \/_/  \/_/   \/_____/   \/_____/     \/_/   \/_____/   \/_____/   \/_____/
```

# [此为真寻bot适配版](https://github.com/HibiKier/zhenxun_bot)
# 经测试，Win下基于Python3.8的真寻不能运行此插件，3.9可以。
原作者Ljzd-PRO 版本跳转[nonebot-plugin-mystool](https://github.com/Ljzd-PRO/nonebot-plugin-mystool)
 - 若登录等待输入验证码或手机号时间过短，请在ENV.DEV文件修改SESSION_EXPIRE_TIMEOUT
 - 真寻食用直接把src目录下nonebot_plugin_mystool文件夹丢进真寻插件文件夹。
 - 详细设置请编辑插件目录下的 config.py
 - 具体设置请查看[🔗官方Wiki 文档](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki)

### 改动内容
基于2022年12月31日版（v0.2.2），改版适配真寻bot。经测试，功能大部分正常。
具体改动如下：
 - init.py添加真寻版帮助索引，并更改功能触发指示以避免功能冲突。
 - help.py更改帮助模块触发词与名称为“米游社帮助”以避免和真寻的帮助冲突。
 - login.py第205行添加超时提示（请与ENV.DEV文件的SESSION_EXPIRE_TIMEOUT同步修改）。
 - timing.py更改签到触发词避免和真寻的签到功能冲突。

基于2023年1月17日版（v0.2.3），重新检查适配。

基于2023年3月19日版（v0.2.4），跟进。

2023年4月1日（v0.2.5），跟进。

2023年5月21日（v0.2.9），跟进。

2023年8月5日（v1.2.0），跟进。

 - 注：原作者在本版实装了qq频道（qqguid）代码，但真寻目前尚未实装相关适配器，造成启动时插件载入失败，所以需要手动到
[qqguild](https://github.com/nonebot/adapter-qqguild)
去下载whl文件对频道插件进行安装，方可正常载入此插件。

2023年8月14日 （v1.2.3），跟进。

2023年8月17日 （v1.2.4），跟进。

2023年8月23日 （v1.3.0），跟进。

2023年9月5日 （v1.3.2），跟进。

2023年9月12日 （v1.3.3），跟进。

2023年9月12日 （v1.3.3），复原。
 - 注：本人眼瞎，没看见v1.0更新时，原作者在`plugin_data.json`中实装了`command_start`字段（即自定义命令前缀），代替了本fork的作用，故本人将所有更改复原，避免与原repo功能重复与矛盾。此版与原作者代码完全相同<del>，下一版将尝试解决nonebot版本不兼容问题</del>。（经查证，原代码中包含`nonebot.Adapter`的使用，此为nonebot2.0.0rc2实装功能。截至目前，真寻源码中描述依赖的`pyproject.toml`指出，`nonebot2 = "^2.0.0rc1"`，即真寻可以使用比rc1更新的nonebot版本运行，故建议遇到不能导入`nonebot.Adapter`的佬，对运行环境内的nonebot进行一个级的升…）
>

### 碎碎念
 - 本人运行ayakasuki佬的改版的插件并不成功，故有此repo。
 - 本插件最终效果仅达到能用水平。
 - 如有适配造成的功能问题，请提issue，本人将尝试解决。


### 📖 插件具体使用说明

请查看原作者文档 -> [🔗Wiki 文档](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki)
