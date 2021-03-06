# AddAccessControlListEntry {#doc_api_Slb_AddAccessControlListEntry .reference}

调用AddAccessControlListEntry在访问控制策略组中添加IP条目。

每个策略组可包含多个IP地址条目或IP地址段条目，访问控制策略组的条目限制如下：

-   单账号每次可添加的IP地址条目个数：50
-   每个访问控制策略组可包含的条目个数：300

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Slb&api=AddAccessControlListEntry&type=RPC&version=2014-05-15)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddAccessControlListEntry|要执行的操作，取值：**AddAccessControlListEntry**。

 |
|AclId|String|是|acl-bp1l0kk4gxce43kze\*\*\*\*\*|访问控制策略组ID。

 |
|RegionId|String|是|cn-hangzhou|访问控制策略组的地域ID。

 |
|AclEntrys|String|否|\[\{"entry":"10.0.0.0/24","comment":"privaterule1"\},\{"entry":"192.168.0.0/16","comment":"privaterule2"\}\]|访问控制策略组中要添加的IP条目，可以指定IP地址或IP地址段（CIDR block），多个IP地址/地址段之间用逗号隔开。

 **说明：** 每次最多可添加50个条目。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|988CB45E-1643-48C0-87B4-928DDF77EA4|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=AddAccessControlListEntry
&AclId=acl-bp1l0kk4gxce43kze*****
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<AddAccessControlListEntryResponse>
    <RequestId>988CB45E-1643-48C0-87B4-928DDF77EA49</RequestId>
</AddAccessControlListEntryResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"988CB45E-1643-48C0-87B4-928DDF77EA49"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/Slb)查看更多错误码。

