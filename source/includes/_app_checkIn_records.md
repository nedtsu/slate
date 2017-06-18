# 打卡紀錄 APP

## 查詢打卡記錄

> The API returns JSON structured like this:

```json
{
  "Meta": {
    "HttpStatusCode": 200
  },
  "Data": [
    {
      "EmployeeName": "姓名",
      "AttendanceDate": "0001-01-01T00:00:00+00:00",
      "IsHoliday": true,
      "WorkList": [
        {
          "AttendanceDate": "0001-01-01T00:00:00+00:00",
          "InAttendanceHistoryId": null,
          "InAttendanceOn": null,
          "InPunchesLocationId": null,
          "InLatitude": 0,
          "InLongitude": 0,
          "Language_InPunchesLocation": null,
          "InOriginType": null,
          "OutAttendanceHistoryId": null,
          "OutAttendanceOn": null,
          "OutPunchesLocationId": null,
          "OutLatitude": 0,
          "OutLongitude": 0,
          "Language_OutPunchesLocation": null,
          "OutOriginType": null,
          "Index": 0,
          "DeptCName": null,
          "EmployeeNumber": null,
          "EmployeeName": null,
          "DeptCode": null
        }
      ],
      "RestList": [
        {
          "AttendanceDate": "0001-01-01T00:00:00+00:00",
          "InAttendanceHistoryId": null,
          "InAttendanceOn": null,
          "InPunchesLocationId": null,
          "InLatitude": 0,
          "InLongitude": 0,
          "Language_InPunchesLocation": null,
          "InOriginType": null,
          "OutAttendanceHistoryId": null,
          "OutAttendanceOn": null,
          "OutPunchesLocationId": null,
          "OutLatitude": 0,
          "OutLongitude": 0,
          "Language_OutPunchesLocation": null,
          "OutOriginType": null,
          "Index": 0,
          "DeptCName": null,
          "EmployeeNumber": null,
          "EmployeeName": null,
          "DeptCode": null
        }
      ],
      "OutOfOfficeList": [
        {
          "AttendanceHistoryId": "00000000-0000-0000-0000-000000000000",
          "AttendanceDate": "0001-01-01T00:00:00+00:00",
          "AttendanceOn": "0001-01-01T00:00:00+00:00",
          "Latitude": 0,
          "Longitude": 0,
          "Language_PunchesLocation": null,
          "DeptCName": null,
          "EmployeeNumber": null,
          "EmployeeName": null,
          "DeptCode": null
        }
      ],
      "ExceptionList": [
        {
          "ExceptionId": "NoCheckIn",
          "Reason": "上班未打卡-無上班打卡紀錄"
        }
      ],
      "BiilingStatus": 0
    }
  ]
}
```

取得 上下班/休息/外出打卡, 異常, 休假狀態 資料

<aside class="notice">
PT 1.6 更新<br>
增加 BiilingStatus: 若後端判斷為"已結算不允許查詢已結算打卡紀錄"時會將值填入 否則為0, APP需優先判斷該值, 大於0 顯示 "資料已結算"
</aside>

### HTTP Request

`GET api/checkinRecords`

### Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
attendanceDateStart | Date | 查詢開始日期
attendanceDateEnd | Date | 查詢結束日期
employeeId | Guid? | 查詢人員ID

### Response
Key | Type | Description
--- | ---- | -----------

### Changelog

Date | Description
---- | -----------

