# RELEASE_NOTES.md

## Ống Kính Hà Thành — v8 (bản ghi bàn giao)

- **Ngày cập nhật tài liệu:** 24/11/2026.
- **Commit mã nguồn được đối chiếu:** [`f6035acb64da6d015ef546cd70065d04a30f6ab7`](https://github.com/Nqanopro/ong-kinh-ha-thanh/commit/f6035acb64da6d015ef546cd70065d04a30f6ab7) (`Add files via upload`, ngày 2026-11-24).
- **Nhánh:** `main` (HEAD trỏ tới `origin/main`).
- **Tag Git quan sát được:** `v1`. Lịch sử cục bộ có hai commit và không có tag `v8`. Vì vậy `v8` ở tiêu đề là phiên bản hồ sơ bàn giao theo yêu cầu, không phải phiên bản được xác nhận bởi tag hoặc metadata phát hành Git.

## Nội dung sản phẩm

- Hai trang HTML5 dùng cấu trúc ngữ nghĩa như `header`, `nav`, `main`, `section`, `article`, `figure`, `table`, `form` và `footer`.
- CSS dùng Grid và Flexbox. Bố cục cơ sở áp dụng ở màn hình nhỏ; media query tại 640px đổi lưới ảnh thành hai cột và tại 960px thành ba cột. Đây là các điểm ngắt trong mã; chưa có kết quả đo kiểm dải 320–1440px được lưu.
- Triển lãm có ba ảnh cục bộ tại `assets/images/`, kèm `alt` và chú thích `<figcaption>`.
- Bảng lịch được bọc trong `.table-wrap` có cuộn ngang; bảng đặt độ rộng tối thiểu 34rem.
- Biểu mẫu dùng kiểm tra HTML5 phía trình duyệt (`required`, `type="email"`, giới hạn độ dài) và gửi bằng GET tới `ket-qua.html`.

## Lỗi và điểm cần xác nhận trước khi đóng gói

- Các ảnh triển lãm đang tham chiếu tài nguyên cục bộ bằng đường dẫn tương đối; ba tệp đích hiện diện trong repository.
- Bảng lịch có wrapper cuộn ngang trong CSS để xử lý độ rộng nhỏ.
- Không có lịch sử chi tiết hoặc báo cáo kiểm thử để chứng minh thời điểm và cách khắc phục các lỗi trước đây; không thể ghi nhận cụ thể lỗi nào đã được sửa dựa trên `git log` hiện có.
- Cấu hình GitHub Pages không có trong cây tệp đã kiểm tra và không thể truy cập URL từ môi trường rà soát. URL dự kiến là <https://nqanopro.github.io/ong-kinh-ha-thanh/>; cần xác minh trạng thái triển khai thực tế.
- Hồ sơ ghi phiên bản `v8`, trong khi repository hiện chỉ có tag `v1`; cần đối chiếu quy ước phiên bản của hồ sơ với người bàn giao.

## Giới hạn hiện tại

Biểu mẫu chỉ thực hiện kiểm tra phía trình duyệt, sau đó gửi dữ liệu qua phương thức GET và điều hướng sang `ket-qua.html`. Không có backend hoặc cơ sở dữ liệu, không lưu thông tin đăng ký và không gửi email thực tế. Dữ liệu biểu mẫu có thể xuất hiện trong URL khi gửi.

## Tiếp tục kiểm tra và đối chiếu

1. Mở `index.html` trực tiếp hoặc qua Live Server; xem kịch bản kiểm tra giao diện và form trong [README.md](README.md).
2. Xác nhận trên GitHub rằng Pages được xuất bản từ `main` / và truy cập URL triển khai.
3. Trước khi cập nhật mã, ghi lại `git rev-parse HEAD`, `git log -1 --oneline` và `git tag --list`; đối chiếu hash với commit nêu trên. Sau mỗi thay đổi, hash HEAD sẽ khác.
4. Nếu quy trình yêu cầu tag phát hành `v8`, tạo và đẩy tag qua quy trình Git của người bàn giao; tài liệu này không khẳng định tag đó đã tồn tại.
