Instagram Clone – Nhóm F4

##  Giới thiệu dự án

Đây là dự án **Instagram Clone** được thực hiện nhằm mục đích học tập và thực hành phát triển ứng dụng web. Dự án mô phỏng một số chức năng cơ bản của mạng xã hội Instagram như đăng bài viết, hiển thị hình ảnh và tương tác người dùng.

---
## Thành viên nhóm

* Thành viên 1: Nguyễn Thúy Hằng
* Thành viên 2: Nguyễn Thị Tiên
* Thành viên 3: Trần Ngọc Minh Thư
* Thành viên 4: Trần Hoàng Lệ Trinh

---
## Công nghệ sử dụng

* **Ngôn ngữ:** PHP
* **Framework:** Laravel
* **Cơ sở dữ liệu:** MySQL
* **Front-end:** HTML, CSS, Blade Template
* **Công cụ hỗ trợ:** XAMPP, Composer, Git/GitHub

---

##  Hướng dẫn cài đặt và chạy dự án

### 1. Yêu cầu môi trường

* PHP >= 8.x
* Composer
* MySQL
* XAMPP hoặc Laragon

### 2. Clone source code

```bash
git clone https://github.com/tt1989182-cyber/nhomf4_igclone_.git
```

### 3. Cài đặt thư viện

```bash
cd nhomf4_igclone_
composer install
```

### 4. Tạo file môi trường

```bash
cp .env.example .env
php artisan key:generate
```

### 5. Cấu hình cơ sở dữ liệu

Mở file `.env` và chỉnh sửa thông tin database cho phù hợp:

```
DB_DATABASE=ten_database
DB_USERNAME=root
DB_PASSWORD=
```

### 6. Chạy migrate (nếu có)

```bash
php artisan migrate
```

### 7. Chạy dự án

```bash
php artisan serve
```

Sau đó truy cập trình duyệt tại: http://127.0.0.1:8000

## Cấu trúc thư mục chính
```text
nhomf4_igclone_/
├── .editorconfig
├── .env
├── .env.example
├── .gitattributes
├── .gitignore
├── artisan
├── composer.json
├── composer.lock
├── package.json
├── package-lock.json
├── phpunit.xml
├── README.md
├── structure.txt
├── vite.config.js
│
├── app/
│   ├── Http/
│   │   └── Controllers/
│   │       ├── Auth/
│   │       │   ├── ConfirmPasswordController.php
│   │       │   ├── ForgotPasswordController.php
│   │       │   ├── LoginController.php
│   │       │   ├── RegisterController.php
│   │       │   ├── ResetPasswordController.php
│   │       │   └── VerificationController.php
│   │       ├── CommentController.php
│   │       ├── Controller.php
│   │       ├── HomeController.php
│   │       ├── LikeController.php
│   │       ├── PostController.php
│   │       └── ProfileController.php
│   ├── Models/
│   │   ├── Comment.php
│   │   ├── Like.php
│   │   ├── Post.php
│   │   └── User.php
│   └── Providers/
│       └── AppServiceProvider.php
│
├── bootstrap/
│   ├── app.php
│   ├── providers.php
│   └── cache/
│       ├── .gitignore
│       ├── packages.php
│       └── services.php
│
├── config/
│   ├── app.php
│   ├── auth.php
│   ├── cache.php
│   ├── database.php
│   ├── filesystems.php
│   ├── logging.php
│   ├── mail.php
│   ├── queue.php
│   ├── services.php
│   └── session.php
│
├── database/
│   ├── factories/
│   │   └── UserFactory.php
│   ├── migrations/
│   │   ├── 0001_01_01_000001_create_cache_table.php
│   │   ├── 0001_01_01_000002_create_jobs_table.php
│   │   ├── 2025_03_10_201935_create_likes_table.php
│   │   ├── 2025_12_11_094953_create_users_table.php
│   │   ├── 2025_12_11_094954_create_comments_table.php
│   │   ├── 2025_12_11_094954_create_posts_table.php
│   │   ├── 2025_12_11_100742_create_sessions_table.php
│   │   ├── 2025_12_11_103353_alter_image_path_length_in_posts_table.php
│   │   ├── 2025_12_11_104018_add_columns_to_likes_table.php
│   │   ├── 2025_12_11_104206_add_post_id_and_user_id_to_comments_table.php
│   │   ├── 2025_12_11_104824_add_profile_fields_to_users_table.php
│   │   ├── 2025_12_11_111635_add_media_to_posts_table.php
│   │   ├── 2025_12_11_113302_add_comment_to_comments_table.php
│   │   ├── 2025_12_11_114410_add_extra_fields_to_users_table.php
│   │   ├── 2025_12_11_115201_add_image_path_to_posts_table.php
│   │   ├── 2025_12_11_120059_create_post_media_table.php
│   │   └── 2025_12_11_120635_create_post_media_table.php
│   └── seeders/
│       └── DatabaseSeeder.php
│
├── public/
│   ├── .htaccess
│   ├── favicon.ico
│   ├── index.php
│   ├── robots.txt
│   └── storage/
│
├── resources/
│   ├── css/
│   │   └── app.css
│   ├── js/
│   │   ├── app.js
│   │   └── bootstrap.js
│   ├── sass/
│   │   ├── app.scss
│   │   └── _variables.scss
│   └── views/
│       ├── auth/
│       │   ├── login.blade.php
│       │   ├── register.blade.php
│       │   ├── verify.blade.php
│       │   └── passwords/
│       │       ├── confirm.blade.php
│       │       ├── email.blade.php
│       │       └── reset.blade.php
│       ├── layouts/
│       │   └── app.blade.php
│       ├── posts/
│       │   ├── create.blade.php
│       │   ├── edit.blade.php
│       │   ├── index.blade.php
│       │   └── show.blade.php
│       ├── profiles/
│       │   ├── edit.blade.php
│       │   └── index.blade.php
│       ├── home.blade.php
│       └── welcome.blade.php
│
├── routes/
│   ├── console.php
│   └── web.php
│
├── storage/
│   ├── app/
│   │   ├── private/
│   │   └── public/
│   │       ├── profile/
│   │       └── uploads/
│   ├── framework/
│   │   ├── cache/
│   │   ├── sessions/
│   │   ├── testing/
│   │   └── views/
│   └── logs/
│       └── laravel.log
│
├── tests/
│   ├── Feature/
│   │   └── ExampleTest.php
│   ├── Unit/
│   │   └── ExampleTest.php
│   └── TestCase.php
│
└── vendor/
```
## Ghi chú

* Dự án **không có tài khoản admin riêng**.
* Các chức năng được xây dựng dựa trên source code của nhóm và phục vụ cho mục đích học tập.
* Giảng viên chỉ cần làm theo các bước cài đặt trên để chạy và chấm bài.

---

## Bản quyền

Dự án phục vụ **học tập – không sử dụng cho mục đích thương mại**.

