#Web Service 接口
##获取用户信息
###接口连接

> https://serverdomain_or_ip/user/[gemsuid]/[idcardnum]
> 例：

> 根据D8账号获取用户信息:

> https://serverdomain/user/d8abcde

>根据D8账号和身份证号获取用户信息

>https://serverdomain/user/d8abcde/110101198001021234

####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| gemsuid     |          是 |  D8账号      |
| idcardnum   |          否 |  身份证号      |

####返回结果
```javascript
{
    "UserID": 144915,
    "GEMSUID": "D8XIWYAN",
    "FirstNameCn": "希望",
    "LastNameCn": "闫",
    "Birthday": "1988-08-12",
    "Gender": "M",
    "Status": 1
}
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| UserID     |用户ID      |
| GEMSUID     |D8账号      |
| FirstNameCn   | 名      |
| LastNameCn   | 姓       |
| Birthday   | 生日      |
| Gender   | 性别：M/F      |
| Status   | 状态,-1停用,1正常      |

##获取经销商用户信息
###接口连接

> https://serverdomain_or_ip/dealeruser/[userid]
> 例：

> 根据D8账号获取用户信息:

> https://serverdomain/dealeruser/129092


####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| userid     |          是 |  用户ID      |

####返回结果
```javascript
[{
    "Email": "dic@bstd-benz.com",
    "Phone": "",
    "Fax": "",
    "DepartmentID": "1",
    "PositionID": "2",
    "Status": 1,
    "DealerID": 50,
    "DealerGroupID": 2
},{},...]

```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| Email     |邮箱      |
| Phone     |电话      |
| Fax   | 传真      |
| DepartmentID   | 部门ID  |
| PositionID   | 职位ID |
| DealerID   | 经销商ID |
| DealerGroupID   | 经销商集团ID |
| Status   | 状态,-1停用,1正常      |

##根据经销商ID获取经销商信息
###接口连接
  https://serverdomain_or_ip/dealer/[dealerid]
  例：
  根据ID获取经销商信息:
  https://serverdomain/dealer/123

####参数
| 字段名        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| dealerid     |          是 |  经销商ID      |

####返回结果说明
```javascript
{
	"DealerID":123,
	"DealerCode":"EHZL13",
	"DealerNameCn":"杭州东星行汽车维修有限公司建国中路分公司",
	"DealerNameEn":"Hangzhou Eastern Star Automobile Service Co., Ltd Jianguo Zhong Road Branch",
	"DealerShortNameCn":"杭州东星行建国中路分公司",
	"DealerShortNameEn":"Hangzhou Eastern Star Automobile Service Co., Ltd Jianguo Zhong Road Branch",
	"CityName":"杭州",
	"ProvinceName":"浙江",
	"Region":"南",
	"ZipCode":"123456",
	"OperatingAddressCn":"建国中路21号",
	"OperatingAddressEn":"No. 21 Jianguo Zhong Road",
	"Fax":"8657187706661",
	"Phone":"8657187706662",
	"Email":"anhuistar@anhuistar-benz.com",
	"Status":1
}
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| DealerID     |经销商ID      |
| DealerCode   | 经销商代码      |
| DealerNameCn   | 经销商中文名称       |
| DealerNameEn   | 经销商英文名称      |
| DealerShortNameCn   | 简称中文      |
| DealerShortNameEn   | 简称英文      |
| CityName   | 市      |
| ProvinceName   | 省      |
| Region   | 邮编      |
| ZipCode   | 职位ID      |
| OperatingAddressCn   | 地址中文      |
| OperatingAddressEn   | 地址英文      |
| Fax   | 传真      |
| Phone   | 电话      |
| Email   | 邮箱      |
| Status   | 状态,-1停用,1正常      |

##根据经销商集团ID获取经销商信息
###接口连接
  https://serverdomain_or_ip/dealerlist/[dealergroupid]
  例：
  根据ID获取经销商信息:
  https://serverdomain/dealerlist/1022

####参数
| 字段名        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| dealerid     |          是 |  经销商集团ID      |

####返回结果说明
```javascript
[{
	"DealerID":123,
	"DealerCode":"EHZL13",
	"DealerNameCn":"杭州东星行汽车维修有限公司建国中路分公司",
	"DealerNameEn":"Hangzhou Eastern Star Automobile Service Co., Ltd Jianguo Zhong Road Branch",
	"DealerShortNameCn":"杭州东星行建国中路分公司",
	"DealerShortNameEn":"Hangzhou Eastern Star Automobile Service Co., Ltd Jianguo Zhong Road Branch",
	"CityName":"杭州",
	"ProvinceName":"浙江",
	"Region":"南",
	"ZipCode":"123456",
	"OperatingAddressCn":"建国中路21号",
	"OperatingAddressEn":"No. 21 Jianguo Zhong Road",
	"Fax":"8657187706661",
	"Phone":"8657187706662",
	"Email":"anhuistar@anhuistar-benz.com",
	"Status":1
},...]
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| DealerID     |经销商ID      |
| DealerCode   | 经销商代码      |
| DealerNameCn   | 经销商中文名称       |
| DealerNameEn   | 经销商英文名称      |
| DealerShortNameCn   | 简称中文      |
| DealerShortNameEn   | 简称英文      |
| CityName   | 市      |
| ProvinceName   | 省      |
| Region   | 邮编      |
| ZipCode   | 职位ID      |
| OperatingAddressCn   | 地址中文      |
| OperatingAddressEn   | 地址英文      |
| Fax   | 传真      |
| Phone   | 电话      |
| Email   | 邮箱      |
| Status   | 状态,-1停用,1正常      |

##获取经销商集团
###接口连接
> https://serverdomain_or_ip/dealergroup
> 例：
> 根据ID获取经销商信息:
> https://serverdomain/dealergroup


####返回结果说明
```javascript
[{
    "GroupID": 1, 
    "GroupNameCn": "LSH", 
    "GroupNameEn": "LSH", 
    "Status": 1
},{}...]
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| GroupID     |经销商集团ID      |
| GroupNameCn   | 经销商代码      |
| GroupNameEn   | 经销商集团英文名称       |
| Status   | 状态:(0:停用、1:正常)      |

##获取部门接口
###接口连接
> https://serverdomain_or_ip/department

> 例：

> 根据ID获取经销商信息:

> https://serverdomain/department

####返回结果说明
```javascript
[
    "DepartmentID": 1, 
"DepartmentNameCn": "售后部", 
    "DepartmentNameEn": "After Sales Department", 
},{}...]
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| DepartmentID     |部门ID      |
| DepartmentNameCn   | 部门名称中文      |
| DepartmentNameEn   | 部门名称英文       |

##获取职位接口
###接口连接
> https://serverdomain_or_ip/position

> 例：

> 根据ID获取经销商信息:

> https://serverdomain/position

####返回结果说明
```javascript
[{
    "PositionID":1,
    "DepartmentID": 1, 
    "PositionNameCn": "配件经理", 
    "PositionNameEn": "Parts Manager", 
},{}...]
```
####返回结果说明
| Key        | 说明                  |
| :--------  | :------------------: |
| PositionID     |职位ID      |
| DepartmentID   | 部门ID      |
| PositionNameCn   | 职位名称中文       |
| PositionNameEn   | 职位名称英文       |
