## sign_up_API

------

### HTTP Method

```
[POST]
```

### Path

```
/notepad/add
/notepad/delete
/notepad/find_both
/notepad/update
/notepad/change_im
```

### PostBody

| 路径名称           | 字段       | 数据类型 | 说明                 |          样例           | 是否必须 |
| ------------------ | ---------- | -------- | -------------------- | :---------------------: | -------- |
| /notepad/add       | name       | string   | 记事本名称           |        "liziyu"         | 是       |
|                    | date       | string   | 创建记事本的日期     |       "20180715"        | 是       |
|                    | detail     | array    | 记事本中记录的内容   | ["aaa","sdsd","gggeee"] | 是       |
|                    | im         | number   | 记录的重要程度(1~5)  |            3            | 是       |
|                    |            |          |                      |                         |          |
| /notepad/delete    | name       | string   | 记事本名称           |        "liziyu"         | 是       |
|                    | date       | string   | 创建记事本的日期     |       "20180715"        | 是       |
|                    |            |          |                      |                         |          |
| /notepad/find_both | name       | string   | 记事本名称           |        "liziyu"         | 是       |
|                    | date       | string   | 创建记事本的日期     |       "20180715"        | 是       |
|                    |            |          |                      |                         |          |
| /notepad/update    | name       | string   | 记事本名称           |        "liziyu"         | 是       |
|                    | date       | string   | 创建记事本的日期     |       "20180715"        | 是       |
|                    | detail     | array    | 记事本中记录的内容   | ["aaa","sdsd","gggeee"] | 是       |
|                    | updatetime | number   | 更新记事本内容的时间 |        20180717         | 是       |
|                    |            |          |                      |                         |          |
| /notepad/change_im | name       | string   | 记事本名称           |        "liziyu"         | 是       |
|                    | date       | string   | 创建记事本的日期     |       "20180715"        | 是       |
|                    | im         | number   | 记录的重要程度(1~5)  |            3            | 是       |
|                    |            |          |                      |                         |          |

**样例：**

```
以/notepad/update为例：
        pad = {
            "name": "yangzeyu_zhang",
            "date": "20180712",
            "detail": ["from home",
                "country road"
            ],
            "updatetime": 20180722
        };

```

### Response

```
"Succeeded"
```

字段说明

| 字段       | 数据类型 | 说明                                         |
| ---------- | -------- | -------------------------------------------- |
| date       | string   | 创建记事本项目时的日期                       |
| name       | String   | 创建记事本项目时的名字                       |
| detail     | Array    | 创建记事本项目时的记录内容                   |
| im         | number   | 创建记事本项目时的事件重要程度               |
| updatetime | number   | （可能拥有的属性）更新记事本内容时的更改时间 |

