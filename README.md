# Ống Kính Hà Thành – Website Câu lạc bộ Nhiếp ảnh & Khám phá Đô thị Hà Nội

## Thông tin dự án

Website tĩnh giới thiệu câu lạc bộ nhiếp ảnh và các hoạt động khám phá đô thị Hà Nội. Trang chủ có phần giới thiệu, triển lãm ảnh, lịch workshop/photowalk và biểu mẫu đăng ký minh họa; `ket-qua.html` trình bày trạng thái sau khi trình duyệt kiểm tra biểu mẫu.

- **Tác giả:** Nguyễn Quốc Anh — MSV: 2071020006 — Lớp CNTT 20-04, Trường Đại học Đại Nam.
- **Repository:** [github.com/Nqanopro/ong-kinh-ha-thanh](https://github.com/Nqanopro/ong-kinh-ha-thanh)
- **GitHub Pages:** [https://nqanopro.github.io/ong-kinh-ha-thanh/](https://nqanopro.github.io/ong-kinh-ha-thanh/)
- **Nguồn xuất bản dự kiến:** nhánh `main`, thư mục `/` (root).
- **Mã nguồn đối chiếu tại thời điểm ghi tài liệu:** `f6035acb64da6d015ef546cd70065d04a30f6ab7` (`main`, `origin/main`). Lịch sử hiện có tag `v1`

## Cấu trúc thực tế

```text
ong-kinh-ha-thanh/
├── assets/
│   └── images/
│       ├── pic1.jpg
│       ├── pic2.jpg
│       └── pic3.jpg
├── css/
│   └── styles.css
├── index.html
├── ket-qua.html
├── README.md
├── AI_LOG.md
└── RELEASE_NOTES.md
```

## Mở và kiểm tra trên máy

1. Mở `index.html` trực tiếp bằng trình duyệt; các tệp CSS và ảnh dùng đường dẫn tương đối. Hoặc mở thư mục dự án trong VS Code và chạy `index.html` bằng tiện ích Live Server.
2. Kiểm tra các kích thước viewport 320px, 640px, 960px và 1440px. CSS dùng bố cục nền một cột, chuyển lưới ảnh sang hai cột từ 640px và ba cột từ 960px; điều hướng được phép xuống dòng.
3. Cuộn tới **Triển lãm**: xác nhận ba ảnh tải từ `assets/images/` và từng ảnh nằm trong `<figure>` có `<figcaption>`.
4. Cuộn tới **Lịch Workshop & Photowalk**: kiểm tra bảng; ở viewport hẹp bảng có vùng cuộn ngang trong `.table-wrap`.
5. Tại biểu mẫu, gửi khi trường bắt buộc còn trống để xem kiểm tra gốc của trình duyệt. Nhập họ tên (2–80 ký tự), email hợp lệ và nội dung (10–500 ký tự), sau đó gửi. Form dùng `GET` và điều hướng tới `ket-qua.html`; dữ liệu được truyền qua tham số URL, không được lưu trên máy chủ.

Đây là các bước kiểm tra đề xuất; tài liệu không khẳng định chúng đã được chạy trong phiên bàn giao này.

## GitHub Pages

Repository hiện có nhánh `main` và các trang HTML ở thư mục gốc, phù hợp với nguồn `main` / được yêu cầu. Cấu hình triển khai không nằm trong các tệp đang có ở workspace. Có thể kiểm tra hoặc đặt tại **Repository → Settings → Pages**, chọn deploy từ nhánh `main`, thư mục `/(root)`, rồi mở URL Pages ở trên để xác nhận.

## Tài liệu bàn giao

- [Nhật ký sử dụng AI và quyết định của sinh viên](AI_LOG.md)
- [Ghi chú phát hành](RELEASE_NOTES.md)
