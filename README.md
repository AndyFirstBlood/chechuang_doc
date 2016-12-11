# api docs

**baseurl  http://xxxxx.xxx**

1.用户管理

(1)验证图片

>GET /api/v1/captcha/image

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

>GET /api/v1/sms/{mobilePhoneNumber}

###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| mobilePhoneNumber  | 必填 |  手机号   |

#### 返回结果

```javascript
{
  OK
}
```

(3)手机注册&&登录

请求说明

>POST /api/v1/auth

###请求参数

| 参数名    |  请求范围| 说明 |
| :-------- | --------:| :--: |
| username  | 必填 |  用户名   |
| mobilePhoneNumber | 必填 | 手机  |
| smsCode     | 必填 | 短信验证码 |

#### 返回结果

```javascript
{
  "user": {
    "username": "xxx",
    "mobilePhoneNumber": "xxxx",
    "mobilePhoneVerified": true,
    "emailVerified": false,
    "objectId": "xxxxx",
    "createdAt": "2016-12-08T15:16:36.646Z",
    "updatedAt": "2016-12-08T15:16:36.646Z"
  },
  "token": "xxxxx"
}
```
