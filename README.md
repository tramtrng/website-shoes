# Website Bán Giày

Dự án là một website bán giày đơn giản được xây dựng bằng PHP, MySQL, HTML, CSS và JavaScript.

## Phạm vi dự án

Dự án này là một **Đồ án cơ sở 2** (đồ án môn học). Code dùng cho mục đích học tập, demo chức năng bán hàng cơ bản.

## Contributors

- Phạm Thị Phúc
- Trần Ngọc Trâm

## Mô tả

- Giao diện khách hàng nằm trong `admin/USERS/`
- Trang quản trị nằm trong `admin/admin/`
- Project sử dụng PHP để xử lý dữ liệu và MySQL để lưu trữ thông tin người dùng, sản phẩm, đơn hàng.
- Một số thư viện đã được tích hợp sẵn trong dự án:
  - `PHPMailer` để gửi email
  - `TFPDF` để xuất PDF
  - `CKEditor` để soạn thảo nội dung
  - `Carbon` để autoload và các tiện ích PHP
  - `FontAwesome` cho icon

## Yêu cầu

- PHP 7.x hoặc PHP 8.x
- MySQL / MariaDB
- Web server Apache
- Trình duyệt để xem giao diện

## Ngôn ngữ & Công nghệ

- PHP (server-side scripting)
- HTML5
- CSS3 (Sass/SCSS may be present in `USERS/sass/`)
- JavaScript (vanilla, plus libraries included with the template)
- MySQL / MariaDB (database)
- Thư viện/third-party: PHPMailer, TFPDF, CKEditor, Carbon, FontAwesome

## Cài đặt và chạy

1. Cài đặt XAMPP, WAMP, Laragon hoặc môi trường PHP + MySQL.
2. Import database từ file `doancs2_shoes (3).sql` vào MySQL.
3. Mở file cấu hình database `admin/admin/config/dbconfig.php` và cập nhật thông tin kết nối:

```php
$servername = "localhost";
$database = "doancs2_shoes";
$username = "pt_shops";
$password = "phuctram";
```

4. Đặt thư mục `admin/` làm thư mục gốc của web server hoặc cấu hình alias trỏ tới `admin/`.

### Nếu dùng XAMPP

- Copy toàn bộ thư mục `DOAN2_UPDATE3/admin` vào `xampp/htdocs/`
- Mở phpMyAdmin và import `doancs2_shoes (3).sql`
- Mở trình duyệt:
  - `http://localhost/USERS/index.php` để vào giao diện khách hàng
  - `http://localhost/admin/index.php` để vào trang quản trị

### Nếu dùng PHP Built-in Server

1. Mở terminal và chuyển đến thư mục `DOAN2_UPDATE3/admin`
2. Chạy:

```bash
php -S localhost:8000
```

3. Mở trình duyệt:
  - `http://localhost:8000/USERS/index.php`
  - `http://localhost:8000/admin/index.php`

> Lưu ý: Built-in PHP server chỉ dùng để thử nghiệm, không dùng cho môi trường production.

## Thông tin cấu trúc chính

- `admin/USERS/` - website khách hàng
- `admin/admin/` - trang quản trị
- `admin/admin/config/dbconfig.php` - cấu hình database
- `admin/mail/PHPMailer/` - thư viện gửi email
- `admin/tfpdf/` - thư viện tạo PDF
- `admin/resources/ckeditor/` - trình soạn thảo CKEditor
- `admin/carbon/` - autoload và thư viện PHP
