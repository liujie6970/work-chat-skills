# work-chat-coach｜同事与朋友单聊沟通技能

版本：1.2.0

仅用于与同事、朋友进行一对一私聊：自然接话、理解对方表达、日常工作协作、情绪回应、分歧处理、拒绝和边界表达。

不包含群聊、领导汇报、下属管理、供应商/客户沟通或正式公文。

## 本次更新
- 每次默认一句、必要时两句；通常 10～40 字，原则上不超过 80 字，禁止长段回复。
- 查询、登记、搜索前先礼貌短回应，再处理，最后简短反馈结果。
- 缺信息只问一个关键问题；成功后才说“已登记”或“已保存”。
- 话术参考已同步精简，分析和多版本输出也受短回复规则约束。

## 文件结构
```text
work-chat-coach/
├── SKILL.md
├── README.md
└── references/
    └── message-patterns.md
```

## 导入 OMB
在对应 Bot 的 Settings → Skills → Import 中，粘贴技能文件夹的 GitHub URL：

https://github.com/liujie6970/work-chat-skills/tree/main/work-chat-coach

检查导入预览，确认包含 SKILL.md 和 references/message-patterns.md 后再 Add。导入后先审核，再启用。

注意：查询/登记/搜索的“先回应、再处理、最后反馈”需要宿主支持分阶段输出。若 Bot API 只能在任务结束后返回一次文本，应由调用端先发送短回应，再调用 Bot，最后发送结果。

## 参考项目
- https://github.com/shengjidaguai-china/goutoujunshi
- https://github.com/vectorAz/goutoujunshi-jev

迁移思路：上下文优先、事实与推测分离、单一沟通动作、自然短消息起草、反馈分支和安全边界；针对同事/朋友私聊重新编写。
