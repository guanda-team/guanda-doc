# AppServer 新需求

## 🔥 架構

```mermaid
flowchart TB
  AppServer -->|HTTP| 機台軟體
  AppServer -->|TCP| Database
  AppServer --> SharedMemory
```

---

## 🔥 Event

### 🔶 啟動時

- 由 DB 載入「是否啟用 App 配對」的旗標，並清除所有配對資料

### 🔶 App 註冊配料時

- 將配料資料寫入 DB

### 🔶 App 註銷配料時

- 將配料資料從 DB 移除

---

## 🔥 Api

### 🔶 設定是否啟用 App 配對

```http
POST {{url}}/api/enableAppPairing
Authorization: Bearer {{token}}
Content-Type: application/json

{
  "enable": true
}
```

### 🔶 機台軟體呼叫註冊配料

```http
POST {{url}}/api/registerAssmebly
Authorization: Bearer {{token}}
Content-Type: application/json

{
}
```

### 🔶 機台軟體呼叫註銷配料

```http
POST {{url}}/api/unregisterAssmebly
Authorization: Bearer {{token}}
Content-Type: application/json

{
}
```

### 🔶 查詢是否啟用 App 配對

```http
GET {{url}}/api/getEnableAppPairing
Authorization: Bearer {{token}}
```

### 🔶 輪詢 App 配料資料

```http
GET {{url}}/api/getAppPairingData
Authorization: Bearer {{token}}
```
