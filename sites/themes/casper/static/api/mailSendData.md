获得发送数据的接口：
```
https://service.wellemail.com/Service/GetReportSummary
```

请求参数：

 | 参数名称 | 参数类型 | 是否必须<br>(1是0否) | 参数说明 | 取之说明 |
 | --- | --- | --- | --- | --- |
 | userName | String | 1 | 用户名 | 已开通的帐号名称 |
 | passWord | String | 1 | 操作密码 | 与帐号名称对应的密码 |
 | jobName | String | 1 | 任务名称 | 任务批号，唯一标定任务 |

  返回值：
  ```
  例如：{ Accepted: true,Message:请求被正常接收,Validation Passed=true, TaskId:5298550fa023c410c439b454,
Value: {Total:0.0, 总提交量
SentCount:0.0,发送数量
SentRate:0.0,
InvalidCount:0.0,无效数量
InvalidRate:0.0,
SendOkCount:0.0,发送成功
SendOkRate:0.0,
ErrorCount:0.0,地址错误
ErrorRate:0.0,
RejectCount:0.0,退回
RejectRate:0.0,
OpenCount:0.0,打开数量
OpenRate:0.0,
ClickCount:0.0,点击数量
ClickRate:0.0,
UnSubscribe:0.0,取消订阅
UnSubscribeRate:0.0
}}
  ```