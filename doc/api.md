#DIC数据接口(讨论版)
[TOC]

##Dealer
###获取全部数据接口
        [https://dicserver/API/IDCIDs/dealer?action=getall&page=1](https://dicserver/API/IDCIDs/dealer)
        请求方式：GET
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
| page     |          是 |  当前页      |
####返回结果说明
``` json
{
	totalCount: 10000,
	page: 1,
	pageSize:100,
    key:["DealerID","DealerNo","DealerCode","IMSCode","SAPCode","DealerTypeID","DealerOwnerID","DealerNameCn","DealerNameEn","DealerShortNameCn","DealerShortNameEn","FormatID","FormatCodeID","_formatcode","Format","ProvinceID","CityID","ZipCode","OperatingAddressCn","OperatingAddressEn","FaxCountryNo","FaxAreaNo","FaxNo","PhoneCountryNo","PhoneAreaNo","PhoneNo","SupportPhoneCountryNo","SupportPhoneAreaNo","SupportPhoneNo","Email","HomePage","Status","DealerGroupID","BDC","LeadingGSSN","LeadingDealership","Region"],
	data:[["40","40E6A30F-BA65-41D8-A140-E0BAC79AC190","EHFB10","CN890067","CN914020","6","1001","安徽之星汽车销售服务有限公司","Anhui Star Automobile Sales & Service Co., Ltd.","安徽之星 ","Anhui Star","1","10250","AH 250","AH250/SC11/BP6","1021","103","230011","汴河路国际汽车城4号展厅","International Autotown No.4 Showroom, Bianhe Road","86","551","439 7668","86","551","64397666","86","551","159 5693 3516","anhuistar@anhuistar-benz.com","","1","1027","2","EHFB10","EHFB10","南"],......]
}
``` 

###获取增量数据接口
>[https://dicserver/API/IDCIDs/dealer?action=getupdate&fromtime=123455](https://dicserver/API/IDCIDs/dealer)
>请求方式：GET
>该接口返回自fromtime开始所有有更新或者新增的dealer数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getupdate表示表示获取增量数据      |
| fromtime     |          是 |  起始时间时间戳      |
####返回结果说明
``` json
{
	totalCount: 100,
    key:["DealerID","DealerNo","DealerCode","IMSCode","SAPCode","DealerTypeID","DealerOwnerID","DealerNameCn","DealerNameEn","DealerShortNameCn","DealerShortNameEn","FormatID","FormatCodeID","_formatcode","Format","ProvinceID","CityID","ZipCode","OperatingAddressCn","OperatingAddressEn","FaxCountryNo","FaxAreaNo","FaxNo","PhoneCountryNo","PhoneAreaNo","PhoneNo","SupportPhoneCountryNo","SupportPhoneAreaNo","SupportPhoneNo","Email","HomePage","Status","DealerGroupID","BDC","LeadingGSSN","LeadingDealership","Region"],
	data:[["40","40E6A30F-BA65-41D8-A140-E0BAC79AC190","EHFB10","CN890067","CN914020","6","1001","安徽之星汽车销售服务有限公司","Anhui Star Automobile Sales & Service Co., Ltd.","安徽之星 ","Anhui Star","1","10250","AH 250","AH250/SC11/BP6","1021","103","230011","汴河路国际汽车城4号展厅","International Autotown No.4 Showroom, Bianhe Road","86","551","439 7668","86","551","64397666","86","551","159 5693 3516","anhuistar@anhuistar-benz.com","","1","1027","2","EHFB10","EHFB10","南"],......]
}
``` 

###根据DealerID获取数据接口
>[https://dicserver/API/IDCIDs/dealer?action=getdatabyid&dealerid=39,40,41](https://dicserver/API/IDCIDs/dealer)
>请求方式：GET
>该接口返回自fromtime开始所有有更新或者新增的dealer数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getdatabyid表示表示获取增量数据      |
| dealerid     |          是 |  dealerid,多个ID用“，”分隔      |
####返回结果说明
``` json
{
    totalCount: 3,
    key: ["DealerID", "DealerNo", "DealerCode", "IMSCode", "SAPCode", "DealerTypeID", "DealerOwnerID", "DealerNameCn", "DealerNameEn", "DealerShortNameCn", "DealerShortNameEn", "FormatID", "FormatCodeID", "_formatcode", "Format", "ProvinceID", "CityID", "ZipCode", "OperatingAddressCn", "OperatingAddressEn", "FaxCountryNo", "FaxAreaNo", "FaxNo", "PhoneCountryNo", "PhoneAreaNo", "PhoneNo", "SupportPhoneCountryNo", "SupportPhoneAreaNo", "SupportPhoneNo", "Email", "HomePage", "Status", "DealerGroupID", "BDC", "LeadingGSSN", "LeadingDealership", "Region"],
    data: [["39", "40E6A30F-BA65-41D8-A140-E0BAC79AC190", "EHFB10", "CN890067", "CN914020", "6", "1001", "安徽之星汽车销售服务有限公司", "Anhui Star Automobile Sales & Service Co., Ltd.", "安徽之星 ", "Anhui Star", "1", "10250", "AH 250", "AH250/SC11/BP6", "1021", "103", "230011", "汴河路国际汽车城4号展厅", "International Autotown No.4 Showroom, Bianhe Road", "86", "551", "439 7668", "86", "551", "64397666", "86", "551", "159 5693 3516", "anhuistar@anhuistar-benz.com", "", "1", "1027", "2", "EHFB10", "EHFB10", "南"],
	["40", "40E6A30F-BA65-41D8-A140-E0BAC79AC190", "EHFB10", "CN890067", "CN914020", "6", "1001", "安徽之星汽车销售服务有限公司", "Anhui Star Automobile Sales & Service Co., Ltd.", "安徽之星 ", "Anhui Star", "1", "10250", "AH 250", "AH250/SC11/BP6", "1021", "103", "230011", "汴河路国际汽车城4号展厅", "International Autotown No.4 Showroom, Bianhe Road", "86", "551", "439 7668", "86", "551", "64397666", "86", "551", "159 5693 3516", "anhuistar@anhuistar-benz.com", "", "1", "1027", "2", "EHFB10", "EHFB10", "南"]]
}

``` 
##Province
###获取全部数据接口
>[https://dicserver/API/IDCIDs/province?action=getall](https://dicserver/API/IDCIDs/province)
>请求方式：GET
>返回所有province数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 34,
    key:["ProvinceID","ProvinceNameCn","ProvinceNameEn","Sort","ProvinceShortNameCn","ProvinceShortNameEn","XPos","YPos"],
	data:[["1001","北京","Beijing","10","NULL","NULL","450","175"],......]
}
```
##City
###获取全部数据接口
>[https://dicserver/API/IDCIDs/city?action=getall](https://dicserver/API/IDCIDs/city)
>请求方式：GET
>返回所有city数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 421,
    key:["CityID","ProvinceID","CityNameCn","CityNameEn","CityLevel","Sort","City1En","City1Cn","City2En","City2Cn","City3En","City3Cn],
	data:[["100","1003","上海","Shanghai","1","0","Shanghai","上海","Shanghai","上海","Shanghai","上海"],......]
}
```
##DealerGroup
###获取全部数据接口
>[https://dicserver/API/IDCIDs/dealergroup?action=getall](https://dicserver/API/IDCIDs/dealergroup)
>请求方式：GET
>返回所有dealergroup数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 38,
    key:["Id","DealerGroupCn","DealerGroupEn","Status"],
	data:[["1000","LSH","LSH","0"],......]
}
```
##FormatCode
###获取全部数据接口
>[https://dicserver/API/IDCIDs/formatcode?action=getall](https://dicserver/API/IDCIDs/formatcode)
>请求方式：GET
>返回所有formatcode数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 14,
    key:["FormatCodeID","FormatCode","FormatID","FormatLevel"],
	data:[["10150","AH 150","1","1"],......]
}
```
##Format
###获取全部数据接口
>[https://dicserver/API/IDCIDs/format?action=getall](https://dicserver/API/IDCIDs/formatcode)
>请求方式：GET
>返回所有formatcode数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 3,
    key:["FormatID","FormatNameCn","FormatNameEn","FormatShortName","Sort"],
	data:[["1","3S店(AH)","Autohaus(AH)","AH","10"],......]
}
```
##OChart
###获取全部数据接口
>[https://dicserver/API/IDCIDs/oChart?action=getall&page=1](https://dicserver/API/IDCIDs/oChart)
>请求方式：GET
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
| page     |          是 |  当前页      |
####返回结果说明
``` json
{
	totalCount: 60000,
    page:1,
    pageSize:50,
    key:["OChartID","CompanyID","DealerID","ParentID","ShowParentID","NodeCategory","NodeType","OChartStandardID","NameCn","NameEn","DescriptionCn","DescriptionEn","Sort","IsAssistant","IsManagement","IsCustom","BelongDepartment","PositionType","IsEqualToStandardPosition"],
	data:[["230000000001","23","0","0","NULL","2","1","1","总经理","总经理","","","1","0","1","0","3","1","1"],......]
}
``` 

###获取增量数据接口
>[https://dicserver/API/IDCIDs/oChart?action=getupdate&fromtime=123455](https://dicserver/API/IDCIDs/oChart)
>请求方式：GET
>该接口返回自fromtime开始所有有更新或者新增的oChart数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getupdate表示表示获取增量数据      |
| fromtime     |          是 |  起始时间时间戳      |
####返回结果说明
``` json
{
	totalCount: 60000,
    page:1,
    pageSize:50,
    key:["OChartID","CompanyID","DealerID","ParentID","ShowParentID","NodeCategory","NodeType","OChartStandardID","NameCn","NameEn","DescriptionCn","DescriptionEn","Sort","IsAssistant","IsManagement","IsCustom","BelongDepartment","PositionType","IsEqualToStandardPosition"],
	data:[["230000000001","23","0","0","NULL","2","1","1","总经理","总经理","","","1","0","1","0","3","1","1"],......]
}
``` 
##User
###获取全部数据接口
>[https://dicserver/API/IDCIDs/user?action=getall&page=1](https://dicserver/API/IDCIDs/user)
>分页方式获取全部USER数据
>请求方式：`GET`
>TopDepartment：`用户一级部门`
>SecondDepartment：`用户二级部门`
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
| page     |          是 |  当前页      |
####返回结果说明
``` json
{
	totalCount: 60000,
    page:1,
    pageSize:50,
    key:["UserID","CardType","CardNumber","DrivingLicense","FamilyNameCn","GivenNameCn","FamilyNameEn","GivenNameEn","Birthday","Gender","QualificationID","CertificationID","DepartmentID","PositionID","Email","PhoneCountryNo","PhoneAreaNo","PhoneNo","FaxCountryNo","FaxAreaNo","FaxNo","MobilePhoneCountryNo","MobilePhoneNo","DealerID","DealergroupID","TopDepartment","SecondDepartment","Status"],
	data:[["230000000001","23","0","0","NULL","2","1","1","总经理","总经理","","","1","0","1","0","3","1",.....],......]
}
``` 

###获取增量数据接口
>[https://dicserver/API/IDCIDs/user?action=getupdate&fromtime=123455](https://dicserver/API/IDCIDs/dealer)
>请求方式：GET
>该接口返回自fromtime开始所有有更新或者新增的dealer数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getupdate表示表示获取增量数据      |
| fromtime     |          是 |  起始时间时间戳      |
####返回结果说明
``` json
{
	totalCount: 300,
    key:["UserID","CardType","CardNumber","DrivingLicense","FamilyNameCn","GivenNameCn","FamilyNameEn","GivenNameEn","Birthday","Gender","QualificationID","CertificationID","DepartmentID","PositionID","Email","PhoneCountryNo","PhoneAreaNo","PhoneNo","FaxCountryNo","FaxAreaNo","FaxNo","MobilePhoneCountryNo","MobilePhoneNo","DealerID","DealergroupID","TopDepartment","SecondDepartment","Status"],
	data:[["230000000001","23","0","0","NULL","2","1","1","总经理","总经理","","","1","0","1","0","3","1",.....],......]
}
``` 

###根据UserID获取数据接口
>[https://dicserver/API/IDCIDs/user?action=getdatabyid&userid=39,40,41](https://dicserver/API/IDCIDs/dealer)
>请求方式：GET
>该接口返回自fromtime开始所有有更新或者新增的user数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getdatabyid表示表示获取增量数据      |
| userid     |          是 |  userid,多个ID用“，”分隔      |
####返回结果说明
``` json
{
	totalCount: 300,
    key:["UserID","CardType","CardNumber","DrivingLicense","FamilyNameCn","GivenNameCn","FamilyNameEn","GivenNameEn","Birthday","Gender","QualificationID","CertificationID","DepartmentID","PositionID","Email","PhoneCountryNo","PhoneAreaNo","PhoneNo","FaxCountryNo","FaxAreaNo","FaxNo","MobilePhoneCountryNo","MobilePhoneNo","DealerID","DealergroupID","TopDepartment","SecondDepartment","Status"],
	data:[["230000000001","23","0","0","NULL","2","1","1","总经理","总经理","","","1","0","1","0","3","1",.....],......]
}
``` 

##Certification
###获取全部数据接口
>[https://dicserver/API/IDCIDs/certification?action=getall&page=1](https://dicserver/API/IDCIDs/certification)
>请求方式：GET
>返回所有certification数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
| page       |          是 |  当前页      |
####返回结果说明
``` json
{
	totalCount: 20000,
	page:1,
	pageSize: 50,
    key:["ID","IdentityCard","Name","OChartStandardID","AcquiredDate","CreateDate"],
	data:[["1","44071119750409361X","CDT Certification (PC) 认证诊断技师 （乘用车）","80,150,165","2005-11-01 00:00:00.000","2015-09-21 16:15:31.317"],......]
}
```

##Qualification
###获取全部数据接口
>[https://dicserver/API/IDCIDs/qualification?action=getall](https://dicserver/API/IDCIDs/qualification)
>请求方式：GET
>返回所有qualification数据
####参数
| 参数        |    是否必须 | 说明                  |
| :--------  | ----------:| :------------------: |
| action     |          是 |  值为getall表示表示获取全部数据      |
####返回结果说明
``` json
{
	totalCount: 10,
    key:["QualificationID","QualificationCn","QualificationEn","Sort"],
	data:[["1","博士研究生","Doctor Degree","10"],......]
}
```
