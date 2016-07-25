#Group.Create

星球创建接口-用于创建星球

##接口调用请求说明

接口URL：http://apihost/?service=Group.Create

请求方式：POST

参数说明：

|参数|类型|是否必须|范围|说明|
|:--|:--|:--|:--|:--|
|user_id|整形|必须|-|用户id|
|name|字符串|必须|最小：1 最大：80|星球名称|
|g_image|字符串  | 必须 ||  url链接|
|g_introduction|字符串|可选||星球简介|

##返回说明
|参数|类型|说明|
|:--|:--|:--|
|code|整型|操作码，1表示创建成功，0表示创建失败|
|info                 |对象   |星球信息对象|
|info.group_base_id   |整型   |星球ID|
|info.user_base_id    |字符串 |创建者ID|
|info.name            |字符串 |星球名称|
|info.g_introduction   |字符串  | 星球简介|
|info.g_image        |字符串|url链接|
|msg                  |字符串 |提示信息|
|info.authorization   |字符串 |权限，01表示创建者，02表示管理员，03表示会员|

##示例

创建名为“鬼扯1”的星球

http://apihost/?service=Group.Create

    JSON:
    {
        "ret": 200,
        "data": {
            "code": 1,
            "msg": "",
            "info": {
                "group_base_id": "48",
                "user_base_id": "15",
                "authorization": "01",
                "name": "鬼扯1",
                "g_introduction": "照片裁剪",
                "URL": "../upload/group/2016/05/28/apic14052.jpg"
            }
        },
        "msg": ""
    }
