邮件发送接口：
```
触发邮件地址：https://service.wellemail.com/Service/SendTriggerEmail
营销邮件地址：https://service.wellemail.com/Service/SendEmail
```
请求参数：

| 参数名称 | 参数类型 | 是否必须 | 参数说明 | 取值说明 |
 | --- | --- | --- | --- | --- |
 | userName | String | 1 | 用户名 |  |
 | subAccount | String | 0 | 子用户名 | 可为空 |
 | password | String | 1 | 操作密码 |  |
 | jobName | String | 1 | 任务名称 | 1、调用方设定，每个邮件模板对应一个jobname；<br>2、自定义的唯一标识，用于后期发送时调用。（例如：UUID 32位、36位都可以）；<br>3、如果需要更改邮件主题、发件人、发件地址或者邮件内容，请用新的jobname。<br>4、首次使用的jobname提交任务，需要人工审核；<br>5、中文或者有特殊符号的时候，需要用URLUTF8编码 |
 | fromName | String | 1 | 发件人名称 | 发件人名称(中文或者有特殊符号的时候，需要用URLUTF8编码) |
 | fromAddress | String | 1 | 发送地址 | 使用企业邮箱地址（腾讯企业邮箱除外） |
 | emails | String | 1 | 目标邮箱地址 | 1、接收邮件的会员邮箱地址；<br>2、如果邮件中需要变量，需要符合csv文件格式的字符串，第一列名称必须为email ，其余各列名称为邮件中变量的名称；<br>3、变量为中文或者有特殊符号的时候，需要用URLUTF8编码； |
 | mailTitle | String | 1 | 发送主题 | 邮件发送后显示的标题(中文或者有特殊符号的时候，需要用URLUTF8编码) |
 | mail | String | 1 | 邮件内容 | 邮件内容在首次发送时上传，utf-8格式保存；以后可以为空； |

 应答内容：
 ```
 例如：提交成功
{ Accepted = true，Message = 请求被正常接收，ValidationPassed = true，
TaskId = 5298550fa023c410c439b454， Value: object }
 ```
 返回值：
 ```
 返回一个JSON对象，包括以下参数
 ```
 | 参数名称 | 类型 | 说明 |
 | --- | --- | --- |
 | TaskId | String | 操作任务号，用来查找问题 |
 | ValidationPassed | Bool | 是否通过认证（用户名认证或其它认证） |
 | Accepted | Bool | 提交任务是否接收成功  |
 | IsHealth | Bool | 提交任务是否正常；<br> 提交出现重复、无效数据或因为费用不够没有发送出去等情况为false |
 | Message | Sting | 任务消息 |
 | Status | Int | 操作结果码 <br> 1 提交成功；<br> -1 提交失败；<br> -100没有找到账户；<br> -101 账户关闭；<br> -102 账户余额不足；<br> -200 没有找到帐户发送通道 |
 | Value | Object | 备用（默认NULL） |
