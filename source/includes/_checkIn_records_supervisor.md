# 人員出勤

## 取得上下班打卡記錄

> The Request returns JSON structured like this:

```json
{
    "Meta": {
        "PageNumber": 1,
        "PageSize": 10,
        "PageCount": 1,
        "HttpStatusCode": 200,
        "BillingDateRanges": [
            {
                "Start": "2017-02-02T00:00:00+00:00",
                "End": "2017-03-01T00:00:00+00:00"
            }
        ]
    },
    "Data": [
        {
            "AttendanceDate": "2017-03-24T00:00:00+00:00",
            "InAttendanceHistoryId": "81b4f670-d25e-474c-8e66-51768ca1eb8a",
            "InAttendanceOn": "2017-03-24T01:00:00+00:00",
            "InPunchesLocationId": "6e579ef4-336f-46be-8f05-de2a783814f0",
            "InLatitude": 0,
            "InLongitude": 0,
            "Language_InPunchesLocation": "1        1",
            "InOriginType": "打卡補登",
            "OutAttendanceHistoryId": "088c662c-973f-4a72-a379-ee48fbe5cedc",
            "OutAttendanceOn": "2017-03-24T01:00:00+00:00",
            "OutPunchesLocationId": "6e579ef4-336f-46be-8f05-de2a783814f0",
            "OutLatitude": 0,
            "OutLongitude": 0,
            "Language_OutPunchesLocation": "1        1",
            "OutOriginType": "打卡補登",
            "Index": 0,
            "DeptCName": "產品研發處",
            "EmployeeNumber": "E0066",
            "EmployeeName": "韓建中",
            "DeptCode": "R3000"
        }
    ]
}
```

<aside class="notice">
PT 1.6 更新<br>
Meta 增加 BillingDateRanges, 判斷 “已結算是否允許查詢已結算打卡紀錄” 排除已結算資料    
</aside>

### HTTP Request

`GET api/checkinRecords/supervisor/onOffWork`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
attendanceDateStart | Date | 查詢開始日期
attendanceDateEnd | Date | 查詢結束日期
departmentId | Guid? | 查詢單位ID
employeeId | Guid? | 查詢人員ID

### Response 請參考 Json
Key | Type | Description
--- | ---- | -----------

### Changelog

Date | Description
---- | -----------

## 取得休息打卡記錄

> The Request returns JSON structured like this:

```json
{
    "Meta": {
        "PageNumber": 1,
        "PageSize": 10,
        "PageCount": 1,
        "HttpStatusCode": 200,
        "BillingDateRanges": [
            {
                "Start": "2017-02-02T00:00:00+00:00",
                "End": "2017-03-01T00:00:00+00:00"
            }
        ]
    },
    "Data": [
        {
            "AttendanceDate": "2017-03-24T00:00:00+00:00",
            "InAttendanceHistoryId": "81b4f670-d25e-474c-8e66-51768ca1eb8a",
            "InAttendanceOn": "2017-03-24T01:00:00+00:00",
            "InPunchesLocationId": "6e579ef4-336f-46be-8f05-de2a783814f0",
            "InLatitude": 0,
            "InLongitude": 0,
            "Language_InPunchesLocation": "1        1",
            "InOriginType": "打卡補登",
            "OutAttendanceHistoryId": "088c662c-973f-4a72-a379-ee48fbe5cedc",
            "OutAttendanceOn": "2017-03-24T01:00:00+00:00",
            "OutPunchesLocationId": "6e579ef4-336f-46be-8f05-de2a783814f0",
            "OutLatitude": 0,
            "OutLongitude": 0,
            "Language_OutPunchesLocation": "1        1",
            "OutOriginType": "打卡補登",
            "Index": 0,
            "DeptCName": "產品研發處",
            "EmployeeNumber": "E0066",
            "EmployeeName": "韓建中",
            "DeptCode": "R3000"
        }
    ]
}

```

<aside class="notice">
PT 1.6 更新<br>
Meta 增加 BillingDateRanges, 判斷 “已結算是否允許查詢已結算打卡紀錄” 排除已結算資料    
</aside>

### HTTP Request

`GET api/checkinRecords/supervisor/rest`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
attendanceDateStart | Date | 查詢開始日期
attendanceDateEnd | Date | 查詢結束日期
departmentId | Guid? | 查詢單位ID
employeeId | Guid? | 查詢人員ID

### Response
Key | Type | Description
--- | ---- | -----------

### Changelog

Date | Description
---- | -----------

## 取得外出打卡記錄

> The Request returns JSON structured like this:

```json
{
    "Meta": {
        "PageNumber": 1,
        "PageSize": 10,
        "PageCount": 68,
        "HttpStatusCode": 200,
        "BillingDateRanges": [
            {
                "Start": "2016-03-18T00:00:00+00:00",
                "End": "2016-03-31T00:00:00+00:00"
            },
            {
                "Start": "2016-08-30T00:00:00+00:00",
                "End": "2016-08-30T00:00:00+00:00"
            }
        ]
    },
    "Data": [
        {
            "AttendanceHistoryId": "3b302121-5fc1-45e6-ae9e-8804767252cf",
            "AttendanceDate": "2016-11-29T00:00:00+00:00",
            "AttendanceOn": "2016-11-29T05:38:16+00:00",
            "Latitude": 24.810075,
            "Longitude": 121.0348983,
            "Language_PunchesLocation": "華雲",
            "DeptCName": "產品研發部",
            "EmployeeNumber": "E0063",
            "EmployeeName": "李華雲",
            "DeptCode": "R3100"
        }
    ]
}

```

<aside class="notice">
PT 1.6 更新<br>
Meta 增加 BillingDateRanges, 判斷 “已結算是否允許查詢已結算打卡紀錄” 排除已結算資料    
</aside>

### HTTP Request

`[GET] api/checkinRecords/supervisor/outWork`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
attendanceDateStart | Date | 查詢開始日期
attendanceDateEnd | Date | 查詢結束日期
departmentId | Guid? | 查詢單位ID
employeeId | Guid? | 查詢人員ID

### Response
Key | Type | Description
--- | ---- | -----------

### Changelog

Date | Description
---- | -----------

## 取得異常記錄

> The Request returns JSON structured like this:

```json
{
    "Meta": {
        "PageNumber": 1,
        "PageSize": 10,
        "PageCount": 68,
        "HttpStatusCode": 200,
        "BillingDateRanges": [
            {
                "Start": "2016-03-18T00:00:00+00:00",
                "End": "2016-03-31T00:00:00+00:00"
            },
            {
                "Start": "2016-08-30T00:00:00+00:00",
                "End": "2016-08-30T00:00:00+00:00"
            }
        ]
    },
    "Data": [
        {
            "AttendanceHistoryId": "3b302121-5fc1-45e6-ae9e-8804767252cf",
            "AttendanceDate": "2016-11-29T00:00:00+00:00",
            "AttendanceOn": "2016-11-29T05:38:16+00:00",
            "Latitude": 24.810075,
            "Longitude": 121.0348983,
            "Language_PunchesLocation": "華雲",
            "DeptCName": "產品研發部",
            "EmployeeNumber": "E0063",
            "EmployeeName": "李華雲",
            "DeptCode": "R3100"
        }
    ]
}

```

<aside class="notice">
PT 1.6 更新<br>
Meta 增加 BillingDateRanges, 判斷 “已結算是否允許查詢已結算打卡紀錄” 排除已結算資料    
</aside>

### HTTP Request

`[GET] api/checkinRecords/supervisor/excpetion`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
year | int | 查詢年度 
month | int | 查詢月份
day | int | 查詢日
departmentId | Guid? | 查詢單位ID
employeeId | Guid? | 查詢人員ID

### Response
Key | Type | Description
--- | ---- | -----------

### Changelog

Date | Description
---- | -----------