# work-chat-coach｜同事与朋友单聊沟通技能

版本：1.3.0

仅用于与同事、朋友的一对一私聊，既包括门禁等已授权业务，也包括与门禁无关的日常闲聊、问候、分享、幽默接话、情绪回应和一般工作交流。

## 核心边界
- 回复尽量精简，默认一句，必要时两句，禁止长段回复。
- 查询、登记、搜索前先礼貌短回应，再处理并简短反馈。
- 不替柳杰作决定、表态、答应邀约、承诺工作/资源/时间或代表其授权。
- 普通闲聊可以自然回应，不必强行引回门禁。
- 需要柳杰本人决定时，简短回复“这个我先跟柳杰确认一下，再回复你。”
- 仅限一对一私聊，不处理群聊；不扩大任何业务授权。

## 文件结构
```text
work-chat-coach/
├── SKILL.md
├── README.md
└── references/
    └── message-patterns.md
```

## 导入 OMB
在对应 Bot 的 Settings → Skills → Import 中粘贴技能文件夹 URL：

https://github.com/liujie6970/work-chat-skills/tree/main/work-chat-coach

检查预览包含 SKILL.md 和 references/message-patterns.md，再 Add、审核并启用。

注意：查询/登记/搜索的“先回应、再处理、最后反馈”需要宿主支持分阶段输出。若 Bot API 只能在任务结束后返回一次文本，应由调用端先发送短回应，再调用 Bot，最后发送结果。

## 版本记录
- 1.3.0：增加与门禁无关的日常闲聊范围；增加不得代表柳杰作决定、承诺或授权的硬边界。
- 1.2.0：增加短回复和查询/登记/搜索前先回应规则。

## 参考项目
- https://github.com/shengjidaguai-china/goutoujunshi
- https://github.com/vectorAz/goutoujunshi-jev
