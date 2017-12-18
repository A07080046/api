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
##### 12. [货主获取交易记录(getBillList)](#12-货主获取交易记录)
## 协议文档
##### 13. [用户协议(user)](#13-用户协议)
##### 14. [获取软件许可协议(software)](#14-获取软件许可协议)
##### 15. [关于(about)](#15-关于)

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
    "phone": "18685192480",
    "email": "42550564@qq.com",
    "registerTime": "2017-08-08 19:43:00",
    "createTime": "2017-08-17T02:46:25.879Z",
    "authority": [
      {
        "20011": "搬货的权限"
      },
      {
        "10008": "修改所在部门信息的权限"
      },
      {
        "10001": "创建成员的权限"
      },
      {
        "10002": "修改成员信息的权限"
      },
      {
        "10003": "删除成员的权限"
      },
      {
        "10005": "充值的权限"
      },
      {
        "10006": "提现的权限"
      }
    ],
    "sex": 0,
    "partment": {
      "shopId": "5995496cd1df03410425a904",
      "name": "王大搬运部",
      "type": 2,
      "descript": "我们活着的意义就是移动",
      "phoneList": "0851-98989000;0851-98989001",
      "isBusy": false,
      "price": 100,
      "modifyTime": "2017-08-21 12:01:26",
      "workTruckId": "59a75bfd4b0e7a4e17cde5da",
      "createTime": "2017-08-18 09:24:02",
      "enable": true,
      "memberCount": 1,
      "chargeMan": {
        "phone": "18385192481",
        "name": "搬运工负责人",
        "id": "599641b27338534997932c44"
      },
      "id": "599641b27338534997932c45"
    },
    "shipper": {
      "name": "广顺达物流公司",
      "logo": "http://192.168.1.111:3000/api/image?id=5989a3c5b48db929e46ad6c4",
      "image": "http://192.168.1.111:3000/api/image?id=5989a3c5b48db929e46ad6c9",
      "sign": "这是一家非常专业的物流公司",
      "phoneList": "0851-86190987;18185192480",
      "address": "贵阳市花果园",
      "legalName": "方运江",
      "legalPhone": "18085192480",
      "createTime": "2017-08-08 19:43:01",
      "legalIDCard": [
        "http://192.168.1.111:3000/api/image?id=5989a3c5b48db929e46ad6cd",
        "http://192.168.1.111:3000/api/image?id=5989a3c5b48db929e46ad6ca"
      ],
      "acountAmount": 99930000,
      "capital": 10000000,
      "descriptList": [
        {
          "img": "http://192.168.1.111:3000/api/image?id=5989a3c5b48db929e46ad6cc",
          "text": "这是我们公司的车队"
        }
      ],
      "chairMan": {
        "phone": "18685192480",
        "id": "5989a3c4b48db929e46ad6b0",
        "phoneList": ""
      },
      "id": "5989a3c5b48db929e46ad6ce",
      "registerShopList": [
        {
          "shop": {
            "name": "华通物流超市",
            "address": {
              "name": "贵州省贵阳市南明区花果园街道花果园L2区"
            },
            "id": "5989a3c0b48db929e46ad68d"
          },
          "id": "5989a3c6b48db929e46ad6d0"
        }
      ]
    },
    "agent": {
      "name": "18684165865收货点",
      "logo": "http://localhost:3000/api/image?id=59f698e10931cf0b4e8b5262",
      "image": "http://localhost:3000/api/image?id=59f698e70931cf0b4e8b5265",
      "sign": "18684165865收货点18684165865收货点",
      "phoneList": "18684165865",
      "address": "贵州省贵阳市云岩区",
      "location": [
        106.709177,
        26.629907
      ],
      "legalName": "1868416586",
      "legalPhone": "18684165865",
      "createTime": "2017-10-30 11:13:59",
      "legalIDCard": [],
      "descriptList": [],
      "id": "59f698f70931cf0b4e8b5266",
      "chairMan": {
        "phone": "18684165865",
        "id": "59df0a26009deb7e9298e18f"
      },
      "referShop": {
        "name": "15555555501",
        "address": "贵州省贵阳市云岩区黔灵山分店",
        "id": "59e426b1b6ee191fe5d4fbf8"
      }
    },
    "phoneList": "",
    "userId": "5989a3c4b48db929e46ad6b0"
  }
}

```
###### authority的说明：
```
authority为用户权限:
(1)总部权限
    0:创建分店的权限
    1:修改分店信息的权限
    2:删除分店的权限
    3:查看分店列表的权限
    4:修改设置的权限
    5:创建收货点的权限
    6:修改收货点的权限
    7:删除收货点的权限
    8:查看收货点的权限
(2)公共权限
    10000:修改所在物流超市信息的权限
    10001:创建成员的权限
    10002:修改成员信息的权限
    10003:删除成员的权限
    10004:查看成员的权限
    10005:充值的权限
    10006:提现的权限
    10007:修改路线的提成的权限
(3)分店权限
    20000:创建物流公司的权限
    20001:修改物流公司的权限
    20002:删除物流公司的权限
    20003:查看物流公司的权限
    20004:创建部门的权限
    20005:修改部门信息的权限
    20006:删除部门的权限
    20007:查看部门的权限
    20008:收货的权限(收货部人员)
    20009:库管的权限(库管部人员)
    20010:搬货的权限(搬运部人员)
    20011:安检的权限(保安部人员)
    20012:配送的权限(配送部人员)
(4)物流公司
    30000:修改物流公司信息的权限
    30001:修改物流公司成员权限的权限
    30002:创建路线的权限
    30003:修改路线的权限
    30004:删除路线的权限
    30005:查看路线的权限
(5)收货点
    40000:修改收货点信息的权限
    40001:修改收货点成员权限的权限
    40002:收货点下单的权限

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
| position | String | 职位 |


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

### 12. [货主获取交易记录](#12-货主获取交易记录getbilllist)
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
## 协议文档

---

### 13. [用户协议](#13-用户协议user)
- `user`
- url: `protocals/user.html`

---

### 14. [获取软件许可协议](#14-获取软件许可协议software)
- `software`
- url: `protocals/software.html`

---

### 15. [关于](#15-关于about)
- `about`
- url: `protocals/about.html`
