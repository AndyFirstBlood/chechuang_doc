# api docs

**baseurl  http://chechuang.leanapp.cn**

1.用户管理

(1)验证图片
>GET /api/v1/auth/image
###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| null  | null |  null   |

#### 返回结果

```javascript

svg+xml,

image-text(验证码内容，在response headers中)

```

(2)请求短信验证

请求说明

>GET /api/v1/smsCode/:mobilePhoneNumber

###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| mobilePhoneNumber  | 必填 |  手机号   |

#### 返回结果

```javascript
{
  "status": 1,
  "code": 200,
  "data": "get smsCode success"
}
```

(3)手机注册&&登录

请求说明

>POST /api/v1//signuporlogin/phone

###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| username  | 必填 |  用户名   |
| mobilePhoneNumber | 必填 | 手机  |
| smsCode     | 必填 | 短信验证码 |

#### 返回结果

```javascript
{
  "status": 1,
  "code": 200,
  "data": {
    "username": "zzr",
    "mobilePhoneNumber": "15751158939",
    "mobilePhoneVerified": true,
    "emailVerified": false,
    "objectId": "58497954ac502e006c5b3519",
    "createdAt": "2016-12-08T15:16:36.646Z",
    "updatedAt": "2016-12-08T15:16:36.646Z"
  }
}
```