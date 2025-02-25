# ARG AI 訂單 Web 系統

結合 OpenAI 和 LangChain 的智能訂單管理系統，提供 AI 對話式訂單服務。

## 功能特點

- 🤖 AI 智能對話：整合 OpenAI API 實現自然對話
- 📚 知識庫管理：使用 LangChain + FAISS 實現 RAG
- 🔄 即時更新：WebSocket 實現即時訂單狀態更新
- 📊 訂單管理：完整的訂單生命週期管理
- 🎯 客製化：支持訂單客製化選項

## 技術棧

- Python 3.8+
- Flask + Flask-SocketIO
- SQLAlchemy + SQLite
- OpenAI API
- LangChain + FAISS

## 安裝步驟

1. 克隆專案：
```bash
git clone https://github.com/your-username/arg-ai-order.git
cd arg-ai-order
```

2. 創建虛擬環境：
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows
```

3. 安裝依賴：
```bash
pip install -r requirements.txt
```

4. 設置環境變數：
```bash
cp .env.example .env
```
編輯 `.env` 文件，填入必要的配置信息

5. 初始化數據庫：
```bash
python init_db.py
```

6. 運行應用：
```bash
python app.py
```

訪問 http://localhost:8080 開始使用

## 配置

在 `.env` 文件中配置以下參數：

- `OPENAI_API_KEY`：OpenAI API 密鑰
- `FLASK_ENV`：運行環境（development/production）
- `SECRET_KEY`：Flask 密鑰
- `SQLALCHEMY_DATABASE_URI`：數據庫連接 URI

## 目錄結構

```
.
├── app.py              # 主應用程序
├── models.py           # 數據庫模型
├── init_db.py         # 數據庫初始化腳本
├── requirements.txt    # 依賴包列表
├── templates/         # HTML 模板
├── uploads/           # 上傳文件存儲
└── instance/          # 實例配置
```

## 貢獻

歡迎提交 Issue 和 Pull Request！

## 授權

MIT License

