# 🏃 Running a First Flutter App

## 📝 1. Tổng Quan Về Chạy Ứng Dụng Flutter Đầu Tiên

Chạy ứng dụng Flutter đầu tiên bao gồm mở simulator, sử dụng lệnh `flutter run` để khởi động ứng dụng, và kiểm tra hoạt động trên simulator. Với thiết bị ảo Pixel 9 chạy Android 16, bạn có thể sử dụng Android Emulator để xem trước và kiểm tra ứng dụng. Quá trình này giúp xác nhận mã nguồn hoạt động đúng trên môi trường mô phỏng.

| **Bước**           | **Mô Tả**                                  |
|---------------------|--------------------------------------------|
| Mở simulator        | Khởi động emulator Pixel 9 (Android 16)    |
| Chạy ứng dụng       | Sử dụng `flutter run`                      |
| Kiểm tra            | Xác nhận ứng dụng chạy trên simulator      |

---

## ⚙️ 2. Cú Pháp và Cách Sụng Dụng

### 2.1. Mở Simulator (Pixel 9 với Android 16)

Khởi động Android Emulator với cấu hình Pixel 9.

Ví dụ:
```sh
# Mở emulator Pixel 9
flutter emulators --launch pixel_9
```

-> Mô tả: Đảm bảo emulator Pixel 9 với Android 16 đã được tạo trước (qua Android Studio). Nếu chưa, tạo bằng: `flutter emulators --create --name pixel_9`.

### 2.2. Chạy Ứng Dụng với `flutter run`

Chạy ứng dụng Flutter trong thư mục dự án.

Ví dụ:
```sh
cd ~/Documents/FlutterProjects/my_flutter_app
flutter run
```

-> Mô tả: Lệnh này biên dịch và chạy ứng dụng trên emulator Pixel 9. Nhấn `r` để reload, `q` để thoát trong terminal.

### 2.3. Kiểm Tra Simulator

Xác nhận ứng dụng hiển thị đúng trên Pixel 9.

Ví dụ:
```sh
# Kiểm tra log trong terminal
flutter logs
```

-> Mô tả: Quan sát terminal để kiểm tra lỗi hoặc thông báo, đảm bảo giao diện hiển thị "Hello Flutter" (hoặc nội dung mặc định).

---

## 📌 3. Tóm Tắt

✅ **Mở Simulator**: Khởi động emulator Pixel 9 (Android 16) bằng `flutter emulators --launch`.

✅ **Chạy Ứng Dụng**: Sử dụng `flutter run` trong thư mục dự án.

✅ **Kiểm Tra**: Xác nhận giao diện và log trên simulator.

---