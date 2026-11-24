# Nhật ký phiên bản

## v3 (24/11/2026) - Bản bàn giao chính thức A3

- Chuẩn hóa hồ sơ trong `docs/`: thêm `evidence-index.md`, `AI_LOG.md` và `evidence/`; dùng `CHANGELOG.md` thay cho `RELEASE_NOTES.md`.
- Đổi tên, chuyển ảnh về trực tiếp trong `assets/` và lưu đúng định dạng JPEG; thêm ảnh banner cắt từ ảnh phố Hà Nội có sẵn.
- Bổ sung bốn ảnh chụp kiểm thử giao diện và biểu mẫu trên phiên bản v3 chạy cục bộ.
- Chuẩn hóa đường dẫn tài nguyên và mô tả nguồn Unsplash, Google Fonts.
- **Chưa kiểm tra:** giao diện trên điện thoại vật lý; hiện mới kiểm tra giả lập 320px và 375px. Bản v3 chưa được đẩy lên GitHub Pages; trang công khai vẫn là phiên bản trước.

## v2 (24/11/2026) - Bổ sung giao diện CSS3 và Responsive

- Hoàn thiện `css/styles.css` theo hướng Mobile-first; lưới ảnh đổi sang hai cột từ 640px và ba cột từ 960px.
- Bổ sung trạng thái `:hover`, `:focus-visible`, `:user-invalid`; bọc bảng lịch bằng `.table-wrap` để cuộn ngang trong khung hẹp.
- Dùng kiểm tra ràng buộc HTML5 và gửi biểu mẫu bằng `GET` tới `ket-qua.html`.
- **Đối chiếu Git:** lịch sử hiện có không tách riêng một commit cho mốc v2; các nội dung này đã xuất hiện trong commit khởi tạo mã nguồn bên dưới.

## v1 (24/11/2026) - Khởi tạo cấu trúc mã nguồn HTML5

- Xây dựng `index.html` và `ket-qua.html` với các phần tử HTML5 ngữ nghĩa như `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<table>` và `<footer>`.
- Lưu ba ảnh ban đầu trong `assets/images/`.
- **Commit mã nguồn trong Git:** [`f6035acb64da6d015ef546cd70065d04a30f6ab7`](https://github.com/Nqanopro/ong-kinh-ha-thanh/commit/f6035acb64da6d015ef546cd70065d04a30f6ab7).
