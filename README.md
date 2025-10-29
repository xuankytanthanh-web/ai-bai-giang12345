## AI Tạo Bài Giảng Điện Tử - Trường THCS Tân Thanh

Hệ thống tạo giáo án tự động bằng AI, hỗ trợ xuất file Word và PowerPoint.

### ✨ Tính năng
- Tạo nội dung giáo án tự động với OpenAI GPT
- Xuất file Word (.docx) theo mẫu 5512
- Xuất file PowerPoint (.pptx) với slides tự động
- Giao diện web hiện đại, responsive

### 📁 Cấu trúc dự án
```
.
├── AI-TAO-BAI-GIANG-DIEN-TU/    # Mã nguồn chính
│   ├── app.py                    # Flask application
│   ├── templates/                # HTML templates
│   └── static/                   # CSS, JS files
├── api/
│   └── index.py                  # Vercel serverless entry point
├── requirements.txt             # Python dependencies
├── vercel.json                  # Vercel configuration
└── README.md                    # Tài liệu này
```

### 🚀 Chạy cục bộ (Windows)

**Cách 1: Dùng script tự động**
```powershell
cd "AI-TAO-BAI-GIANG-DIEN-TU"
./setup.ps1
```

**Cách 2: Chạy thủ công**
```powershell
cd "AI-TAO-BAI-GIANG-DIEN-TU"
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -U pip
pip install -r ../requirements.txt
$env:OPENAI_API_KEY = "sk-your-key-here"
python app.py
```

Truy cập: http://127.0.0.1:5000

### 📤 Đẩy lên GitHub

```bash
# Khởi tạo git repo (nếu chưa có)
git init

# Thêm tất cả files
git add .

# Commit
git commit -m "Initial commit: AI Tạo Bài Giảng with Vercel deployment"

# Đổi tên branch thành main
git branch -M main

# Thêm remote (thay <username> và <repo-name> bằng thông tin của bạn)
git remote add origin https://github.com/<username>/<repo-name>.git

# Đẩy lên GitHub
git push -u origin main
```

### 🌐 Deploy lên Vercel

1. **Tạo project trên Vercel:**
   - Truy cập [vercel.com](https://vercel.com)
   - Đăng nhập và chọn "New Project"
   - Import GitHub repository vừa tạo

2. **Thiết lập Environment Variables:**
   - Vào **Project Settings** → **Environment Variables**
   - Thêm các biến sau:
     ```
     OPENAI_API_KEY = sk-your-openai-api-key-here
     SECRET_KEY = your-secret-key-here (tùy chọn)
     OPENAI_MODEL = gpt-4o-mini (tùy chọn, nếu muốn chỉ định model cụ thể)
     ```

3. **Deploy:**
   - Nhấn **Deploy**
   - Vercel sẽ tự động:
     - Cài đặt dependencies từ `requirements.txt`
     - Build và deploy ứng dụng
     - Cấu hình routing theo `vercel.json`

4. **Kiểm tra:**
   - Sau khi deploy thành công, truy cập URL do Vercel cung cấp
   - Ứng dụng sẽ tự động có HTTPS và CDN

### 🔧 Xử lý lỗi

**Lỗi 404 NOT_FOUND:**
- Kiểm tra `OPENAI_API_KEY` đã được thiết lập đúng trong Vercel
- Kiểm tra model OpenAI có sẵn với tài khoản của bạn
- Xem logs trong Vercel Dashboard → Deployments → Logs

**Lỗi Import hoặc đường dẫn:**
- Đảm bảo cấu trúc thư mục đúng như trong README
- Kiểm tra `vercel.json` có đúng cấu hình

**Lỗi static files không load:**
- Đảm bảo các file trong `static/` đã được commit lên GitHub
- Kiểm tra đường dẫn trong HTML template (`/static/css/style.css`, `/static/js/script.js`)

### 📝 Yêu cầu hệ thống
- Python 3.11+
- OpenAI API key (từ [platform.openai.com](https://platform.openai.com))
- Tài khoản Vercel (miễn phí)

### 📄 License
© 2025 Trường THCS Tân Thanh


