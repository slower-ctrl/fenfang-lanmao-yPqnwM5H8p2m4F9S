
某一天 ceo 需要一个登录系统，找了开发团队


# 控制狂团队


领导点了卡布奇诺，打开了自己轻薄的 mac book， 点开 word 文档, 开始编写：



```
1. 项目背景
2. 名词解析
3. 数据表设计
  3.1 user表
  3.2 Role表
  。。。。。。
4. api 设计
  4.1 用户信息api
  4.2 登录api
  。。。。。。

```

领导续了杯摩卡，继续编写


3\.1 user表




| 字段 | 类型 |
| --- | --- |
| user\_id | varchar(10\) |
| email | varchar(255\) |
| password | varchar(255\) |
| registration\_date | timestamp |
| create\_at | timestamp |
| create\_by | varchar(10\) |
| update\_at | timestamp |
| update\_by | varchar(10\) |


3\.2 Role表




| 字段 | 类型 | note |
| --- | --- | --- |
| id | int |  |
| user\_id | varchar(10\) |  |
| Role | varchar(30\) | admin / normal |
| create\_at | timestamp |  |
| create\_by | varchar(10\) |  |
| update\_at | timestamp |  |
| update\_by | varchar(10\) |  |


。。。。。


领导有点饿了，叫了份可可奥利奥脏脏毛巾卷， 继续编写


4\.1 用户信息api




| request | response |
| --- | --- |
| GET /user\_query?user\_id\=xxx | `{ "user_id": "xxx", "password": "xxxx"}` |


4\.2 登录api




| request | response |
| --- | --- |
| POST /user\_login `{"user_id": "xxx", "password": "xxxx"}` | `{ "success": true / false}` |


。。。。。。


第二天，领导叫来了程序员们，给了份word 文档


听话的程序们加班加点用 c\# 写了实现：



```
/// 不要问我为什么字段命名不规范，我只是一个打工仔，上有80岁老母，下有3岁熊孩子
/// 领导 ： 1. 我们要严格遵守db规范
/// 领导 ： 2. json 要与 db 统一
/// 领导 ： 3. 因此，不管什么语言和框架都不能影响规范

public class UserInfo
{
  public string user_id {get;set;}
 public string password {get;set;}
 public DateTime registration_date {get;set;}
 public string create_by {get;set;}
 public DateTime create_at {get;set;}
 public string update_at {get;set;}
 public DateTime update_at {get;set;}
 .....
}

public class UserInfoController
{
  [HttpGet("user_login")]
  public UserInfo GetUser(UserInfo user)
  {
      ......
  }

  [HttpPost("user_query")]
  public UserInfo GetUser(string user_id)
  {
      ......
  }
}

```

# 土豪团队


领导点了卡布奇诺，打开了自己轻薄的 mac book，点开了 auth0 网站


看了看功能，很满意


看了看价格，不算贵


第二天 领导找了 hr


下午 入职 1年的某某某 打包回了家


# 时代潮流团队


领导点了卡布奇诺，打开了自己轻薄的 mac book，点开 chatgpt



```
hello chatgpt, 帮我设计一份 登录系统
chatgpt ： 正在生成中。。。。

```

第二天，领导叫来了程序员们，给了份word 文档


听话的程序们也点开了 chatgpt



```
hello chatgpt, 帮我按照这份 word文档实现一个登录系统
chatgpt ： 正在生成中。。。。

```

 本博客参考[楚门加速器p](https://tianchuang88.com)。转载请注明出处！
