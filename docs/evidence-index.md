# Bảng đối chiếu kiểm thử

Các kiểm thử của phiên bản v3 được thực hiện trên website chạy cục bộ trong trình duyệt Chrome. Các tệp PNG là ảnh chụp màn hình thật; ảnh desktop/mobile là ảnh toàn trang chụp với viewport tương ứng. Trang GitHub Pages được kiểm tra riêng, vì hiện chưa phản ánh các thay đổi v3 trong workspace.

| Em thử gì | Cách thao tác | Kết quả | Ảnh/link |
|---|---|---|---|
| Mở trang GitHub Pages công khai | Mở URL trong cửa sổ ẩn danh, sau đó kiểm tra phản hồi trang, CSS cùng ảnh hiện được tham chiếu. | Trang và `styles.css` trả HTTP 200; ba ảnh cũ trong `assets/images/` tải được. Trang công khai vẫn là bản trước v3, chưa có bốn ảnh mới trong `assets/`. | [GitHub Pages](https://nqanopro.github.io/ong-kinh-ha-thanh/) |
| Kiểm tra tài nguyên của bản v3 | Chạy bản v3 cục bộ, tải trang, stylesheet và bốn tệp ảnh trong `assets/`. | Trang, CSS và cả bốn ảnh JPEG trả HTTP 200; bốn ảnh tải thành công trong trình duyệt. | [Ảnh desktop](./evidence/01-desktop-1440px.png) |
| Bấm ba mục menu và kiểm tra focus | Lần lượt bấm **Triển lãm**, **Lịch sinh hoạt**, **Tham gia CLB**; dùng phím Tab để tới liên kết điều hướng. | Cả ba liên kết tới đúng phân mục. Liên kết đang focus có viền `:focus-visible` 3px. | [Ảnh desktop](./evidence/01-desktop-1440px.png) |
| Xem ở bề rộng 320px | Mô phỏng viewport 320×720; kiểm tra lưới ảnh, menu, chiều rộng trang và `.table-wrap`. | Lưới ảnh một cột; menu tự xuống hai hàng; bảng cuộn ngang bên trong wrapper (544px nội dung trong khung 286px); trang không tràn ngang. Kết quả tương tự ở 375px. | [Ảnh mobile 320px](./evidence/02-mobile-320px.png) |
| Thử biểu mẫu bỏ trống và email sai | Gửi form khi để trống; sau đó nhập đủ họ tên/nội dung nhưng dùng email `quocanh@` rồi gửi. | Trình duyệt chặn cả hai lần gửi. Email sai có `:user-invalid` và viền đỏ; trang không điều hướng. | [Ảnh lỗi kiểm tra form](./evidence/03-form-validation-error.png) |
| Gửi biểu mẫu hợp lệ | Nhập họ tên **Nguyễn Quốc Anh**, email `quocanh@example.com`, nội dung **Mình dùng điện thoại và muốn tham gia photowalk cuối tuần** rồi gửi. | Trình duyệt chuyển tới `ket-qua.html` bằng `GET`; các tham số `fullname`, `email`, `message` có mặt trên URL. Ảnh chụp cửa sổ Chrome gồm thanh địa chỉ và trang kết quả. | [Ảnh kết quả gửi form](./evidence/04-form-submit-ket-qua.png) |

## Trạng thái phát hành

Các kiểm thử responsive, điều hướng, biểu mẫu và bốn ảnh tài nguyên ở trên áp dụng cho bản v3 trong workspace. Nhánh `main` trên GitHub vẫn ở phiên bản trước khi thực hiện các thay đổi này; cần đẩy bản v3 lên và xác nhận lại GitHub Pages để cập nhật bản demo công khai.
