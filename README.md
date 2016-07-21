十三、企业通知
一、企业通知详情
1)测试：messageNotice/messageNoticeList
2)输入参数：
名称	类型	输入/输出	描述
customerId	String	In	公司ID
createrId	String	in	创建人

3)输出参数：
名称	类型	输入/输出	描述
headLine	String	Out	标题
userAmount			通知总人数
noReadAmount			没有阅读人数
status			状态值（0：发布；1：草稿；2：作废）
templateType			模板类型(1000：系统默认；1001：会议模板；1002：活动模板；1003：培训模板)


4)返回结果：
取返回的json字符串中的data对象的值	
返回结果	描述
测试	http://localhost:8080/hdsec/messageNotice/messageNoticeList?customerId=AEB1F6F3-8E86-4D9B-96E1-19D1B273BA53

data	{
    "result": true,
    "data": [
        {
            "pageNum": 1,
            "pageSize": 20,
            "totalCount": 0,
            "orderField": null,
            "orderDirection": "asc",
            "keywords": null,
            "status": "0",
            "type": "1",
            "startDate": null,
            "endDate": null,
            "id": "6fffc4d49d8e40b68e57bc6bcad8bd88",
            "customerId": "838B148E-C7E1-4123-9283-B5FF92A9E6B9",
            "content": "wwww",
            "createrId": "111",
            "createTime": "2016-07-21 10:35:39.0",
            "userIdListStr": "",
            "hasRead": "",
            "startTime": "1900-01-01 00:00:00.0",
            "endTime": "1900-01-01 00:00:00.0",
            "noticeTime": "1900-01-01 00:00:00.0",
            "headLine": "fff",
            "compereId": "",
            "compereName": "",
            "address": "",
            "templateType": "1000",
            "signAddress": "",
            "userId": null,
            "lat": "",
            "lng": "",
            "createStartTime": null,
            "createEndTime": null,
            "userAmount": "3",
            "noReadAmount": "3",
            "endIndex": 20,
            "startIndex": 0
        },
        {
            "pageNum": 1,
            "pageSize": 20,
            "totalCount": 0,
            "orderField": null,
            "orderDirection": "asc",
            "keywords": null,
            "status": "0",
            "type": "1",
            "startDate": null,
            "endDate": null,
            "id": "919c6707ca4e431faac58c505931cb22",
            "customerId": "",
            "content": "",
            "createrId": "",
            "createTime": "2016-07-21 10:26:21.767",
            "userIdListStr": "",
            "hasRead": "",
            "startTime": "1900-01-01 00:00:00.0",
            "endTime": "1900-01-01 00:00:00.0",
            "noticeTime": "1900-01-01 00:00:00.0",
            "headLine": "",
            "compereId": "",
            "compereName": "",
            "address": "",
            "templateType": "",
            "signAddress": "",
            "userId": null,
            "lat": null,
            "lng": null,
            "createStartTime": null,
            "createEndTime": null,
            "userAmount": "1",
            "noReadAmount": "1",
            "endIndex": 20,
            "startIndex": 0
        }
    ],
    "count": 10,
    "statusCode": "200",
    "status": "100",
    "message": "操作成功",
    "navTabId": "",
    "rel": "",
    "callbackType": "",
    "forwardUrl": "",
    "msg": "上传成功",
    "err": ""
}
	


二、企业通知反馈
1)测试：messageNotice/feedBackListApp
2)输入参数：
名称	类型	输入/输出	描述
messageId	String	In	消息ID

3)输出参数：
名称	类型	输入/输出	描述
amount	int	Out	通知人总数
messageUsers			未看通知的人员数据集合

4)返回结果：
取返回的json字符串中的data对象的值	
返回结果	描述
测试	http://localhost:8080/hdsec/messageNotice/feedBackListApp?messageId=758b1f96936f448c97f4b2fd7ba8f39a

data	{
    "result": true,
    "data": {
        "amount": 3,
        "messageUsers": [
            {
                "id": "B95D742E035448D0A9FD5A953C29A210",
                "messageId": "758b1f96936f448c97f4b2fd7ba8f39a",
                "customerId": "838B148E-C7E1-4123-9283-B5FF92A9E6B9",
                "userId": "a168",
                "hasRead": "0",
                "createTime": "2016-07-21 11:22:34.18",
                "userName": "小管理员",
                "userPhone": "",
                "secPhone": null
            },
            {
                "id": "C6FB9CEA9C4F4827A2276B57E2DD8493",
                "messageId": "758b1f96936f448c97f4b2fd7ba8f39a",
                "customerId": "838B148E-C7E1-4123-9283-B5FF92A9E6B9",
                "userId": "666",
                "hasRead": "0",
                "createTime": "2016-07-21 11:22:34.18",
                "userName": "小六",
                "userPhone": "",
                "secPhone": null
            },
            {
                "id": "E4E3F78136654473908211A9C165A880",
                "messageId": "758b1f96936f448c97f4b2fd7ba8f39a",
                "customerId": "838B148E-C7E1-4123-9283-B5FF92A9E6B9",
                "userId": "643",
                "hasRead": "0",
                "createTime": "2016-07-21 11:22:34.18",
                "userName": "打算",
                "userPhone": "",
                "secPhone": null
            }
        ]
    },
    "count": 1,
    "statusCode": "200",
    "status": "100",
    "message": "操作成功",
    "navTabId": "",
    "rel": "",
    "callbackType": "",
    "forwardUrl": "",
    "msg": "上传成功",
    "err": ""
}
	


三、发布通知
1)测试：messageNotice/submitMessage
2)输入参数：
名称	类型	输入/输出	描述
messageStr	json	In	{
    "id": "消息ID",
    "headLine": "标题",
    "content": "内容",
    "startTime": "活动开始时间",
    "endTime": "活动结束时间",
    "noticeTime": "会议和培训时间2016-07-21 14:29:20",
    "compereId": "主持人ID6323",
    "compereName": "主持人姓名 京忆秋",
    "address": "地址 成都339停车场",
    "templateType": "1000：系统默认；1001：会议模板；1002：活动模板；1003：培训模板",
    "signAddress": "签到地址42路公交车站公共厕所",
    "customerId": "838B148E-C7E1-4123-9283-B5FF92A9E6B9",
    "createrId": "111",
    "lat": "23.132148",
userStr
    "lng": "113.33097",
    "status": "状态0：发布；1：草稿；2：作废"
}
userStr	json		[
    {
        "userId": "555",
        "userName": "王五",
        "userPhone": "erp手机号码",
        "secPhone": "小蜜手机号码"
    },
    {
        "userId": "2888",
        "userName": " 小八",
        "userPhone": "暂无联系电话",
        "secPhone": ""
    }
]

3)返回结果：
取返回的json字符串中的data对象的值	
返回结果	描述
测试	http://localhost:8080/hdsec/messageNotice/submitMessage?messageStr={}&userStr=[]

data	{
    "result": true,
    "data": null,
    "count": 1,
    "statusCode": "200",
    "status": "100",
    "message": "0",
    "navTabId": "",
    "rel": "",
    "callbackType": "",
    "forwardUrl": "",
    "msg": "上传成功",
    "err": ""
}
	

