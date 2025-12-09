# Code Sync Tool

從遠程下載 ZIP 並同步代碼的工具。

## 安裝

```bash
npm install --save-dev @sharedutils/code-sync
```

## 使用

在 `package.json` 中添加配置：

```json
{
  "scripts": {
    "code-sync": "code-sync"
  },
  "code-sync": [
    {
      "name": "shared-components",
      "zipUrl": "https://example.com/code.zip",
      "unzipPath": "./src/shared",
      "clean": true
    }
  ]
}
```

運行：

```bash
npm run code-sync              # 運行所有任務
npm run code-sync <task-name>  # 運行指定任務
```

## 配置項

| 字段 | 必需 | 說明 |
|------|------|------|
| name | ✅ | 任務名稱 |
| zipUrl | ✅ | ZIP 下載地址 |
| unzipPath | ✅ | 解壓目標路徑 |
| clean | ❌ | 解壓前清理目錄，默認 `false` |

## 許可證

ISC
