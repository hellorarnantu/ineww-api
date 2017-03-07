# ineww-api
INEWW 后台接口API文档



[toc]


## 1 新闻模块

### 1.1  用获取全部新闻

    get {domain}/ineww/news

URL参数

|名称|类型|是否必须|描述|
|--|--|--|--|
|page|int|否|页数(1,~)|
|page_per|int|否|每页条数(5,~)|

返回结果
```
{
    "code": "200001", 
    "data": {
        "count": 20, 
        "page_per": 10, 
        "page": 1, 
        "result": [
            {
                "news_id": 236, 
                "keywords": "家电 涨价",  #关键字
                "source": "搜狐网",  #来源
                "category": 0, 　#类别（0新闻）
                "title": "家电行业缩短产业链 是应对涨价还是行业地震", 
                "created_time": 1488889044, ＃时间
                "image": "http://img.mp.itc.cn/upload/20170307/f1ca19bd4d5a4438829a8cb8bcab3392_th.png", 
                "author": "康斯坦丁", ＃作者
                "brief": null　#简介
            }
        ]
    }
}
```

### 1.2 获取新闻详情

    get {domain}/ineww/news/:news_id
    

返回结果
``` 
{
    "code": "200001", 
    "data": {
        "category": 0, 
        "content": " # 内容
    <span>（科技新发现 康斯坦丁/文）</span>
</p>", 
        "title": "家电行业缩短产业链 是应对涨价还是行业地震", 
        "image": "http://img.mp.itc.cn/upload/20170307/f1ca19bd4d5a4438829a8cb8bcab3392_th.png", 
        "author": "康斯坦丁", 
        "brief": null, 
        "news_id": 236, 
        "source": "搜狐网", 
        "created_time": 1488889044, 
        "keywords": "家电 涨价", 
        "original": "http://it.sohu.com/20170307/n482634804.shtml"　＃l来源
    }
}
```
