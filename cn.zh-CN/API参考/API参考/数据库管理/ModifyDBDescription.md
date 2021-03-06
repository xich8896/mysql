# ModifyDBDescription {#reference_xbj_pfg_12b .reference}

## 描述 {#section_l21_v32_12b .section}

该接口用于修改数据库的备注名，便于记录该数据库，比如为数据库修改备注名为“阿里云测试环境实例数据库A”。

**说明：** 此接口不支持PostgreSQL和PPAS。

## 请求参数 {#section_qzx_w32_12b .section}

|名称|类型|是否必须|描述|
|--|--|----|--|
|Action|String|是|系统规定参数，取值为ModifyDBDescription。|
|DBInstanceId|String|是|实例名。|
|DBName|String|是|数据库名。|
|DBDescription|String|是|修改DB备注。|

## 返回参数 {#section_rpk_z32_12b .section}

|名称|类型|描述|
|--|--|--|
|<公共返回参数\>| |详见[公共参数](cn.zh-CN/API参考/使用API/公共参数.md#)。|

## 请求示例 {#section_l4g_pj2_12b .section}

```
https://rds.aliyuncs.com/?Action=ModifyDBDescription
&DBInstanceId=rdsaiiabnaiiabn
&DBInstanceDescription=testwangyichengDBdescribe
&<公共请求参数>
```

## 返回示例 {#section_xtg_rj2_12b .section}

**XML格式**

```
< ModifyDBDescriptionResponse>
         <RequestId>17F57FEE-EA4F-4337-8D2E-9C23CAA63D74</RequestId>
</ ModifyDBDescriptionResponse>
```

**JSON格式**

```
{
    "RequestId": " 17F57FEE-EA4F-4337-8D2E-9C23CAA63D74"
  }
```

