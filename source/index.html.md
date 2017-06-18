---
title: Attendance API Reference

language_tabs:
  - javascript
  - csharp

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - checkIn_settings
  - checkIn_records
  - checkIn_records_supervisor
  - app_checkIn_records
  - app_department_attendance
  - errors
  - markdown_syntax

search: true
---

# Introduction

Welcome to the Attendance API! 

目前文件包含 內容：

1. 打卡設定
2. 打卡記錄
3. 人員出勤
4. 打卡記錄 (APP)
5. 人員出勤 (APP)

其他部分為 slate 預設與測試請忽略

Authentication 請參考目前作法

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>