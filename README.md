# Github Action 企业微信消息发送插件
原作者为 wertycn
通过企业微信自定义应用发送通知，支持执行失败后发送失败通知、自定义模板

支持消息类型：
* 文本
* markdown

支持发送模式：
* 调用时发送
* 完成时发送
* 调用及结束时均发送

使用方式：

```yaml
- name: 企业微信markdown消息发送
  uses: mason105/send_message_to_wechat_work_app@main
  with:
    wechat_id: xxxx # 企业微信id
    agent_secret: xxxx # 应用密钥
    agent_id: 1000002 #应用id
    to_user:  userid1| userid2# 消息接收人，多个使用竖线|分割,默认为空发送给所有人
    msgtype: markdown or text
    send_step: main # 消息发送时机 main 正常流程  post action 执行完成后发送
    content: "Test message"
```

自定义action参考文档
https://docs.github.com/cn/actions/creating-actions/about-custom-actions#further-reading


