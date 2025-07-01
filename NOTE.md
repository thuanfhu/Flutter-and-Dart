# 🛠️ From Dart To Machine Code

## 📝 1. Tổng Quan Về Quá Trình Biên Dịch Từ Dart Sang Mã Máy

Mã Dart và Flutter được biên dịch thành mã máy để chạy trên các thiết bị di động (iOS hoặc Android) thông qua quy trình do Dart và Flutter tools quản lý. Quá trình này bao gồm việc phân tích cú pháp mã Dart từ trên xuống dưới, sau đó biên dịch thành mã native hoặc mã máy (machine code) để thực thi trực tiếp trên thiết bị. Điều này đảm bảo hiệu suất cao và tích hợp mượt mà với nền tảng.

| **Giai Đoạn**      | **Mô Tả**                                  |
|--------------------|--------------------------------------------|
| Phân tích cú pháp  | Xử lý mã Dart từ trên xuống dưới           |
| Biên dịch          | Chuyển thành mã native/mã máy              |
| Thực thi           | Chạy trên thiết bị di động                 |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Phân Tích Cú Pháp Từ Trên Xuống Dưới

Mã Dart được đọc và phân tích bởi Dart analyzer trước khi biên dịch.

Ví dụ:
```dart
void main() {
  runApp(const MyApp());
}
```

-> Mô tả: Mã trên được phân tích từ `void main()` xuống `runApp()`, đảm bảo cú pháp đúng trước khi biên dịch.

### 2.2. Biên Dịch Thành Mã Native/Máy

Flutter tools sử dụng AOT (Ahead-Of-Time) compilation để tạo mã máy.

Ví dụ:
```sh
flutter build apk
```

-> Mô tả: Lệnh này biên dịch mã Dart thành mã máy cho Android, cho phép ứng dụng chạy trực tiếp trên thiết bị.

### 2.3. Thực Thi Trên Thiết Bị

Mã máy được thực thi trên máy ảo hoặc phần cứng thiết bị.

Ví dụ:
```sh
flutter run
```

-> Mô tả: Sau biên dịch, ứng dụng chạy trên emulator hoặc thiết bị thực, tận dụng mã native cho hiệu suất cao.

---

## 📌 3. Tóm Tắt

✅ **Phân Tích Cú Pháp**: Xử lý mã Dart từ trên xuống dưới.

✅ **Biên Dịch**: Chuyển thành mã native/máy bằng Flutter tools với AOT compilation.

✅ **Thực Thi**: Chạy trực tiếp trên thiết bị di động (iOS/Android).

---