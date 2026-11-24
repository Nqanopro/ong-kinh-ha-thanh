# AI_LOG.md — Nhật ký sử dụng AI và quyết định của sinh viên

## Phạm vi và nguồn chứng cứ

Nhật ký này được lập khi rà soát mã nguồn và lịch sử Git trong workspace. Repository không chứa lịch sử hội thoại, prompt, bản nháp hay báo cáo chạy thử; vì vậy không thể xác nhận công cụ AI, câu lệnh đã dùng, gợi ý AI, các quyết định theo trình tự thời gian hoặc kết quả kiểm thử trước đây. Các mục dưới đây ghi nhận điều có thể kiểm chứng trong mã hiện tại, đồng thời đánh dấu rõ phần không có chứng cứ. Không xem các mô tả này là bản ghi hội thoại AI.

**Nguồn được kiểm tra:** `index.html`, `ket-qua.html`, `css/styles.css`, `assets/images/`, `git log`. HEAD là `f6035acb64da6d015ef546cd70065d04a30f6ab7`, commit `Add files via upload`; log cục bộ chỉ có hai commit. Không có tệp prompt hoặc test report trong cây dự án.

## 1. Ảnh triển lãm và đường dẫn tài nguyên

- **Hiện tượng/dữ kiện ban đầu:** Ba phần tử ảnh trong `index.html` tham chiếu `assets/images/pic1.jpg`, `pic2.jpg`, `pic3.jpg`. Cả ba tệp tồn tại tại các đường dẫn tương ứng trong repository.
- **Nhận định trước khi hỏi AI:** Không có ghi chép để xác nhận nhận định hoặc việc đã hỏi AI. Từ mã hiện tại có thể thấy ảnh được phục vụ cục bộ bằng đường dẫn tương đối.
- **Công cụ và prompt đã dùng:** Không được ghi lại trong workspace; không thể xác nhận.
- **Gợi ý từ AI:** Không có chứng cứ lưu trữ để xác nhận gợi ý nào.
- **Quyết định của sinh viên:** Mã hiện tại sử dụng các ảnh cục bộ. Đây là mô tả trạng thái mã, không đủ chứng cứ để kết luận sinh viên chuyển ảnh từ nguồn ngoài theo gợi ý AI.
- **Phần mã liên quan:** Các `<img>` trong `index.html`; tài nguyên `assets/images/pic1.jpg`, `pic2.jpg`, `pic3.jpg`.
- **Kiểm thử lại/kết quả thực tế:** Chưa có kết quả chạy trình duyệt được lưu. Có thể kiểm tra bằng cách mở trang và xác nhận ba ảnh tải; chưa xác nhận việc đó đã được thực hiện.

## 2. Bảng lịch trình ở màn hình hẹp

- **Hiện tượng/dữ kiện ban đầu:** `index.html` đặt bảng `.schedule-table` bên trong `<div class="table-wrap">`. `css/styles.css` đặt `overflow-x: auto` cho wrapper và `min-width: 34rem` cho bảng.
- **Nhận định trước khi hỏi AI:** Không có nhật ký nhận định hoặc trao đổi AI. Mã cho thấy bảng giữ độ rộng tối thiểu và wrapper cung cấp cuộn ngang.
- **Công cụ và prompt đã dùng:** Không có dữ liệu xác minh.
- **Gợi ý từ AI:** Không có dữ liệu xác minh.
- **Quyết định của sinh viên:** Cấu trúc bao bảng hiện tại hỗ trợ tràn nội dung theo chiều ngang trong vùng bảng; không thể xác nhận đây là quyết định sau một gợi ý AI.
- **Phần mã liên quan:** `.table-wrap`, `.schedule-table` trong `css/styles.css` và bảng lịch trong `index.html`.
- **Kiểm thử lại/kết quả thực tế:** Chưa có ảnh chụp hoặc báo cáo kiểm thử viewport 320px. Có thể đặt viewport 320px, cuộn ngang trong vùng bảng và quan sát trang không bị bảng ép rộng; kết quả thực tế chưa được ghi nhận.

## 3. Biểu mẫu đăng ký tĩnh

- **Hiện tượng/dữ kiện ban đầu:** Form trong `index.html` dùng `action="ket-qua.html"`, `method="get"`; trường họ tên, email và nội dung có ràng buộc HTML như `required`, `type="email"`, `minlength` và `maxlength`. `ket-qua.html` mô tả dữ liệu được truyền qua tham số URL và không được lưu vào cơ sở dữ liệu.
- **Nhận định trước khi hỏi AI:** Không có ghi chép trao đổi. Cấu hình hiện tại thể hiện kiểm tra bằng trình duyệt, không có xử lý phía máy chủ.
- **Công cụ và prompt đã dùng / gợi ý từ AI:** Không có chứng cứ để xác nhận.
- **Quyết định của sinh viên:** Mã hiện tại giữ luồng đăng ký ở mức tĩnh và thông báo giới hạn lưu trữ rõ trên trang kết quả. Không thể xác nhận lịch sử ra quyết định hoặc việc AI tham gia.
- **Phần mã liên quan:** `<form>` và các trường trong `index.html`; phần thông báo tại `ket-qua.html`.
- **Kiểm thử lại/kết quả thực tế:** Chưa có kết quả gửi form được lưu. Có thể thử gửi dữ liệu thiếu/sai định dạng để kiểm tra chặn của trình duyệt, rồi gửi dữ liệu đạt ràng buộc để kiểm tra điều hướng GET; chưa xác nhận các thao tác này đã chạy.

## 4. Bố cục và điểm ngắt responsive

- **Hiện tượng/dữ kiện ban đầu:** `css/styles.css` có media query tại `min-width: 640px` và `min-width: 960px`; lưới ảnh lần lượt có một, hai và ba cột. `.header-bar` và `.main-nav` dùng Flexbox kèm `flex-wrap: wrap`.
- **Nhận định, AI/prompt và quyết định theo thời gian:** Không có ghi chép đủ để tái dựng chuỗi tương tác hoặc xác định phần nào do AI đề xuất. Chỉ có thể mô tả quy tắc trong mã hiện tại.
- **Phần mã liên quan:** `css/styles.css`, các quy tắc `.header-bar`, `.main-nav`, `.photo-grid` và hai media query.
- **Kiểm thử lại/kết quả thực tế:** Không có báo cáo kiểm tra ở các độ rộng 320–1440px. Các kích thước này là kịch bản kiểm tra được đề xuất trong [README.md](README.md), không phải kết quả đã xác nhận.

## Kết luận về tính xác thực

Mã nguồn xác nhận các cấu trúc và hành vi khai báo nêu trên, nhưng không xác nhận lịch sử dùng AI hoặc việc chúng được kiểm thử thành công. Để hoàn thiện nhật ký sử dụng AI theo đúng trình tự thực tế, cần bổ sung prompt, gợi ý, quyết định và kết quả từ ghi chép thật của người thực hiện; không nên suy diễn các dữ kiện đó từ mã cuối cùng.
