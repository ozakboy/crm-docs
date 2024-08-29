# Customer API Documentation

## Save Customer Data

Save or update customer information.

### Endpoint

```
POST /api/Customer/SaveData
```

### Request Body

Content-Type: application/json

| Field | Type | Description | Required | 
|-------|------|-------------|----------|
| caseName | string | 案名 | Yes |
| name | string | 姓名 | Yes |
| phone | string | 电话 | Yes |
| email | string | Email | No |
| inDate | string (date-time) | 填写时间 | Yes |
| source | string | 来源 FB / IG / EDM | Yes |
| adSource | string | 广告来源 | Yes |
| remark | string | 备注 | No |
| contactTime | string | 联络时间 | No |
| q1 | string | 问题一 | No |
| q2 | string | 问题二 | No |
| q3 | string | 问题三 | No |
| q4 | string | 问题四 | No |
| q5 | string | 问题五 | No |
| q6 | string | 问题六 | No |
| q7 | string | 问题七 | No |
| q8 | string | 问题八 | No |

### Sample Request

```json
{
  "caseName": "Test",
  "name": "测试人",
  "phone": "0900293291",
  "email": "Test@test.com.w",
  "inDate": "2022-11-24T14:08:19.505Z",
  "source": "EDM",
  "adSource": "EDM",
  "remark": "TestAPI",
  "contactTime": "2022-11-24",
  "Q1":"问题一",
  "Q2":"问题二",
  "Q3":"问题三",
  "Q4":"问题四",
  "Q5":"问题五",
  "Q6":"问题六",
  "Q7":"问题七",
  "Q8":"问题八"
}
```

### Response

#### Success Response

**Code**: 200

**Content**: 
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

### Notes

- The `phone` field should match the pattern: `^([0-9]{10})$`
- All date-time fields should be in ISO 8601 format
- The `source` field should be one of: FB, IG, or EDM