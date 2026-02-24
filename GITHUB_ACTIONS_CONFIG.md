# GitHub Actions 配置指南

## 1. Fork 仓库
点击右上角 `Fork` 按钮将仓库 fork 到你的 GitHub 账户

## 2. 配置 Secrets
在你的 forked 仓库中：
- 进入 `Settings` → `Secrets and variables` → `Actions`
- 点击 `New repository secret`

### 必需的 Secrets：

**AI 模型配置：**
```
Name: OPENAI_API_KEY
Value: sk-sp-4007e06bdda34e25bd828cf7b02fe709

Name: OPENAI_BASE_URL  
Value: https://dashscope.aliyuncs.com/compatible-mode/v1

Name: OPENAI_MODEL
Value: qwen-max
```

**股票列表：**
```
Name: STOCK_LIST
Value: 600519,000858,AAPL,TSLA  # 修改为你想要的股票
```

**QQ 邮箱配置：**
```
Name: EMAIL_SENDER
Value: your_qq_number@qq.com

Name: EMAIL_PASSWORD  
Value: your_qq_authorization_code  # QQ邮箱授权码，不是登录密码！

Name: EMAIL_RECEIVERS
Value: your_qq_number@qq.com  # 可以是同一个邮箱
```

### 可选的 Secrets（推荐）：
```
Name: TAVILY_API_KEYS
Value: your_tavily_api_key  # 新闻搜索，每月1000次免费

Name: REPORT_TYPE
Value: full  # 或 simple
```

## 3. 启用 Actions
- 进入 `Actions` 标签页
- 点击 `I understand my workflows, go ahead and enable them`

## 4. 手动测试
- 在 `Actions` 页面选择 `每日股票分析`
- 点击 `Run workflow` → `Run workflow`

## 5. 自动运行
默认每个**工作日 18:00（北京时间）**自动执行

## QQ 邮箱授权码获取步骤：
1. 登录 QQ 邮箱
2. 进入 `设置` → `账户`
3. 找到 `POP3/IMAP/SMTP/Exchange/CardDAV/CalDAV服务`
4. 开启 `SMTP服务`，系统会生成一个16位授权码
5. 将这个授权码填入 `EMAIL_PASSWORD` Secret 中

## 注意事项：
- Secrets 是加密存储的，不会泄露到代码中
- 至少配置一个通知渠道（邮箱、Telegram、企业微信等）
- AI 模型至少配置一个（你已经配置了百炼）
- 股票列表是必需的