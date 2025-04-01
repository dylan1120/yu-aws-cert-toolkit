# yu-aws-cert-toolkit
🎯 A developer-focused AWS toolkit for hands-on cloud development and automation.

This project is built with the goal of:
- Helping learners understand AWS services through practical code
- Demonstrating best practices for AWS SDK usage, serverless architecture, and infrastructure as code
- Serving as a personal portfolio to showcase cloud engineering skills

## Features

- 🗂️ Modular structure for each AWS service
- 🧪 Realistic code examples with test scripts
- 📦 Uses Python, Boto3, and AWS CLI
- 🔒 Easy to configure via `.env` file

## Getting Started

```bash
git clone https://github.com/YuHan/yu-aws-cert-toolkit.git
cd yu-aws-cert-toolkit
pip install -r requirements.txt
cp .env.example .env


yu-aws-cert-toolkit/
│
├── README.md                  # 專案說明：目的、功能模組、使用方法
├── requirements.txt           # Python 依賴套件清單
├── .env.example               # 範例環境變數檔案（如 AWS_KEY、REGION）
│
├── config/
│   └── aws_config.py          # 處理 AWS 認證與 boto3 session 建立
│
├── utils/
│   ├── logger.py              # 統一日誌格式
│   └── aws_helpers.py         # 共用 AWS 操作函式（如 create_client）
│
├── modules/                   # 核心功能模組
│   ├── s3_uploader/           
│   │   ├── s3_uploader.py     # 上傳檔案至 S3
│   │   └── test_s3_upload.py  # 單元測試或 demo script
│   │
│   ├── dynamodb_demo/
│   │   ├── dynamodb_setup.py  # 建立 DynamoDB table 並插入資料
│   │   └── test_dynamodb.py
│   │
│   ├── lambda_deploy/
│   │   ├── lambda_function.py # Lambda handler 內容
│   │   ├── deploy_lambda.py   # 上傳並部署 Lambda
│   │   └── test_lambda.py
│   │
│   ├── cloudformation_demo/
│   │   ├── template.yaml      # CloudFormation YAML 模板
│   │   ├── deploy_stack.py    # 建立 Stack
│   │   └── test_stack.py
│   │
│   ├── iam_roles_demo/
│   │   └── create_roles.py    # 建立 IAM Role 與權限
│   │
│   └── eventbridge_scheduler/
│       └── setup_scheduler.py # 建立排程觸發 Lambda
│
└── cli.py                     # 主 CLI 入口，可加參數執行特定模組
