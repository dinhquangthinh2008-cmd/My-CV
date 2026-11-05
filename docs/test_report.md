# BÁO CÁO KIỂM THỬ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio CV — Đinh Quang Thịnh |
| Phiên bản | v1.0.0 |
| Ngày kiểm thử | 05/11/2026 |
| Người thực hiện/đánh giá | Chưa xác định |
| Phạm vi | Đối chiếu mã nguồn, nội dung, tài liệu và các yêu cầu trước bàn giao |
| Hình thức đánh giá | Rà soát tĩnh tài liệu HTML/CSS và README; chưa xác nhận kiểm thử trực tiếp trên trình duyệt |

### Quy ước trạng thái

- **Đạt:** Có đủ căn cứ xác nhận hạng mục đáp ứng yêu cầu trong phạm vi đánh giá.
- **Chưa đạt:** Đã phát hiện vấn đề cụ thể cần xử lý trước khi chấp nhận.
- **Cần cải thiện:** Chưa có đủ minh chứng, cần kiểm tra bổ sung hoặc hoàn thiện để tăng mức độ sẵn sàng.

> Trạng thái trong báo cáo phản ánh rà soát tĩnh hiện có. Các hạng mục chưa chạy thử được ghi rõ là chưa xác minh, không được xem là đã kiểm thử thành công.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Chưa đạt | Trang có nội dung portfolio và điều hướng; biểu mẫu chưa gửi dữ liệu, một số liên kết dự án/mạng xã hội đang để `#`. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Chưa đạt | Đã chụp minh chứng tại mobile, tablet và desktop; ảnh mobile cho thấy nội dung bị tràn/cắt ngang. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Có hướng dẫn chạy website tĩnh; chưa có kết quả đo hiệu năng hoặc kiểm tra lỗi khi vận hành. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy quy trình backend trong phạm vi rà soát; cần xác nhận cách xử lý dữ liệu biểu mẫu, HTTPS và thông tin công khai trước phát hành. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Chưa đạt | Có README và release note; phát hiện ID `contact` bị lặp và một số nội dung/đường dẫn mẫu chưa hoàn thiện. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã lưu minh chứng ảnh responsive cho mobile/tablet/desktop; chưa có biên bản chạy thử trên môi trường sạch hoặc kết quả kiểm thử tổng thể. |

## 3. Nội dung chi tiết theo tiêu chí

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Nội dung giới thiệu, kỹ năng và dự án được tổ chức thành các mục riêng | Đạt | Có các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ trong `index.html`. |
| Điều hướng nội bộ đến các mục trên trang | Cần cải thiện | Các liên kết `#about`, `#skills`, `#projects`, `#contact` được khai báo; cần chạy thử các liên kết trên trình duyệt, đặc biệt do trang hiện có hai phần cùng khai báo `id="contact"`. |
| Liên kết xem chi tiết dự án | Chưa đạt | Các nút “Xem chi tiết” trong thẻ dự án đang dùng `href="#"`, chưa dẫn đến nội dung dự án. |
| Liên kết GitHub và LinkedIn | Chưa đạt | Các liên kết này đang dùng `href="#"`; cần thay bằng URL chính xác và kiểm tra đích đến. |
| Biểu mẫu liên hệ gửi và xử lý dữ liệu | Chưa đạt | Form chưa khai báo `action`/`method`, các trường chưa có thuộc tính `name` và chưa thấy tích hợp dịch vụ gửi dữ liệu. README cũng ghi nhận form chưa kết nối backend/dịch vụ email. |
| Kiểm tra dữ liệu nhập bắt buộc ở mức trình duyệt | Cần cải thiện | Có các thuộc tính `required` và trường email dùng `type="email"`; cần kiểm thử các trường hợp hợp lệ/không hợp lệ trên trình duyệt. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Bố cục responsive trên màn hình nhỏ, vừa và lớn | Chưa đạt | Đã chụp tại viewport mobile 390×844, tablet 768×1024 và desktop 1366×900. Ảnh mobile cho thấy phần mô tả và ảnh đại diện tràn khỏi khung nhìn, bị cắt ở mép phải; cần sửa và chụp lại để xác nhận. |
| Điều hướng và khả năng nhận biết các khu vực nội dung | Cần cải thiện | Có `header`, `nav`, `main`, `section` và `footer`; cần kiểm tra trực quan thứ tự tab, trạng thái focus và trải nghiệm trên màn hình nhỏ. |
| Văn bản thay thế cho hình ảnh | Đạt | Các ảnh đại diện và ảnh dự án trong `index.html` có khai báo `alt`; cần xác nhận nội dung mô tả phù hợp với ảnh thực tế. |
| Tính duy nhất của ID trong tài liệu | Chưa đạt | `index.html` khai báo `id="contact"` ở hai section. ID trùng có thể khiến điều hướng và công nghệ hỗ trợ xác định sai vị trí. |
| Khả năng đọc và độ tương phản màu sắc | Cần cải thiện | CSS định nghĩa màu nền, chữ và viền; chưa có kết quả đo tương phản hoặc đánh giá khả năng đọc trên thiết bị khác nhau. |
| Chính tả và tính nhất quán nội dung | Cần cải thiện | Cần rà soát nội dung mô tả dự án và thông tin liên hệ trước bàn giao; ví dụ có lỗi đánh máy trong mô tả dự án và một số thông tin còn là mẫu. |
| Tương thích trình duyệt | Cần cải thiện | Chưa có biên bản kiểm tra trên Chrome, Edge, Firefox hoặc Safari. |

#### Minh chứng ảnh chụp responsive

Ảnh được chụp trực tiếp từ trang bằng Chrome headless, không chỉnh sửa nội dung giao diện. Mỗi ảnh ghi lại viewport ban đầu; chưa phải ảnh chụp toàn bộ trang.

| Thiết bị mô phỏng | Viewport | Minh chứng |
|---|---:|---|
| Mobile | 390×844 | [responsive-mobile-390x844.png](screenshots/responsive-mobile-390x844.png) |
| Tablet | 768×1024 | [responsive-tablet-768x1024.png](screenshots/responsive-tablet-768x1024.png) |
| Desktop | 1366×900 | [responsive-desktop-1366x900.png](screenshots/responsive-desktop-1366x900.png) |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Khởi chạy website theo hướng dẫn bàn giao | Cần cải thiện | README hướng dẫn mở `index.html`, chạy Python HTTP server hoặc dùng Docker/Nginx; chưa xác nhận các bước này trên môi trường sạch. |
| Tải tài nguyên tĩnh | Cần cải thiện | Trang tham chiếu CSS và ảnh bằng đường dẫn tương đối; cần chạy website từ thư mục gốc và kiểm tra lỗi 404 trong Network/Console. |
| Hành vi khi gửi biểu mẫu | Chưa đạt | Form chưa được kết nối xử lý; cần tránh tạo cảm giác dữ liệu đã được gửi thành công khi chưa có dịch vụ nhận dữ liệu. |
| Lỗi JavaScript và lỗi trình duyệt | Cần cải thiện | Chưa có biên bản kiểm tra Console. |
| Hiệu năng tải trang cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước ảnh hoặc chỉ số hiệu năng bằng công cụ trình duyệt/Lighthouse. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Thông tin bí mật/khóa truy cập trong mã nguồn | Cần cải thiện | Đây là rà soát tĩnh giới hạn; cần kiểm tra toàn bộ repository và lịch sử mã nguồn trước khi công khai. |
| Thông tin cá nhân và liên kết công khai | Chưa đạt | Email mẫu `dinhquangthinh@example.com` và một số liên kết mẫu còn xuất hiện; xác nhận/cập nhật nội dung được phép công khai trước phát hành. |
| Thu thập, truyền và lưu dữ liệu từ biểu mẫu | Cần cải thiện | Chưa thấy backend hoặc chính sách lưu trữ dữ liệu. Nếu tích hợp form, cần xác định nơi nhận, mục đích sử dụng, thời hạn lưu và thông báo cho người dùng. |
| Bảo vệ dữ liệu khi triển khai | Cần cải thiện | README mô tả các cách chạy cục bộ; cấu hình HTTPS và bảo vệ dữ liệu trên môi trường triển khai chưa được xác minh. |
| Quản lý cấu hình môi trường | Đạt | README cho biết dự án không yêu cầu tệp `.env` hoặc bước cấu hình môi trường; cần đánh giá lại nếu bổ sung backend/dịch vụ bên ngoài. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Tách cấu trúc HTML và CSS | Đạt | HTML nằm trong `index.html`; stylesheet được đặt tại `assets/css/styles.css`. |
| Tính nhất quán của cấu trúc HTML | Chưa đạt | Có hai section cùng `id="contact"` trong `index.html`; cần gộp hoặc đổi ID và cập nhật điều hướng tương ứng. |
| Tính chính xác của nội dung | Cần cải thiện | Cần rà soát chính tả, mô tả dự án, email và các URL mẫu trước khi phát hành. |
| Hướng dẫn cài đặt/chạy dự án | Đạt | `README.md` có hướng dẫn chạy trực tiếp, Python HTTP server và Docker/Nginx trên các hệ điều hành. |
| Tài liệu release note | Đạt | `docs/RELEASENOTE.md` ghi nhận phiên bản v1.0.0, chức năng và các hạn chế đã biết. |
| Tài liệu thay đổi lớn | Cần cải thiện | `docs/AI_LOG.md` có ghi nhận phát hành; cần tiếp tục cập nhật khi có thay đổi lớn tiếp theo. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng cụ thể |
|---|---|---|
| Có hướng dẫn triển khai/chạy cục bộ | Đạt | `README.md` mô tả chạy bằng trình duyệt, Python server và Docker/Nginx. |
| Kiểm tra quy trình triển khai trên môi trường sạch | Cần cải thiện | Chưa có kết quả thực thi hoặc biên bản xác nhận các hướng dẫn hoạt động từ bản tải mới. |
| Có bộ kiểm thử tự động và kết quả chạy | Cần cải thiện | Chưa có kết quả kiểm thử tự động được cung cấp trong phạm vi báo cáo. |
| Kiểm thử thủ công trên trình duyệt/thiết bị | Cần cải thiện | Chưa có ma trận trình duyệt, thiết bị, phiên bản hoặc kết quả pass/fail kèm theo. |
| Minh chứng kiểm thử có thể đối chiếu | Cần cải thiện | Cần bổ sung ảnh chụp màn hình, kết quả Console/Network và thông tin môi trường cho các hạng mục đã kiểm tra. |
| Thông tin người kiểm thử và phê duyệt | Cần cải thiện | Chưa xác định người thực hiện, người đánh giá và người chấp thuận bàn giao. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm hiện có cấu trúc portfolio tĩnh, các mục nội dung chính, stylesheet responsive và tài liệu hướng dẫn chạy. Tuy nhiên, báo cáo hiện dựa trên rà soát tĩnh; chưa có minh chứng kiểm thử vận hành trên trình duyệt hoặc môi trường triển khai. Một số vấn đề chức năng và cấu trúc đã được phát hiện, do đó **chưa đủ căn cứ để xác nhận sản phẩm sẵn sàng bàn giao**.

### Vấn đề cần ưu tiên xử lý

1. **Ưu tiên cao:** Gộp hoặc đổi ID `contact` đang bị trùng; kiểm tra lại mọi liên kết điều hướng.
2. **Ưu tiên cao:** Quyết định cách xử lý biểu mẫu. Nếu form chưa được hỗ trợ, thông báo rõ cho người dùng và không thể hiện rằng dữ liệu đã gửi; nếu cần gửi dữ liệu, tích hợp và kiểm thử dịch vụ nhận form.
3. **Ưu tiên cao:** Thay các liên kết `#` của dự án/GitHub/LinkedIn bằng đích đến hợp lệ hoặc bỏ các liên kết chưa sẵn sàng.
4. **Ưu tiên trung bình:** Xác nhận email và thông tin cá nhân được phép công khai; rà soát chính tả và nội dung mô tả.
5. **Ưu tiên cao:** Sửa hiện tượng tràn/cắt nội dung ở viewport mobile, sau đó chụp lại và xác nhận responsive trên mobile, tablet, desktop. Hoàn tất thêm kiểm thử trình duyệt, liên kết, tài nguyên, form và lỗi Console; lưu minh chứng.
6. **Trước bàn giao:** Chạy lại quy trình từ hướng dẫn README trên môi trường sạch và cập nhật trạng thái từng hạng mục sau khi có minh chứng.

### Kết luận bàn giao

- **Trạng thái đề xuất:** Chưa chấp thuận bàn giao chính thức.
- **Điều kiện xem xét lại:** Khắc phục các vấn đề ưu tiên cao, hoàn tất kiểm thử thực tế, đính kèm minh chứng và được người phụ trách xác nhận.

## 5. Xác nhận

| Vai trò | Họ tên | Ngày | Xác nhận |
|---|---|---|---|
| Người kiểm thử | Chưa xác định |  |  |
| Người đánh giá | Chưa xác định |  |  |
| Người phụ trách bàn giao | Chưa xác định |  |  |
