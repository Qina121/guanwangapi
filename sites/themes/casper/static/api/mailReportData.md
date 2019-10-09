获得邮件报表页面的接口： 
```
https://service.wellemail.com/Service/GetStatisticsHashkey
```
请求参数：

| 参数名称 | 参数类型 | 是否必须<br>(1是0否) | 参数说明 | 取之说明 |
 | --- | --- | --- | --- | --- |
 | userName | String | 1 | 用户名 | 已开通的帐号名称 |
 | passWord | String | 1 | 操作密码 | 与帐号名称对应的密码 |
 | jobName | String | 1 | 任务名称 | 任务批号，唯一标定任务 |

返回值：
```
string  HashKey 
Hashkey为取得任务详细统计网页的链接，用于打开链接 
https://service.wellemail.com/Statistics/Index/HashKey
```

报表中的详细数据，通过以下链接获取：
```
https://service.wellemail.com/Statistics/DownloadDetails/HashKey 
```

格式如下：

 <table>
<tr>
    <td>1234567@qq.com</td>
    <td>Open</td>
    <td>2015/5/14 13:28</td>
    <td>    </td>
</tr>
<tr>
    <td>1234567@qq.com</td>
    <td>Click</td>
    <td>2015/5/14 13:28</td>
    <td> www.taobao.com   </td>
</tr>
</table>