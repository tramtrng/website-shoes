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

## Giao diện sau khi hoàn thành

### Giao diện khách hàng (`admin/USERS/`)

- Trang chủ hiển thị danh sách sản phẩm
- Trang danh mục sản phẩm (`category.php`, `product_type.php`) cho phép lọc theo loại giày.
- Trang chi tiết sản phẩm (`single-product.php`) hiển thị thông tin, ảnh, giá và nút thêm vào giỏ hàng.
- Giỏ hàng (`cart.php`, `cart_tt.php`) hiển thị sản phẩm đã chọn, số lượng, tổng tiền và nút để thanh toán.
- Quy trình thanh toán (`checkout.php`, `thanhtoan.php`, `xulythanhtoan.php`) cho phép khách hàng nhập thông tin giao hàng và thanh toán.
- Trang lịch sử đơn hàng / xem đơn hàng (`lichsudonhang.php`, `xemdonhang.php`) để khách hàng quản lý đơn đã đặt.
- Trang liên hệ và hỗ trợ (`contac_us.php`, `contact_process.php`).

### Giao diện quản trị (`admin/admin/`)

- Trang đăng nhập quản trị để vào khu vực bảo mật.
- Bảng điều khiển tổng quan với các chỉ số cơ bản (đơn hàng, khách hàng, sản phẩm...).
- Quản lý sản phẩm và danh mục (`product_add.php`, `product_editing.php`, `view_product.php`, `view_categories.php`, `view_types_shose.php`).
- Quản lý đơn hàng (`indonhang.php`, `xemdonhang.php`, `xemdonhang.php`, `lietke.php`).
- Quản lý người dùng và liên hệ (`view_users.php`, `view_lienhe.php`, `view_tuvan.php`).
- Hỗ trợ xuất PDF đơn hàng và gửi email thông báo.

## Ảnh giao diện

### Ảnh 1: Giao diện login

![Giao diện login](docs/screenshots/login.jpg)

### Ảnh 2: Giao diện trang admin

![Giao diện admin](docs/screenshots/admin-dashboard.svg)

### Ảnh 3: Giao diện trang sản phẩm

![Giao diện trang sản phẩm](docs/screenshots/product-page.png)

## Thông tin cấu trúc chính

- `admin/USERS/` - website khách hàng
- `admin/admin/` - trang quản trị
- `admin/admin/config/dbconfig.php` - cấu hình database
- `admin/mail/PHPMailer/` - thư viện gửi email
- `admin/tfpdf/` - thư viện tạo PDF
- `admin/resources/ckeditor/` - trình soạn thảo CKEditor
- `admin/carbon/` - autoload và thư viện PHP
