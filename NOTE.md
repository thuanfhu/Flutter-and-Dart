# 🛠️ Project Creation & Setting Up a Code Editor for Flutter Development

## 📝 1. Tổng Quan Về Tạo Dự Án và Cài Đặt Trình Soạn Thảo Mã

Tạo dự án Flutter và thiết lập trình soạn thảo mã là bước đầu tiên để phát triển ứng dụng. Quá trình bao gồm di chuyển đến thư mục mong muốn, sử dụng lệnh `flutter create` để khởi tạo dự án, và cấu hình một trình soạn thảo mã như Visual Studio Code (VSCode) với các extension phù hợp. Tên dự án có thể sử dụng ký tự `_` (underscore) thay vì space hoặc `-` để đảm bảo tuân thủ quy tắc đặt tên của Dart/Flutter.

| **Bước**           | **Mô Tả**                                  |
|---------------------|--------------------------------------------|
| Di chuyển thư mục   | Chọn thư mục làm nơi chứa dự án            |
| Tạo dự án           | Sử dụng `flutter create` với tên hợp lệ    |
| Cài đặt trình soạn thảo | Cấu hình VSCode với extension Flutter    |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Tạo Dự Án Flutter

Di chuyển đến thư mục mong muốn và sử dụng lệnh `flutter create`.

Ví dụ:

```sh
cd ~/Documents/FlutterProjects
flutter create my_flutter_app
```

-> Mô tả: Di chuyển đến thư mục `FlutterProjects` và tạo dự án với tên `my_flutter_app`. Tên dự án nên dùng `_` (ví dụ: `my_flutter_app`) thay vì space hoặc `-` để tránh lỗi cú pháp Dart.

### 2.2. Cài Đặt Trình Soạn Thảo Mã (VSCode)

Cài đặt VSCode và thêm extension Flutter để hỗ trợ phát triển.

Ví dụ:

```sh
# Cài đặt VSCode (nếu chưa có)
# Tải từ https://code.visualstudio.com/

# Cài đặt extension Flutter
# Mở VSCode, vào Extensions (Ctrl+Shift+X), tìm và cài "Flutter"
```

-> Mô tả: Sau khi cài VSCode, thêm extension Flutter để có gợi ý mã, debug, và xem trước giao diện trực tiếp.

---

## 📌 3. Tóm Tắt

✅ **Tạo Dự Án**: Di chuyển thư mục, dùng `flutter create` với tên dùng `_` (không dùng space hoặc `-`).

✅ **Trình Soạn Thảo**: Nên dùng VSCode và cài extension Flutter để hỗ trợ phát triển.

---