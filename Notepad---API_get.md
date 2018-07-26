## sign_up_API

------

### HTTP Method

```
[GET]
```

### Path

```
/notepad
/notepad/find_name?name=name
/notepad/find_im?im=im
/notepad/im_paixu
```

参数说明

| 参数 | 说明                                                       |
| ---- | ---------------------------------------------------------- |
| name | 校验参数，计算方法：md5(JSON.stringify(body) + md5('ATX')) |
| im   | 校验参数，计算方法：md5(JSON.stringify(body) + md5('ATX')) |

**样例**

```
/notepad
/notepad/find_name?name="ziyu_li"
/notepad/find_im?im=3
/notepad/im_paixu
```

### Response

```
**/notepad**
{
    "Items": [
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        }
        ...
    "Count": {type:'number'},
    "ScannedCount": {type:'number'}
}


**/notepad/find_name?name=name**
{
    "Items": [
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
    ],
    "Count": 1,
    "ScannedCount": 1
}

**/notepad/find_im?im=3**
{
    "Items": [
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        }
        ...
    ],
    "Count": {type:'number'},
    "ScannedCount": {type:'number'}
}

**/notepad/im_paixu**
{
    "Items": [
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        },
        {
            "date": {type:'string'},
            "name": {type:'string'},
            "detail": {type:'array'},
            "im": {type:'number'},
            ("updatetime": {type:'number'})
        }
        ...
    ],
    "Count": {type:'number'},
    "ScannedCount": {type:'number'}
}

```

**样例**

```
**/notepad**
{
    "Items": [
        {
            "date": "20180722",
            "name": "really",
            "detail": [
                "!!!!!!",
                "hahaha"
            ],
            "im": 3
        },
        {
            "date": "20180712",
            "name": "nang_hong",
            "detail": [
                "good night",
                "I will go to sleep"
            ],
            "im": 2
        },
        {
            "date": "20180719",
            "name": "lixiaomei",
            "detail": [
                "TTTTT"
            ],
            "im": 4
        },
        {
            "date": "20180712",
            "name": "ziyu_li",
            "detail": [
                "body in life",
                "come on baby",
                "!!!"
            ],
            "im": 5
        },
        {
            "date": "20180712",
            "name": "yang_hong",
            "detail": [
                "The I go swimming with my friend. ",
                " What a happy day!"
            ],
            "im": 3
        },
        {
            "date": "20180712",
            "name": "yangzeyu_zhang",
            "detail": [
                "what a nice day!!!",
                "I am so happy hahahaha",
                "from home",
                "country road"
            ],
            "im": 1,
            "updatetime": 20180722
        }
    ],
    "Count": 6,
    "ScannedCount": 6
}


**/notepad/find_name?name=ziyu_li**
{
    "Items": [
        {
            "name": "ziyu_li",
            "date": "20180712",
            "detail": [
                "body in life",
                "come on baby",
                "!!!"
            ],
            "im": 5
        }
    ],
    "Count": 1,
    "ScannedCount": 1
}

**/notepad/find_im?im=3**
{
    "Items": [
        {
            "name": "really",
            "date": "20180722",
            "detail": [
                "!!!!!!",
                "hahaha"
            ],
            "im": 3
        },
        {
            "date": "20180712",
            "name": "yang_hong",
            "detail": [
                "The I go swimming with my friend. ",
                " What a happy day!"
            ],
            "im": 3
        }
    ],
    "Count": 2,
    "ScannedCount": 2
}

**/notepad/im_paixu**
{
    "Items": [
        {
            "date": "20180712",
            "name": "ziyu_li",
            "detail": [
                "body in life",
                "come on baby",
                "!!!"
            ],
            "im": 5
        },
        {
            "date": "20180719",
            "name": "lixiaomei",
            "detail": [
                "TTTTT"
            ],
            "im": 4
        },
        {
            "date": "20180722",
            "name": "really",
            "detail": [
                "!!!!!!",
                "hahaha"
            ],
            "im": 3
        },
        {
            "date": "20180712",
            "name": "yang_hong",
            "detail": [
                "The I go swimming with my friend. ",
                " What a happy day!"
            ],
            "im": 3
        },
        {
            "date": "20180712",
            "name": "nang_hong",
            "detail": [
                "good night",
                "I will go to sleep"
            ],
            "im": 2
        },
        {
            "date": "20180712",
            "name": "yangzeyu_zhang",
            "detail": [
                "what a nice day!!!",
                "I am so happy hahahaha",
                "from home",
                "country road"
            ],
            "im": 1
        }
    ],
    "Count": 6,
    "ScannedCount": 6
}
```

字段说明

| 字段       | 数据类型 | 说明                                         |
| ---------- | -------- | -------------------------------------------- |
| date       | string   | 创建记事本项目时的日期                       |
| name       | String   | 创建记事本项目时的名字                       |
| detail     | Array    | 创建记事本项目时的记录内容                   |
| im         | number   | 创建记事本项目时的事件重要程度               |
| updatetime | number   | （可能拥有的属性）更新记事本内容时的更改时间 |

