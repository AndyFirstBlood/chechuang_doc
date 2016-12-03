# api docs

1.用户管理

(1)注册

请求说明

>POST /api/v1/register

###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| username  | 必填 |  用户名   |
| password  | 必填 |  密码  |
| phone     | 必填 | 手机  |

#### 返回结果

```javascript
{
  "username": "zzr",
  "mobilePhoneNumber": "15751158939",
  "emailVerified": false,
  "mobilePhoneVerified": false,
  "objectId": "5842fbbaac502e006ccd4ab4",
  "createdAt": "2016-12-03T17:07:06.268Z",
  "updatedAt": "2016-12-03T17:07:06.268Z"
}
```