# 目录
## 基础api
##### 1. [登录(login)](#1-登录)
##### 2. [注册(register)](#2-注册)
##### 3. [发送验证码(requestSendVerifyCode)](#3-发送验证码)
##### 4. [修改支付密码(setPaymentPassword)](#4-修改支付密码)
##### 5. [修改登录密码(findPassword)](#5-修改登录密码)
##### 6. [获取账户余额(getRemainAmount)](#6-获取账户余额)
##### 7. [货主账户提现(withdraw)](#7-货主账户提现)
##### 8. [获取个人信息(getPersonalInfo)](#8-获取个人信息)
##### 9. [修改个人信息(modifyPersonalInfo)](#9-修改个人信息)
##### 10. [修改密码(modifyPassword)](#10-修改密码)
##### 11. [意见反馈(submitFeedback)](#11-意见反馈)
##### 12. [获取交易记录列表(getBillList)](#12-获取交易记录列表)
##### 13. [获取交易记录(getBills)](#13-获取交易记录)
##### 14. [业务员获取下级列表(getSuborList)](#14-业务员获取下级列表)
##### 15. [检查客户状态(checkCustomerPhone)](#15-检查客户状态)
##### 16. [给客户打电话(callVisitCustomer)](#16-给客户打电话)
##### 17. [添加客户(addCustomer)](#17-添加客户)
##### 18. [获取业务员名字(getUserNameByPhone)](#18-获取业务员名字)
##### 19. [获取收到的通知数(getNotifyCount)](#19-获取收到的通知数)
##### 20. [获取通知列表(getNotifyList)](#20-获取通知列表)
##### 21. [读通知(readNotify)](#21-读通知)
##### 22. [业务员申请成为上级(requestBecomeSuperior)](#22-业务员申请成为上级)
##### 23. [回应业务员申请成为我的上级(answerBecomeSubor)](#23-回应业务员申请成为我的上级)
##### 24. [获取客户列表(getCustomers)](#24-获取客户列表)
## 协议文档
##### 25. [用户协议(user)](#25-用户协议)
##### 26. [获取软件许可协议(software)](#26-获取软件许可协议)
##### 27. [关于(about)](#27-关于)

---

## 基础api

---

### 1. [登录](#1-登录login)
- `login`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| phone | String | 登录手机号码 |
| password | String | 登录密码 |

```js
{
    "success": true,
    "context": {
        "userId": "10000"
    }
}
```

---


### 2. [注册](#2-注册register)
- `register`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| phone | String | 登录手机号码 |
| email | String | 找回密码的邮箱 |
| password | String | 登录密码 |


```js
{
    "success": true
}
```

---
### 3. [发送验证码](#3-发送验证码requestsendverifycode)
- `requestSendVerifyCode`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| phone | String | 登录手机号码 |

```js
{
    "success": true
}
```

---

### 4. [修改支付密码](#4-修改支付密码setpaymentpassword)
- `setPaymentPassword`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 登录手机号码 |
| password | String | 新密码 |
| verifyCode | String | 验证码 |


```js
{
    "success": true
}
```

---
### 5. [修改登录密码](#5-修改登录密码findpassword)
- `findPassword`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 登录手机号码 |
| password | String | 新密码 |
| verifyCode | String | 验证码 |

```js
{
    "success": true
}
```

---

### 6. [获取账户余额](#6-获取账户余额getremainamount)
- `getRemainAmount`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |


```js
{
  "success": true,
  "context": {
    "amount": 98800
  }
}
```


---


### 7. [货主账户提现](#7-货主账户提现withdraw)
- `withdraw`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| amount | Number | 提现金额 |
| thirdpartyAccount | Number | 提现账户平台（第三方的账号  0：支付宝(A)， 1：财付通(C)，2：工商银行(G)，3：建设银行(J)， 4：中国银行（Z）， 5：农业银行(N)，规则，给定的缩写字母+账号） |


```js
{
  "success": true,
  "context": {
    "amount": 99097
  }
}
```

---

### 8. [获取个人信息](#8-获取个人信息getpersonalinfo)
- `getPersonalInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |


```js
{
  "success": true,
  "context": {
    "phone": "13712341230",
    "starLevel": 0,
    "name": "业务员0",
    "joinTime": "2017-12-15T01:05:09.330Z",
    "superiorId": "5a331fc159bbe877c873f166",
    "registerTime": "2017-12-15 09:05:04",
    "dropStarLevel": 0,
    "appraiseStarLevel": 0,
    "businessStarLevel": 0,
    "suborCount": 0,
    "isSetPaymentPassword": 1,
    "sex": 0,
    "userId": "5a331fc059bbe877c873f160"
  }
}

```
---

### 9. [修改个人信息](#9-修改个人信息modifypersonalinfo)
- `modifyPersonalInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 登录手机号码 |
| name | String | 用户名 |
| head | String | 头像 |


```js
{
    "success": true,
}
```

---

### 10. [修改密码](#10-修改密码modifypassword)
- `modifyPassword`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| oldPassword | String | 旧密码 |
| newPassword | String | 新密码 |

```js
{
    "success": true,
}
```

---

### 11. [意见反馈](#11-意见反馈submitfeedback)
- `submitFeedback`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| content | String | 内容 |
| email | String | 联系邮箱 |

```js
{
    "success": true,
}
```

---

### 12. [获取交易记录列表](#12-获取交易记录列表getbilllist)
- `getBillList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "count": 1,
    "billList": [
      {
        "tradeAmountYuan": 100000,
        "tradeTime": "2017-08-08 19:43:09",
        "tradeAmount": 10000000,
        "thirdpartyAccount": "A支付宝测试账号",
        "orderId": null,
        "remark": "个人充值"
      }
    ]
  }
}

```

---

### 13. [获取交易记录](#13-获取交易记录getbills)
- `getBills`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| type | String | income,withdraw |
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "withdraw": {
      "count": 0,
      "list": []
    },
    "income": {
      "count": 0,
      "list": []
    }
  }
}

```

---

### 14. [业务员获取下级列表](#14-业务员获取下级列表getsuborlist)
- `getSuborList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| type | String | normal,history,public |
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "normal": {
      "list": [
        {
          "suspend": false,
          "id": "5a331fb659bbe877c873f130",
          "name": "发货人0",
          "phone": "13812341200",
          "fixedStarLevel": 3,
          "maxFloatStarLevel": 0,
          "starLevel": 3,
          "suspendTime": null,
          "lastCallTime": "2017-12-15 09:05:09"
        }
      ]
    },
    "history": {
      "list": []
    },
    "public": {
      "list": []
    }
  }
}

```

---

### 15. [检查客户状态](#15-检查客户状态checkcustomerphone)
- `checkCustomerPhone`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 客户手机号 |


```js
{
  "success": true
}

```
---

### 16. [给客户打电话](#16-给客户打电话callvisitcustomer)
- `callVisitCustomer`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 客户手机号 |


```js
{
  "success": true
}

```
---

### 17. [添加客户](#17-添加客户addcustomer)
- `addCustomer`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 客户手机号 |


```js
{
  "success": true
}

```

---

### 18. [获取业务员名字](#18-获取业务员名字getusernamebyphone)
- `getUserNameByPhone`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 业务员手机号 |


```js
{
  "success": true,
  "context": {
      "name": "业务员3"
    }
}

```

---

### 19. [获取收到的通知数](#19-获取收到的通知数getnotifycount)
- `getNotifyCount`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |


```js
{
  "success": true,
  "context": {
    "count": 0
  }
}

```
---

### 20. [获取通知列表](#20-获取通知列表getnotifylist)
- `getNotifyList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| type | Number | 0:接收,1:发送 |
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "notifyList": [
      {
        "type": 30000,
        "data": {
          "superiorId": "5a331fc059bbe877c873f160",
          "superiorName": "业务员0"
        },
        "createTime": "2017-12-18 15:12:11",
        "needFeadback": true,
        "id": "5a376a4bf9ef7148fd1004b8"
      }
    ]
  }
}

```
---

### 21. [读通知](#21-读通知readnotify)
- `readNotify`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| notifyId | ID | 通知Id |


```js
{
  "success": true
}

```
---

### 22. [业务员申请成为上级](#22-业务员申请成为上级requestbecomesuperior)
- `requestBecomeSuperior`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| phone | String | 要发展的业务员手机号 |


```js
{
  "success": true
}

```
---

### 23. [回应业务员申请成为我的上级](#23-回应业务员申请成为我的上级answerbecomesubor)
- `answerBecomeSubor`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| notifyId | ID | 通知Id |
| isOk | Boolean | 是否同意 |


```js
{
  "success": true
}

```

---

### 24. [获取客户列表](#24-获取客户列表getcustomers)
- `getCustomers`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| keyword | String | 关键字 |
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "suborList": [
      {
        "phone": "13712341231",
        "starLevel": 0,
        "name": "业务员1",
        "joinTime": "2017-12-15T01:05:09.281Z",
        "superiorId": "5a331fc259bbe877c873f16c",
        "registerTime": "2017-12-15 09:05:05",
        "dropStarLevel": 0,
        "appraiseStarLevel": 0,
        "businessStarLevel": 0,
        "suborCount": 1,
        "isSetPaymentPassword": 1,
        "sex": 0,
        "id": "5a331fc159bbe877c873f166"
      }
    ]
  }
}

```

---
## 协议文档

---

### 25. [用户协议](#25-用户协议user)
- `user`
- url: `protocals/user.html`

---

### 26. [获取软件许可协议](#26-获取软件许可协议software)
- `software`
- url: `protocals/software.html`

---

### 27. [关于](#27-关于about)
- `about`
- url: `protocals/about.html`
