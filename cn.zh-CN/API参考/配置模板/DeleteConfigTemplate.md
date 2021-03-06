# DeleteConfigTemplate {#doc_api_WebPlus_DeleteConfigTemplate .reference}

调用DeleteConfigTemplate删除一个配置模板。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=WebPlus&api=DeleteConfigTemplate&type=ROA&version=2019-03-20)

## 请求头 {#requestHeadList .section}

该接口使用公共请求头，无特殊请求头。请参见公共请求参数文档。

## 请求语法 {#requestGrammer .section}

```
DELETE /pop/v1/wam/configTemplate HTTP/1.1
```

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|TemplateId|String|是|wct-5d3e9d2a2977ca5251e0\*\*\*\*|配置模板ID，将删除此配置模板

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|OK|响应代码，若成功请求为OK

 |
|Message|String|success|响应消息，若成功请求为success

 |
|RequestId|String|0E0A3207-12BD-4F5D-A3C2-E33BEEBB\*\*\*\*|请求ID

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http://webplus.cn-hangzhou.aliyuncs.com/pop/v1/wam/configTemplate?ServiceCode=webx&Id=wct-5d233291daae5125d353****&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteConfigTemplateResponse>
      <Message>success</Message>
      <RequestId>0E0A3207-12BD-4F5D-A3C2-E33BEEBB****</RequestId>
      <Code>OK</Code>
</DeleteConfigTemplateResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Message":"success",
	"RequestId":"688D65D8-6509-4F04-A0F0-6B04D774****",
	"Code":"OK"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|ResourceAuthFailed|The specified resource does not exist or it does not belong to this Alibaba Cloud account.|相关资源不存在或不属于此阿里云账号。|

访问[错误中心](https://error-center.aliyun.com/status/product/WebPlus)查看更多错误码。

