# Website: Thầy Lê Xuân Kỷ — Giáo viên Tin học THCS Tân Thanh

Trang web tĩnh, có thể triển khai nhanh trên GitHub Pages hoặc Vercel.

## Cấu trúc

```
.
├─ index.html
├─ styles.css
└─ README.md
```

## Chạy cục bộ

- Mở `index.html` bằng trình duyệt (double-click).

## Triển khai lên GitHub Pages

1. Tạo repository mới trên GitHub, ví dụ: `le-xuan-ky-site`.
2. Đưa mã nguồn lên:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: site Thay Le Xuan Ky"
   git branch -M main
   git remote add origin https://github.com/<username>/le-xuan-ky-site.git
   git push -u origin main
   ```
3. Trong GitHub repo → Settings → Pages → Source chọn `Deploy from a branch`, Branch chọn `main` và thư mục `/root`.
4. Chờ vài phút, trang sẽ có tại: `https://<username>.github.io/le-xuan-ky-site/`.

## Triển khai lên Vercel

1. Đăng nhập `https://vercel.com/`.
2. Import dự án trực tiếp từ GitHub repository vừa tạo.
3. Framework preset: chọn `Other` (vì đây là site tĩnh).
4. Nhấn Deploy. Sau ~1 phút sẽ có URL dạng `https://<project>.vercel.app`.

### Tuỳ chọn: Cấu hình domain tùy chỉnh
- Trên Vercel: vào `Settings → Domains` và thêm domain.
- Trên GitHub Pages: thêm DNS `CNAME` trỏ về GitHub Pages theo hướng dẫn của GitHub.

## Ghi chú bản quyền hình ảnh

Hình ảnh AI trong trang lấy từ Unsplash theo giấy phép tự do sử dụng. Bạn có thể thay bằng hình của trường hoặc ảnh cá nhân nếu có quyền sử dụng.
