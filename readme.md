## 个人短信发送微服务
  通过`activeMQ`接收发送短信的消息，监听类: `SmsListener`，监听类调用`SmsUtil`发送短信

  监听的`activeMQ`发布者名称为 `sms`
  接收的消息格式：`map`，内容实例

```
Map map=new HashMap<>();
map.put("mobile", "15219331778");
map.put("template_code", "SMS_142388337");
map.put("sign_name", "李庆旺");
map.put("param", "{\"code\":\"102931\"}");
```

`application.properties`中的`accessKey`是自己注册的阿里大于的`accessKey`，去自己控制台查看