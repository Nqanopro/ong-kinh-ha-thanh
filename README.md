# Ống Kính Hà Thành

## Tên sản phẩm và tác giả

**Ống Kính Hà Thành** — Nguyễn Quốc Anh, MSV: 2071020006, Lớp CNTT 20-04.

## Sản phẩm này là gì?

Đây là website tĩnh HTML5/CSS3 giới thiệu Câu lạc bộ Nhiếp ảnh & Khám phá Đô thị Hà Nội (Ống Kính Hà Thành). Website trưng bày ảnh kèm chú thích, giới thiệu lịch Workshop/Photowalk định kỳ và có biểu mẫu đăng ký mô phỏng.

## Bản dùng thử và mã nguồn

- **GitHub Pages:** <https://nqanopro.github.io/ong-kinh-ha-thanh/>
- **Repository:** <https://github.com/Nqanopro/ong-kinh-ha-thanh>

Trang Pages hiện phản hồi HTTP 200 nhưng tại thời điểm kiểm tra vẫn hiển thị bản trước, dùng ba ảnh ở `assets/images/`. Phiên bản v3 trong hồ sơ này chưa được đẩy lên GitHub; cần cập nhật nhánh `main` và xác nhận lại trang Pages trước khi giới thiệu đây là bản trực tuyến cuối cùng.

## Tính năng chính

1. Điều hướng cuộn mượt tới ba phân mục: **Triển lãm**, **Lịch sinh hoạt** và **Tham gia CLB**.
2. Phần giới thiệu có ảnh banner và số liệu hoạt động câu lạc bộ.
3. Triển lãm góc nhìn thành viên hiển thị ba thẻ ảnh responsive, dùng `<figure>` và `<figcaption>`.
4. Bảng lịch Workshop định kỳ và biểu mẫu đăng ký dùng ràng buộc HTML5; dữ liệu hợp lệ được gửi bằng `GET` sang `ket-qua.html`.

## Cách mở và sử dụng

1. Mở <https://nqanopro.github.io/ong-kinh-ha-thanh/> sau khi bản v3 được xuất bản; hoặc mở `index.html` trực tiếp trong trình duyệt hay chạy qua Live Server.
2. Nhấn **Triển lãm**, **Lịch sinh hoạt** hoặc **Tham gia CLB** trên thanh điều hướng để tới từng khu vực nội dung.
3. Tại mục **Đăng ký tham gia cùng câu lạc bộ**, nhập họ tên, email và thông tin thiết bị; nhấn **Kiểm tra & Gửi đăng ký** để thử luồng xác nhận sang `ket-qua.html`.

## Cấu trúc thư mục

```text
ong-kinh-ha-thanh/
├── assets/
│   ├── anh-banner-pho-ha-noi.jpg
│   ├── ca-phe-pho.jpg
│   ├── do-thi-ben-song.jpg
│   └── ha-noi-pho-co.jpg
├── css/
│   └── styles.css
├── docs/
│   ├── AI_LOG.md
│   ├── evidence-index.md
│   └── evidence/
│       ├── 01-desktop-1440px.png
│       ├── 02-mobile-320px.png
│       ├── 03-form-validation-error.png
│       └── 04-form-submit-ket-qua.png
├── index.html
├── ket-qua.html
├── README.md
└── CHANGELOG.md
```

## Nguồn xuất bản và tài nguyên

- Cấu hình xuất bản được yêu cầu: GitHub Pages từ nhánh `main`, thư mục `/(root)`. Bản v3 cần được đồng bộ lên nhánh này và xác nhận trong **Settings → Pages**.
- Bốn tệp JPEG trong `assets/` được lưu cục bộ từ tư liệu Unsplash; ba ảnh dùng trong triển lãm, ảnh banner là bản cắt ngang từ ảnh phố Hà Nội. Phông chữ Be Vietnam Pro và Lora được nhúng từ Google Fonts.
- Nội dung lịch sinh hoạt và số liệu câu lạc bộ là dữ liệu mô phỏng phục vụ đồ án.

## Đã kiểm tra

Các kết quả kiểm thử và ảnh chụp được ghi trong [docs/evidence-index.md](./docs/evidence-index.md).

## Hạn chế và phần chưa kiểm tra

- Biểu mẫu chỉ kiểm tra dữ liệu trên trình duyệt rồi gửi bằng `GET`; chưa gửi email hoặc lưu dữ liệu vào cơ sở dữ liệu.
- Đã kiểm tra giao diện giả lập ở độ rộng 320px và 375px; chưa kiểm tra trên iPhone vật lý.
- Bản v3 trong workspace chưa được xuất bản lên GitHub Pages.

## Khai báo sử dụng AI

Nhật ký sử dụng AI và phần em rà soát, chỉnh sửa được ghi tại [docs/AI_LOG.md](./docs/AI_LOG.md).
