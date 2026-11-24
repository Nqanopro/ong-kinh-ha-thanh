# Nhật ký sử dụng AI

Nhật ký này ghi lại phần hỗ trợ AI trong quá trình rà soát và hoàn thiện hồ sơ bàn giao v3. Các mục mô tả công việc thực hiện trong lượt hoàn thiện này; không suy diễn lịch sử AI trước đó từ trạng thái mã nguồn.

| Ngày | Dùng AI làm gì | Em sửa lại gì |
|---|---|---|
| 24/11/2026 | Hỗ trợ rà soát đường dẫn ảnh, định dạng tệp và cách bảng hiển thị trên màn hình hẹp. | Em kiểm tra ảnh trong mã nguồn, chuẩn hóa tên/định dạng JPEG, thêm banner cắt từ ảnh cục bộ; giữ `.table-wrap` và tự kiểm tra ở 320px, 375px. |
| 24/11/2026 | Hỗ trợ sắp xếp hồ sơ bàn giao v3 và soạn bảng đối chiếu kiểm thử. | Em đối chiếu từng nội dung với kết quả chạy thật, đặt tài liệu trong `docs/`, giữ lại giới hạn của bản Pages chưa cập nhật và ghi rõ phần chưa kiểm tra. |

## Lượt 1 — Ảnh cục bộ và bố cục màn hình hẹp

- **Bối cảnh:** Mã nguồn ban đầu đã dùng ảnh cục bộ, không còn liên kết ảnh bên ngoài trong các thẻ `<img>`. Ba tệp có đuôi `.jpg` nhưng nội dung thực tế là AVIF và nằm trong `assets/images/`. Bảng lịch đã được bọc bằng `.table-wrap` và CSS đã bật cuộn ngang.
- **AI hỗ trợ:** Rà soát đường dẫn và định dạng tài nguyên; đề xuất đưa các tệp ảnh vào một thư mục dễ theo dõi, dùng tên `kebab-case`, đồng thời kiểm tra lại hành vi responsive.
- **Em chỉnh sửa:** Chuyển ba ảnh thành JPEG thực, đổi tên và đặt trực tiếp trong `assets/`; tạo thêm một bản cắt ngang của ảnh phố Hà Nội để làm banner. Em giữ nguyên wrapper bảng hiện có thay vì thêm một cơ chế cuộn khác.
- **Em kiểm tra lại:** Bốn ảnh tải thành công trên bản chạy cục bộ. Ở 320px và 375px, lưới ảnh xếp một cột, menu xuống dòng, bảng cuộn trong `.table-wrap` và trang không tràn ngang. Chưa kiểm tra trên điện thoại vật lý.

## Lượt 2 — Chuẩn hóa hồ sơ bàn giao v3

- **Bối cảnh:** Tài liệu cũ nằm ở thư mục gốc và chưa có bảng minh chứng tập trung. Trang GitHub Pages công khai vẫn dùng ba ảnh cũ trong `assets/images/`.
- **AI hỗ trợ:** Đề xuất cấu trúc `docs/`, soạn README, CHANGELOG, nhật ký AI và bảng minh chứng theo yêu cầu bàn giao.
- **Em chỉnh sửa:** Đặt nhật ký AI và bảng minh chứng trong `docs/`, thay `RELEASE_NOTES.md` bằng `CHANGELOG.md`, cập nhật README và bổ sung bốn ảnh chụp kiểm thử thật. Em sửa mô tả để không khẳng định v3 đã xuất bản khi nhánh GitHub chưa có các thay đổi này.
- **Em kiểm tra lại:** Mở từng ảnh minh chứng, xác nhận URL `GET` trên Chrome và đối chiếu HTTP của trang Pages với kết quả kiểm tra bản cục bộ. Bản Pages cần được cập nhật riêng trước khi có thể xác nhận phiên bản công khai là v3.
