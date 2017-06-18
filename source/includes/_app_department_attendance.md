# 人員出勤 APP

## 取得單位出勤狀況

> The API returns JSON structured like this:

```json
{
  "Meta": {
    "HttpStatusCode": 200
  },
  "Data": {
    "DeptCName": "直屬員工",
    "DeptCode": null,
    "AllNumber": 1,
    "AttendedNumber": 0,
    "AbsenceNumber": 1,
    "LeaveNumber": 0,
    "OvertimeNumber": 0,
    "EmployeeList": [
      {
        "EmployeeId": "00000000-0000-0000-0000-000000000000",
        "Name": "姓名",
        "PictureUrl": "",
        "IsExpected": true,
        "IsAttended": false,
        "IsAbsence": true,
        "IsLeave": false,
        "IsOvertime": false,
        "ShowColor": false,
        "ExceptionList": [
          {
            "ExceptionId": null,
            "Reason": "-"
          }
        ],
        "LeaveSheets": [
          {
            "LeaveRequestFormId": "00000000-0000-0000-0000-000000000000",
            "LeaveStartDatetime": "0001-01-01T00:00:00+00:00",
            "LeaveEndDatetime": "0001-01-01T00:00:00+00:00",
            "TotalHours": 0
          }
        ],
        "OvertimeSheets": [
          {
            "OvertimeRequestFormId": "00000000-0000-0000-0000-000000000000",
            "OvertimeStartDatetime": "0001-01-01T00:00:00+00:00",
            "OvertimeEndDatetime": "0001-01-01T00:00:00+00:00",
            "TotalHours": 0
          }
        ]
      }
    ]
  }
}
```

取得單位出勤狀況, 異常, 請假單, 加班單

<aside class="notice">
PT 1.6 更新<br>
後端判斷"已結算不允許查詢已結算打卡紀錄" 且 該天人員已出勤結算, ExceptionList 為 []
</aside>

### HTTP Request

`[GET] api/checkinRecords/Department`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
Date | Date | 查詢日期
departmentId | Guid? | 查詢單位ID, 空值為查詢 直屬人員

### Changelog

Date | Description
---- | -----------
2017-06-18 | init
