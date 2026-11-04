# Portfolio CV - Đinh Quang Thịnh

Trang portfolio/CV cá nhân giới thiệu Đinh Quang Thịnh, các kỹ năng Frontend, một số dự án tiêu biểu và thông tin liên hệ. Giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Hiển thị các kỹ năng và công nghệ.
- Trưng bày các dự án mẫu: ứng dụng trắc nghiệm, tra cứu phim, thương mại điện tử và trình phát nhạc.
- Điều hướng nhanh đến phần giới thiệu, kỹ năng, dự án và liên hệ.
- Cung cấp biểu mẫu liên hệ và liên kết email.
- Bố cục responsive, có thể xem trực tiếp bằng trình duyệt.

> **Lưu ý:** Đây là website tĩnh. Biểu mẫu liên hệ hiện chỉ có giao diện, chưa kết nối máy chủ hoặc dịch vụ gửi email nên nút gửi chưa chuyển thông tin đi đâu.

## Công nghệ

- **HTML5:** cấu trúc nội dung và các thành phần ngữ nghĩa.
- **CSS3:** giao diện, Flexbox, CSS Grid, responsive và hiệu ứng.
- **Git/GitHub:** quản lý mã nguồn.

JavaScript, Tailwind CSS, Webpack và các kỹ năng khác được liệt kê trong phần kỹ năng trên trang; dự án website hiện tại không cần các công cụ này để chạy.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không cần cài Node.js, npm hay cơ sở dữ liệu.
- Tùy chọn: Git để tải mã nguồn; Python 3 hoặc Docker nếu muốn chạy website qua máy chủ web cục bộ.

## Cài đặt

### Tải mã nguồn bằng Git

```bash
git clone https://github.com/dinhquangthinh2008-cmd/My-CV.git
cd My-CV
```

Hoặc tải repository dưới dạng ZIP từ GitHub và giải nén. Các lệnh chạy bên dưới cần được thực hiện tại thư mục chứa `index.html`.

## Cấu hình

Dự án không có bước cấu hình môi trường hay tệp `.env`. Để cá nhân hóa nội dung, chỉnh sửa `index.html`; để thay đổi giao diện, chỉnh sửa `assets/css/styles.css`. Ảnh được lưu trong `assets/img/`.

Trước khi công khai trang, hãy thay email mẫu `dinhquangthinh@example.com`, các liên kết `#` và thông tin GitHub/LinkedIn trong `index.html` bằng thông tin thật. Biểu mẫu chỉ hoạt động đầy đủ khi được tích hợp với backend hoặc dịch vụ xử lý biểu mẫu.

## Chạy thử

### Windows

**Mở trực tiếp:** mở `index.html` bằng trình duyệt.

**Chạy máy chủ cục bộ (Python 3):** mở PowerShell tại thư mục dự án rồi chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có sẵn, thử `python -m http.server 8000`. Mở [http://localhost:8000](http://localhost:8000) trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Docker

Cần cài và khởi động Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux). Chạy lệnh tại thư mục dự án để phục vụ website bằng Nginx:

**PowerShell (Windows):**

```powershell
docker run --rm --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm --name my-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, mở [http://localhost:8080](http://localhost:8080). Dừng bằng `Ctrl+C`; container sẽ tự được xóa nhờ tùy chọn `--rm`. Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`.

## Thông tin liên hệ

- **Tác giả:** Đinh Quang Thịnh
- **GitHub:** [dinhquangthinh-cmd](https://github.com/dinhquangthinh-cmd)
- **Email đang hiển thị trên trang:** `dinhquangthinh@example.com` (địa chỉ mẫu; vui lòng cập nhật trước khi sử dụng)
- **LinkedIn đang hiển thị trên trang:** `linkedin.com/in/dinhthinh` (hãy kiểm tra và thay bằng liên kết chính xác)
