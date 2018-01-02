# 目录
## 基础api
##### 1. [登录(login)](#1-登录)
##### 2. [注册(register)](#2-注册)
##### 3. [发送验证码(requestSendVerifyCode)](#3-发送验证码)
##### 4. [修改支付密码(setPaymentPassword)](#4-修改支付密码)
##### 5. [修改登录密码(findPassword)](#5-修改登录密码)
##### 6. [获取账户余额(getRemainAmount)](#6-获取账户余额)
##### 7. [账户充值(recharge)](#7-账户充值)
##### 8. [账户提现(withdraw)](#8-账户提现)
##### 9. [获取个人信息(getPersonalInfo)](#9-获取个人信息)
##### 10. [修改个人信息(modifyPersonalInfo)](#10-修改个人信息)
##### 11. [修改密码(modifyPassword)](#11-修改密码)
##### 12. [意见反馈(submitFeedback)](#12-意见反馈)
##### 13. [获取中国区划地址(getRegionAddress)](#13-获取中国区划地址)
##### 14. [获取发货点地址(getStartPointAddress)](#14-获取发货点地址)
## 搬运队api
##### 15. [搬运队获取待扫描货车(getWaitScanTruckInfo)](#15-搬运队获取待扫描货车)
##### 16. [搬运队获取搬运历史(getCarryList)](#16-搬运队获取搬运历史)
##### 17. [搬运队修改搬运部信息(modifyOwnPartment)](#17-搬运队修改搬运部信息)
##### 18. [搬运部获取当前搬运货车信息(getWorkTruckInfo)](#18-搬运部获取当前搬运货车信息)
## 司机api
##### 19. [司机获取当前运输中的货车信息(getOnWayTruck)](#19-司机获取当前运输中的货车信息)
##### 20. [司机上传位置信息(uploadLocation)](#20-司机上传位置信息)
##### 21. [司机确认到达(confirmReach)](#21-司机确认到达)
##### 22. [司机获取位置列表(getLocationList)](#22-司机获取位置列表)
## 分店api
##### 23. [总部确认卡车认证通过(passExamineTruck)](#23-总部确认卡车认证通过)
##### 24. [库管扫描入库(placeStorage)](#24-库管扫描入库)
##### 25. [董事长修改参数(modifySettingInfo)](#25-董事长修改参数)
##### 26. [收货部获取需要上传照片的订单(getLastestOrderByReceivePartment)](#26-收货部获取需要上传照片的订单)
##### 27. [收货部为货单上传照片(setPhotoForOriginOrder)](#27-收货部为货单上传照片)
##### 28. [收货部为货单下中转单(placeTransferOrder)](#28-收货部为货单下中转单)
##### 29. [收货部获取货单详情(getOrderDetailByReceivePartment)](#29-收货部获取货单详情)
##### 30. [收货部获取订单(getOrdersByReceivePartment)](#30-收货部获取订单)
##### 31. [库管部获取订单(getOrdersByWareHousePartment)](#31-库管部获取订单)
##### 32. [库管部获取正在装车的订单列表(getLoadingOrderList)](#32-库管部获取正在装车的订单列表)
##### 33. [库管部扫描入库(placeStorage)](#33-库管部扫描入库)
##### 34. [保安部检查卡车状态(checkTruckPass)](#34-保安部检查卡车状态)
##### 35. [分店获取成员列表(getMemberList)](#35-分店获取成员列表)
##### 36. [分店创建成员(createMember)](#36-分店创建成员)
##### 37. [分店创建成员(modifyMember)](#37-分店创建成员)
##### 38. [分店获取部门信息(getOwnPartmentInfo)](#38-分店获取部门信息)
##### 39. [获取统计信息(getStatistics)](#39-获取统计信息)
## 协议文档
##### 40. [用户协议(user)](#40-用户协议)
##### 41. [获取软件许可协议(software)](#41-获取软件许可协议)
##### 42. [关于(about)](#42-关于)

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

### 7. [账户充值](#7-账户充值recharge)
- `recharge`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| amount | Number | 充值金额 |
| thirdpartyAccount | Number | 充值账户平台（第三方的账号  0：支付宝(A)， 1：财付通(C)，2：工商银行(G)，3：建设银行(J)， 4：中国银行（Z）， 5：农业银行(N)，规则，给定的缩写字母+账号） |


```js
{
  "success": true,
  "context": {
    "amount": 99097
  }
}
```

---

### 8. [账户提现](#8-账户提现withdraw)
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

### 9. [获取个人信息](#9-获取个人信息getpersonalinfo)
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

### 10. [修改个人信息](#10-修改个人信息modifypersonalinfo)
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

### 11. [修改密码](#11-修改密码modifypassword)
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

### 12. [意见反馈](#12-意见反馈submitfeedback)
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


### 13. [获取中国区划地址](#13-获取中国区划地址getregionaddress)
- `getRegionAddress`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| parentCode | Number | 上级编码 |
| type | Number | 0:长途地址,1:短途地址 |

```js
{
  "success": true,
  "context": {
    "addressList": [
      {
        "id": 1,
        "code": 11,
        "parentCode": 0,
        "name": "北京市",
        "level": 1
      }
    ]
  }
}
```
---

### 14. [获取发货点地址](#14-获取发货点地址getstartpointaddress)
- `getStartPointAddress`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| parentCode | Number | 上级编码 |
| region | String | 区划地址 |

```js
{
  "success": true,
  "context": {
    "addressList": [
      {
        "name": "华通物流超市",
        "address": {
          "name": "贵阳市石板镇"
        },
        "id": "59841315ad007024a2c0ce9b",
        "isShop": true
      }
    ]
  }
}
```

---

## 搬运队api

---
### 15. [搬运队获取待扫描货车](#15-搬运队获取待扫描货车getwaitscantruckinfo)
- `getWaitScanTruckInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "truckList": [
      {
        "plateNo": "贵A-778899",
        "drivingLicense": "A71236717",
        "createTime": "2017-08-30 17:22:07",
        "totalWeight": 10,
        "orderCount": 1,
        "id": "59a683bf48382f73b5977cb7"
      }
    ]
  }
}
```

---
### 16. [搬运队获取搬运历史](#16-搬运队获取搬运历史getcarrylist)
- `getCarryList`
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
    "count": 6,
    "truckList": [
      {
        "plateNo": "贵A-778899",
        "drivingLicense": "A71236717",
        "createTime": "2017-08-30 17:22:59",
        "totalWeight": 10,
        "orderCount": 1,
        "id": "59a683f391f69d7410de75e1"
      },
      {
        "plateNo": "123",
        "drivingLicense": "123",
        "createTime": "2017-08-25 16:12:43",
        "totalWeight": 10,
        "orderCount": 1,
        "id": "599fdbfb0db48253c419d810"
      },
      {
        "plateNo": "1234",
        "drivingLicense": "123456789",
        "createTime": "2017-08-25 16:09:07",
        "totalWeight": 10,
        "orderCount": 1,
        "id": "599fdb23ff2ce453630e6e11"
      }
    ]
  }
}
```

---
### 17. [搬运队修改搬运部信息](#17-搬运队修改搬运部信息modifyownpartment)
- `modifyOwnPartment`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| price | Number | 单价 |
| enable | Bool | 是否在线 |

```js
{
  "success": true,
  "context": {
    "name": "搬运部",
    "descript": "我们活着的意义就是移动",
    "phoneList": "0851-98989000;0851-98989001",
    "price": 100,
    "enable": true,
    "chargeMan": {
      "phone": "18385192480",
      "name": "搬运工负责人",
      "id": "59954970d1df03410425a91c",
      "phoneList": ""
    },
    "id": "59954970d1df03410425a91d"
  }
}
```

---
### 18. [搬运部获取当前搬运货车信息](#18-搬运部获取当前搬运货车信息getworktruckinfo)
- `getWorkTruckInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "shipperId": "59954973d1df03410425a946",
    "shopId": "5995496cd1df03410425a904",
    "plateNo": "贵A-778899",
    "drivingLicense": "A71236717",
    "truckType": "4.5米 高栏",
    "driverId": "599575cc277608472d636e97",
    "carryPartmentId": "599641b27338534997932c45",
    "createTime": "2017-08-31 08:44:45",
    "unloadAllOrderList": [],
    "totalSize": 0,
    "totalWeight": 0,
    "totalNumbers": 0,
    "orderCount": 0,
    "orderList": [],
    "state": 3,
    "locationList": [],
    "insuanceMount": 1000000,
    "carryPrice": 100,
    "id": "59a75bfd4b0e7a4e17cde5da"
  }
}
```

---

## 司机api

---
### 19. [司机获取当前运输中的货车信息](#19-司机获取当前运输中的货车信息getonwaytruck)
- `getOnWayTruck`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "shipperId": "59954973d1df03410425a946",
    "shopId": "5995496cd1df03410425a904",
    "plateNo": "贵AA1234",
    "drivingLicense": "1234567890123",
    "truckType": "5.5米平板",
    "driverId": "599575cc277608472d636e97",
    "carryPartmentId": "59954970d1df03410425a91d",
    "scannerId": "59954972d1df03410425a928",
    "createTime": "2017-08-25 15:03:56",
    "unloadAllOrderList": [],
    "totalSize": 1.4,
    "totalWeight": 14,
    "totalNumbers": 5,
    "orderCount": 1,
    "orderList": [
      "599e7fabead9861cc2a8e213"
    ],
    "state": 7,
    "locationList": [],
    "insuanceMount": 100000,
    "carryPrice": 100,
    "id": "599fcbdc89a721507f4a990c"
  }
}
```

---
### 20. [司机上传位置信息](#20-司机上传位置信息uploadlocation)
- `uploadLocation`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| address | String | 地址 |
| longitude | ID | 经度 |
| latitude | ID | 维度 |

```js
{
  "success": true
}
```

---
### 21. [司机确认到达](#21-司机确认到达confirmreach)
- `confirmReach`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true
}
```

---
### 22. [司机获取位置列表](#22-司机获取位置列表getlocationlist)
- `getLocationList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "locationList": [
    {
      "time": "2017-09-08 14:32:53",
      "latitude": 26.561979,
      "longitude": 106.684821,
      "address": "贵州省贵阳市南明区花果园街道花果园L1区"
    },
    {
      "time": "2017-09-08 14:29:33",
      "latitude": 26.561979,
      "longitude": 106.684821,
      "address": "贵州省贵阳市南明区花果园街道花果园L1区"
    }
  ]
}
```

---

## 分店api

---
### 23. [总部确认卡车认证通过](#23-总部确认卡车认证通过passexaminetruck)
- `passExamineTruck`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| truckId | ID | 卡车Id |

```js
{
  "success": true
}

```

---
### 24. [库管扫描入库](#24-库管扫描入库placestorage)
- `placeStorage`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| orderId | ID | 订单Id |
| count | Number | 货物件数 |

```js
{
  "success": true,
  "order": {
    "storeScannerId": "59954970d1df03410425a91a",
    "shopId": "5995496cd1df03410425a904",
    "senderId": "59954981d1df03410425a951",
    "receiverId": "59954981d1df03410425a952",
    "receiverName": "18885192481",
    "endPoint": "北京市东城区景山街道",
    "endPointLastCode": 110101002,
    "receivePartmentId": "59954970d1df03410425a917",
    "receiveMemberId": "59954970d1df03410425a916",
    "roadmapId": "59954975d1df03410425a94c",
    "shipperChairManId": "59954972d1df03410425a928",
    "shipperId": "59954973d1df03410425a946",
    "createTime": "2017-08-17 15:45:05",
    "stateList": [
      {
        "state": 5,
        "count": 1,
        "_id": "59954d7dd1df03410425a95e"
      },
      {
        "state": 4,
        "count": 4,
        "_id": "59954982d1df03410425a95a"
      }
    ],
    "needPayInsuanceFee": 0,
    "needPayTransportFee": 1200,
    "proxyChargeProfit": 0,
    "proxyCharge": 0,
    "designatedFee": 0,
    "totalDesignatedFee": 1200,
    "realFee": 1200,
    "branchProfit": 100,
    "masterProfit": 100,
    "fee": 1000,
    "payTool": 0,
    "payMode": 2,
    "isReachPay": false,
    "insuanceFee": 0,
    "insuanceMount": 0,
    "isInsuance": false,
    "isSendToDoor": false,
    "size": 1,
    "weight": 10,
    "totalNumbers": 5,
    "roadmapRankIndex": 0,
    "isSenderRepresentShipper": false,
    "id": "59954981d1df03410425a953"
  }
}
```

---
### 25. [董事长修改参数](#25-董事长修改参数modifysettinginfo)
- `modifySettingInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| sizeWeightRate | number | 方量重量比 |
| insuanceRate | number | 保险费与保价的比 |
| insuanceMountRate | number | 保价与运费的比 |
| insuanceBaseValue | number | 保险的保底值 |
| proxyChargeProfitRate | number | 手续费与代收货款的比 |
| gradientPriceList | array | 阶梯价格的梯度 |
| additionalDeliverTime | number | 代签额外增加时间 |
| noticeShipperStorageWeight | number | 通知物流公司的吨数 |
| bondAmountWeightRate | number | 每吨货需要的保证金 |
| rankedMaskFirstRankWeight | number | 屏蔽物流公司货物的基数 |
| rankedMaskRateList | array | 屏蔽物流公司排名的梯度 |

```js
{
    "success": true,
}
```

---
### 26. [收货部获取需要上传照片的订单](#26-收货部获取需要上传照片的订单getlastestorderbyreceivepartment)
- `getLastestOrderByReceivePartment`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "shopId": "5995496cd1df03410425a904",
    "receiverName": "18885192481",
    "endPoint": "北京市东城区东华门街道",
    "endPointLastCode": 110101001,
    "receivePartmentId": "59954970d1df03410425a917",
    "receiveMemberId": "59954970d1df03410425a916",
    "createTime": "2017-08-22 16:09:42",
    "stateList": [
      {
        "state": 0,
        "count": 5,
        "_id": "599be6c68e337d17123e9c1f"
      }
    ],
    "needPayInsuanceFee": 0,
    "needPayTransportFee": 0,
    "proxyChargeProfit": 0,
    "proxyCharge": 0,
    "designatedFee": 0,
    "totalDesignatedFee": 1200,
    "realFee": 0,
    "branchProfit": 0,
    "masterProfit": 0,
    "fee": 0,
    "payTool": 0,
    "payMode": 1,
    "isReachPay": true,
    "insuanceFee": 0,
    "insuanceMount": 0,
    "isInsuance": true,
    "isSendToDoor": true,
    "size": 1,
    "weight": 10,
    "totalNumbers": 5,
    "roadmapRankIndex": -1,
    "isSenderRepresentShipper": false,
    "receiver": {
      "phone": "18885192481",
      "id": "59954981d1df03410425a952"
    },
    "sender": {
      "phone": "18885192480",
      "id": "59954981d1df03410425a951"
    },
    "id": "599be6c68e337d17123e9c1e",
    "state": 0
  }
}
```

---
### 27. [收货部为货单上传照片](#27-收货部为货单上传照片setphotofororiginorder)
- `setPhotoForOriginOrder`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| orderId | ID | 货单Id |
| photo | String | 图片地址 |

```js
{
  "msg": "没有该订单"
}
```

---
### 28. [收货部为货单下中转单](#28-收货部为货单下中转单placetransferorder)
- `placeTransferOrder`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| orderId | ID | 货单Id |
| totalNumbers | Number | 总件数 |
| weight | Number | 重量 |
| size | Number | 方量 |

```js
{
  "success": true,
  "context": {
    "shopId": "5995496fd1df03410425a913",
    "senderId": "59954972d1df03410425a928",
    "receiverId": "59954981d1df03410425a952",
    "receiverName": "18885192481",
    "endPoint": "北京市东城区景山街道",
    "endPointLastCode": 110101002,
    "receivePartmentId": "59954970d1df03410425a919",
    "receiveMemberId": "59954970d1df03410425a918",
    "modifyTime": "2017-09-02 09:20:10",
    "createTime": "2017-09-02 09:20:10",
    "stateList": [
      {
        "state": 0,
        "count": 5,
        "_id": "59aa074ad920502bddbbf7c1"
      }
    ],
    "needPayInsuanceFee": 0,
    "needPayTransportFee": 0,
    "proxyChargeProfit": 0,
    "proxyCharge": 0,
    "designatedFee": 0,
    "totalDesignatedFee": 1200,
    "realFee": 0,
    "branchProfit": 0,
    "masterProfit": 0,
    "fee": 0,
    "payTool": 0,
    "payMode": 0,
    "isReachPay": false,
    "insuanceFee": 0,
    "insuanceMount": 0,
    "isInsuance": false,
    "isSendToDoor": false,
    "size": 1,
    "weight": 50,
    "totalNumbers": 5,
    "roadmapRankIndex": -1,
    "isSenderRepresentShipper": true,
    "isTransferOrder": true,
    "id": "59aa074ad920502bddbbf7c0"
  }
}
```

---
### 29. [收货部获取货单详情](#29-收货部获取货单详情getorderdetailbyreceivepartment)
- `getOrderDetailByReceivePartment`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| orderId | ID | 货单Id |

```js
{
  "success": true,
  "context": {
    "shopId": "5995496cd1df03410425a904",
    "receiverName": "18885192481",
    "endPoint": "北京市东城区景山街道",
    "endPointLastCode": 110101002,
    "receivePartmentId": "59954970d1df03410425a917",
    "receiveMemberId": "59954970d1df03410425a916",
    "modifyTime": "2017-08-31 11:29:54",
    "createTime": "2017-08-31 11:29:54",
    "stateList": [
      {
        "state": 5,
        "count": 5,
        "_id": "59a782b298e48164554806ba"
      }
    ],
    "needPayInsuanceFee": 0,
    "needPayTransportFee": 0,
    "proxyChargeProfit": 0,
    "proxyCharge": 0,
    "designatedFee": 0,
    "totalDesignatedFee": 1200,
    "realFee": 0,
    "branchProfit": 0,
    "masterProfit": 0,
    "fee": 0,
    "payTool": 0,
    "payMode": 0,
    "isReachPay": false,
    "insuanceFee": 0,
    "insuanceMount": 0,
    "isInsuance": false,
    "isSendToDoor": false,
    "size": 1,
    "weight": 10,
    "totalNumbers": 5,
    "roadmapRankIndex": -1,
    "isSenderRepresentShipper": false,
    "receiver": {
      "phone": "18885192481",
      "id": "59954981d1df03410425a952"
    },
    "sender": {
      "phone": "18885192480",
      "id": "59954981d1df03410425a951"
    },
    "isTransferOrder": false,
    "id": "59a782b298e48164554806b7"
  }
}
```

---
### 30. [收货部获取订单](#30-收货部获取订单getordersbyreceivepartment)
- `getOrdersByReceivePartment`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| type | String | 类型 (tostore,stored)|
| keyword | String | 关键字|
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "topay": {
      "count": 0,
      "list": []
    },
    "toprint": {
      "count": 0,
      "list": []
    },
    "tostore": {
      "count": 2,
      "list": [
        {
          "endPoint": "北京市东城区景山街道",
          "stateList": [
            {
              "state": 5,
              "count": 5,
              "_id": "599e7fb2ead9861cc2a8e262"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7fb2ead9861cc2a8e259"
        },
        {
          "endPoint": "北京市东城区景山街道",
          "stateList": [
            {
              "state": 5,
              "count": 5,
              "_id": "599e7fb1ead9861cc2a8e258"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7fb1ead9861cc2a8e24f"
        }
      ]
    },
    "stored": {
      "count": 15,
      "list": [
        {
          "endPoint": "北京市东城区景山街道",
          "stateList": [
            {
              "state": 6,
              "count": 5,
              "_id": "599fea3c0db48253c419d84d"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7fb0ead9861cc2a8e245"
        },
        {
          "endPoint": "北京市东城区景山街道",
          "stateList": [
            {
              "state": 7,
              "count": 5,
              "_id": "599fe94a0db48253c419d83f"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7fafead9861cc2a8e23b"
        },
        {
          "endPoint": "北京市东城区景山街道",
          "stateList": [
            {
              "state": 7,
              "count": 5,
              "_id": "599fe5e50db48253c419d835"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7faeead9861cc2a8e231"
        }
      ]
    }
  }
}

```
---
### 31. [库管部获取订单](#31-库管部获取订单getordersbywarehousepartment)
- `getOrdersByWareHousePartment`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| type | String | 类型 (stored,loaded)|
| keyword | String | 关键字|
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "tostore": {
      "count": 0,
      "list": []
    },
    "stored": {
      "count": 19,
      "list": [
        {
          "endPoint": "北京市东城区景山街道",
          "modifyTime": "2017-08-30 19:07:30",
          "createTime": "2017-08-30 19:07:30",
          "stateList": [
            {
              "state": 6,
              "count": 5,
              "_id": "59a69c8c03819c74dd8d488a"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 0,
          "payMode": 0,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shop": {
            "name": "华通物流超市",
            "address": "贵州省贵阳市南明区花果园街道花果园L2区",
            "id": "5995496cd1df03410425a904"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "59a69c7203819c74dd8d4885"
        },
        {
          "endPoint": "北京市东城区景山街道",
          "modifyTime": "2017-08-31 08:58:21",
          "createTime": "2017-08-28 19:57:48",
          "stateList": [
            {
              "state": 6,
              "count": 5,
              "_id": "59a4053ca655283c6ff39d04"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 0,
          "payMode": 0,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shop": {
            "name": "华通物流超市",
            "address": "贵州省贵阳市南明区花果园街道花果园L2区",
            "id": "5995496cd1df03410425a904"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "59a4053ca655283c6ff39cff"
        },
        {
          "endPoint": "北京市东城区景山街道",
          "modifyTime": "2017-08-31 08:58:21",
          "createTime": "2017-08-24 15:26:42",
          "stateList": [
            {
              "state": 6,
              "count": 5,
              "_id": "59a62763477dfaa641c83e89"
            }
          ],
          "needPayInsuanceFee": 0,
          "needPayTransportFee": 48,
          "payMode": 2,
          "size": 1,
          "weight": 10,
          "totalNumbers": 5,
          "receiveMember": {
            "phone": "18185192480",
            "name": "收货部负责人",
            "id": "59954970d1df03410425a916"
          },
          "shipper": {
            "name": "广顺达物流公司",
            "id": "59954973d1df03410425a946"
          },
          "shop": {
            "name": "华通物流超市",
            "address": "贵州省贵阳市南明区花果园街道花果园L2区",
            "id": "5995496cd1df03410425a904"
          },
          "receiver": {
            "phone": "18885192481",
            "id": "59954981d1df03410425a952"
          },
          "sender": {
            "phone": "18885192480",
            "id": "59954981d1df03410425a951"
          },
          "id": "599e7fb2ead9861cc2a8e259"
        }
      ]
    }
  }
}
```
---
### 32. [库管部获取正在装车的订单列表](#32-库管部获取正在装车的订单列表getloadingorderlist)
- `getLoadingOrderList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "shipperId": "59954973d1df03410425a946",
    "shopId": "5995496cd1df03410425a904",
    "plateNo": "贵A-778899",
    "drivingLicense": "A71236717",
    "truckType": "4.5米 高栏",
    "driverId": "599575cc277608472d636e97",
    "carryPartmentId": "599641b27338534997932c45",
    "scannerId": "59954972d1df03410425a928",
    "createTime": "2017-08-31 08:44:45",
    "unloadAllOrderList": [
      {
        "endPoint": "北京市东城区景山街道",
        "totalNumbers": 5,
        "receiver": {
          "phone": "18885192481"
        },
        "sender": {
          "phone": "18885192480"
        },
        "id": "59a69c7203819c74dd8d4885",
        "unloadNumber": 4
      }
    ],
    "totalSize": 1.2,
    "totalWeight": 12,
    "totalNumbers": 6,
    "orderCount": 2,
    "orderList": [
      {
        "endPoint": "北京市东城区景山街道",
        "createTime": "2017-08-31 09:44:41",
        "size": 1,
        "weight": 10,
        "totalNumbers": 5,
        "receiver": {
          "phone": "18885192481",
          "id": "59954981d1df03410425a952"
        },
        "sender": {
          "phone": "18885192480",
          "id": "59954981d1df03410425a951"
        },
        "id": "59a76a0901d61855a2875c12"
      },
      {
        "endPoint": "北京市东城区景山街道",
        "createTime": "2017-08-30 19:07:30",
        "size": 1,
        "weight": 10,
        "totalNumbers": 5,
        "receiver": {
          "phone": "18885192481",
          "id": "59954981d1df03410425a952"
        },
        "sender": {
          "phone": "18885192480",
          "id": "59954981d1df03410425a951"
        },
        "id": "59a69c7203819c74dd8d4885"
      }
    ],
    "state": 4,
    "locationList": [],
    "insuanceMount": 1000000,
    "carryPrice": 100,
    "id": "59a75bfd4b0e7a4e17cde5da"
  }
}
```

---
### 33. [库管部扫描入库](#33-库管部扫描入库placestorage)
- `placeStorage`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| orderId | ID | 货单Id |
| count | Number | 数量 |

```js
{
  "success": true,
  "order": {
    "shopId": "5995496cd1df03410425a904",
    "senderId": "59954981d1df03410425a951",
    "receiverId": "59954981d1df03410425a952",
    "receiverName": "18885192481",
    "endPoint": "北京市东城区景山街道",
    "endPointLastCode": 110101002,
    "receivePartmentId": "59954970d1df03410425a917",
    "receiveMemberId": "59954970d1df03410425a916",
    "roadmapId": "599d22fec71183033861fd74",
    "shipperChairManId": "59954972d1df03410425a928",
    "shipperId": "59954973d1df03410425a946",
    "storeScannerId": "59954970d1df03410425a91a",
    "createTime": "2017-08-24 15:26:41",
    "stateList": [
      {
        "state": 6,
        "count": 1,
        "_id": "59a405d0a655283c6ff39d05"
      },
      {
        "state": 5,
        "count": 4,
        "_id": "599e7fb1ead9861cc2a8e258"
      }
    ],
    "needPayInsuanceFee": 0,
    "needPayTransportFee": 48,
    "proxyChargeProfit": 0,
    "proxyCharge": 0,
    "designatedFee": 0,
    "totalDesignatedFee": 1200,
    "realFee": 48,
    "branchProfit": 4,
    "masterProfit": 4,
    "fee": 40,
    "payTool": 0,
    "payMode": 2,
    "isReachPay": false,
    "insuanceFee": 0,
    "insuanceMount": 0,
    "isInsuance": false,
    "isSendToDoor": false,
    "size": 1,
    "weight": 10,
    "totalNumbers": 5,
    "roadmapRankIndex": 0,
    "isSenderRepresentShipper": false,
    "id": "599e7fb1ead9861cc2a8e24f"
  }
}
```

### 34. [保安部检查卡车状态](#34-保安部检查卡车状态checktruckpass)
- `checkTruckPass`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| driverId | ID | 司机Id |

```js
{
  "success": true,
  "context": {
    "isEnter": true,
    "driver": {
      "phone": "18985192480",
      "email": "42550564@qq.com",
      "name": "方运江",
      "head": "http://192.168.1.111:3000/api/image?id=599577a97aad4147a4f845db",
      "birthday": "1982-02-25",
      "address": "贵州省贵阳市",
      "license": "599577a97aad4147a4f845db",
      "licenseNo": "123123123",
      "registerTime": "2017-08-17 18:54:04",
      "sex": 0,
      "age": 35,
      "id": "599575cc277608472d636e97"
    }
  }
}
```

### 35. [分店获取成员列表](#35-分店获取成员列表getmemberlist)
- `getMemberList`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| keyword | String | 关键字|
| pageNo | Number | 页码 |
| pageSize | Number | 每一页大小 |

```js
{
  "success": true,
  "context": {
    "count": 1,
    "memberList": [
      {
        "phone": "18085192480",
        "name": "方运江",
        "post": "董事长",
        "authority": [
          0,
          1,
          2,
          3,
          4,
          5,
          6,
          7,
          8,
          10000,
          10001,
          10002,
          10003,
          10004,
          10005,
          10006,
          10007
        ],
        "id": "5995496ad1df03410425a8f2"
      }
    ]
  }
}
```

### 37. [分店创建成员](#37-分店创建成员modifymember)
- `createMember`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| name | String | 成员名|
| phone | String | 成员手机|
| authority | Array | 成员权限 |

```js
{
  "success": true,
  "context": {
    "name": "王小二",
    "phone": "13312341234",
    "authority": [
      10000,
      10001
    ],
    "id": "59a8f7792bdb4d2ef77b63e5"
  }
}
```

### 37. [分店创建成员](#37-分店创建成员modifymember)
- `modifyMember`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| memberId | ID | 成员Id |
| name | String | 成员名|
| phone | String | 成员手机|
| authority | Array | 成员权限 |

```js
{
  "success": true,
  "context": {
    "name": "王小三",
    "phone": "13312341234",
    "authority": [
      10000,
      10002
    ],
    "id": "59a8f7792bdb4d2ef77b63e5"
  }
}
```

### 38. [分店获取部门信息](#38-分店获取部门信息getownpartmentinfo)
- `getOwnPartmentInfo`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |

```js
{
  "success": true,
  "context": {
    "shopId": "5995496cd1df03410425a904",
    "name": "库管部",
    "type": 1,
    "descript": "看家我最在行",
    "phoneList": "0851-98989000;0851-98989001",
    "isBusy": false,
    "createTime": "2017-08-17 15:44:48",
    "enable": false,
    "memberCount": 1,
    "chargeMan": {
      "phone": "18285192480",
      "name": "库管部负责人",
      "id": "59954970d1df03410425a91a"
    },
    "id": "59954970d1df03410425a91b"
  }
}
```

---

### 39. [获取统计信息](#39-获取统计信息getstatistics)
- `getStatistics`
- 请求方式：`POST`

| 参数名称 | 参数类型  | 描述 |
| :- |:-:| :-:|
| userId | ID | 用户Id |
| shopId | ID | 分店Id |

```js
{
  "success": true,
  "context": {
    "branchProfit" : [0, 0, 0, 0, 0, 0, 0],
  "count": [1, 0, 0, 0, 0, 0, 0],
  "insuanceFee": [0, 0, 0, 0, 0, 0, 0],
  "insuanceMount": [0, 0, 0, 0, 0, 0, 0],
  "isInsuance": [0, 0, 0, 0, 0, 0, 0],
  "isReachPay": [0, 0, 0, 0, 0, 0, 0],
  "masterProfit": [0, 0, 0, 0, 0, 0, 0],
  "proxyCharge": [0, 0, 0, 0, 0, 0, 0],
  "realFee": [1, 0, 0, 0, 0, 0, 0],
  "size": [1, 0, 0, 0, 0, 0, 0],
  "totalDesignatedFee": [0, 0, 0, 0, 0, 0, 0],
  "weight": [1, 0, 0, 0, 0, 0, 0],
  }
}
```


---
## 协议文档

---

### 40. [用户协议](#40-用户协议user)
- `user`
- url: `protocals/user.html`

---

### 41. [获取软件许可协议](#41-获取软件许可协议software)
- `software`
- url: `protocals/software.html`

---

### 42. [关于](#42-关于about)
- `about`
- url: `protocals/about.html`
