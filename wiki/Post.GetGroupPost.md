#Post.GetGroupPost

星球页面帖子显示

##接口调用请求说明

接口URL：http://apilost/?service=Post.GetGroupPost

请求方式：GET

参数说明：

|参数|类型|是否必须|默认值|说明|
|:--|:--|:--|:--:|:--|
|group_id|int|必须|-|星球ID|
|pn|int|不必须|1|第几页|
##返回说明
|参数|类型|说明|
|:--|:--|:--|
|posts.postID	|	int|	帖子ID|
|posts.title	|string|	标题|
|posts.text	|string|	内容|
|posts.createTime|	date|	发帖时间|
|posts.nickname|string	|发帖人|
|posts.sticky|int	|是否置顶|
|posts.groupID|int	|星球ID|
|posts.groupName	|string|	星球名称|
|pageCount	|int	|总页数|
|currentPage	|int	|当前页|

##示例

显示星球ID为1的第1页帖子

http://apilost/?service=Post.GetGroupPost&group_id=1&pn=1

    JSON:
{
    "ret": 200,
    "data": {
        "groupID": "1",
        "groupName": "鬼扯天地",
        "posts": [
            {
                "digest": "0",
                "postID": "1",
                "title": "title1",
                "text": "text1454",
                "createTime": "2016",
                "id": "1",
                "nickname": "caoyu",
                "sticky": "0"
            },
            {
                "digest": "0",
                "postID": "2",
                "title": "title2",
                "text": "text1454",
                "createTime": "2019",
                "id": "1",
                "nickname": "caoyu",
                "sticky": "0"
            }
        ],
        "pageCount": 1,
        "currentPage": 1
    },
    "msg": ""
}
