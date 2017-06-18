# 打卡設定

## 取得打卡設定

> The Request returns JSON structured like this:

```json
{
  "Meta": {
  "HttpStatusCode": 200
  },
  "Data": {
  "IsBillingRecordQueryable": false
  }
}
```

取得打卡其他設定

### HTTP Request

`[GET] api/CheckInSettings`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

### Response

Key | Type | Description
--- | ---- | -----------
IsBillingRecordQueryable | boolean | 已結算是否允許查詢已結算打卡紀錄

## 更新打卡設定

> The request body JSON structured like this:

```json
{
  "IsBillingRecordQueryable": false
}
```

更新打卡設定

### HTTP Request

`[PUT] api/CheckInSettings`

### Body

Key | Type | Description
--- | ---- | -----------
IsBillingRecordQueryable | boolean | 已結算是否允許查詢已結算打卡紀錄

### Changelog

Date | Description
---- | -----------
