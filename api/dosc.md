#CRM系統 Customer API Documentation

## Save Customer Data

保存或更新客戶信息。

### 端點

```
POST /api/Customer/SaveData
```

### 請求正文

Content-Type: application/json

| 欄位 | 類型 | 描述 | 必填 | 
|-------|------|-------------|----------|
| caseName | string | 案名 | 是 |
| name | string | 姓名 | 是 |
| phone | string | 電話 | 是 |
| email | string | Email | 否 |
| inDate | string (date-time) | 填寫時間 | 是 |
| source | string | 來源 FB / IG / EDM | 是 |
| adSource | string | 廣告來源 | 是 |
| remark | string | 備註 | 否 |
| contactTime | string | 聯絡時間 | 否 |
| q1 | string | 問題一 | 否 |
| q2 | string | 問題二 | 否 |
| q3 | string | 問題三 | 否 |
| q4 | string | 問題四 | 否 |
| q5 | string | 問題五 | 否 |
| q6 | string | 問題六 | 否 |
| q7 | string | 問題七 | 否 |
| q8 | string | 問題八 | 否 |

### 範例請求

```json
{
  "caseName": "Test",
  "name": "測試人",
  "phone": "0900293291",
  "email": "Test@test.com.w",
  "inDate": "2022-11-24T14:08:19.505Z",
  "source": "EDM",
  "adSource": "EDM",
  "remark": "TestAPI",
  "contactTime": "2022-11-24",
  "Q1":"問題一",
  "Q2":"問題二",
  "Q3":"問題三",
  "Q4":"問題四",
  "Q5":"問題五",
  "Q6":"問題六",
  "Q7":"問題七",
  "Q8":"問題八"
}
```

### 回應

#### 成功回應

**代碼**: 200

**內容**: 
```json
{
  "caseName": "string",
  "name": "string",
  "phone": "string",
  "email": "string",
  "inDate": "2024-08-29T04:33:33.156Z",
  "source": "string",
  "adSource": "string",
  "remark": "string",
  "contactTime": "string",
  "q1": "string",
  "q2": "string",
  "q3": "string",
  "q4": "string",
  "q5": "string",
  "q6": "string",
  "q7": "string",
  "q8": "string"
}
```

### 注意事項

- `phone` 欄位應符合以下模式：`^([0-9]{10})$`
- 所有日期時間欄位應採用 ISO 8601 格式
- `source` 欄位應為以下之一：FB、IG 或 EDM