# GitHub Actions Secrets 配置

在你的 GitHub 仓库中配置以下 Secrets：

## AI 模型配置
- **Name**: `OPENAI_API_KEY`
  - **Value**: `sk-sp-4007e06bdda34e25bd828cf7b02fe709`

- **Name**: `OPENAI_BASE_URL`
  - **Value**: `https://dashscope.aliyuncs.com/compatible-mode/v1`

- **Name**: `OPENAI_MODEL`
  - **Value**: `qwen-max`

## 股票配置
- **Name**: `STOCK_LIST`
  - **Value**: `600519,000858,AAPL,TSLA` (你可以修改为你想要的股票)

## 邮箱通知配置
- **Name**: `EMAIL_SENDER`
  - **Value**: `weisq.heimdall@foxmail.com`

- **Name**: `EMAIL_PASSWORD`
  - **Value**: `hgkpcmmbxgmteaff`

- **Name**: `EMAIL_RECEIVERS`
  - **Value**: `weisq.heimdall@foxmail.com`

## 其他可选配置
- **Name**: `REPORT_TYPE`
  - **Value**: `full`

- **Name**: `NEWS_MAX_AGE_DAYS`
  - **Value**: `3`

- **Name**: `BIAS_THRESHOLD`
  - **Value**: `5.0`

- **Name**: `ANALYSIS_DELAY`
  - **Value**: `10`