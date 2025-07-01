# 🛠️ Understanding "const" Values

## 📝 1. Tổng Quan Về Giá Trị "const"

Trong Dart (ngôn ngữ của Flutter), từ khóa `const` được sử dụng để khai báo các giá trị không đổi (constant values) tại thời điểm biên dịch, giúp tối ưu hóa hiệu suất runtime. Khi một widget như `Text` được khai báo với `const`, Dart chỉ lưu một bản sao duy nhất trong bộ nhớ thiết bị (Device Memory), ngay cả khi được sử dụng nhiều lần trong ứng dụng. Điều này giảm tiêu tốn tài nguyên bằng cách tái sử dụng cùng một đối tượng bộ nhớ (ví dụ: địa chỉ bộ nhớ `<0x021d36e0>` cho `Text widget A`) thay vì tạo mới mỗi lần.

| **Khái Niệm**       | **Mô Tả**                                  |
|---------------------|--------------------------------------------|
| `const`             | Khai báo giá trị không đổi                 |
| Tối ưu hóa bộ nhớ   | Tái sử dụng đối tượng trong bộ nhớ         |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Khai Báo `const` trong Widget

Sử dụng `const` để khai báo widget không đổi, như `Text`.

Ví dụ:
```dart
const Text('Hello World!') // Được định nghĩa và sử dụng lần đầu
```

-> Mô tả: Widget `Text` được đánh dấu `const`, tạo một đối tượng cố định trong bộ nhớ.

### 2.2. Tác Động Đến Bộ Nhớ Thiết Bị

Giá trị `const` được lưu trong Device Memory và tái sử dụng.

Ví dụ:
```dart
void main() {
  const widgetA = Text('Hello World!');
  const widgetB = Text('Hello World!');
  print(identical(widgetA, widgetB)); // Trả về true, cùng đối tượng
}
```

-> Mô tả: `identical()` xác nhận `widgetA` và `widgetB` là cùng một đối tượng trong bộ nhớ.

---

## 📌 3. Tóm Tắt

✅ **Khái Niệm `const`**: Khai báo giá trị không đổi tại thời điểm biên dịch.

✅ **Tối ưu Hiệu Suất**: Giúp Dart tái sử dụng đối tượng trong bộ nhớ, giảm tiêu tốn tài nguyên.

---