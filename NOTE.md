# 🛠️ Building User Interfaces with Flutter Widgets

## 📝 1. Tổng Quan Về Xây Dựng Giao Diện Người Dùng với Widget trong Flutter

Trong Flutter, giao diện người dùng (UI) được xây dựng hoàn toàn bằng mã, sử dụng sự kết hợp của các **widget**, được tổ chức thành một cấu trúc gọi là **Widget Tree**. Widget là các khối xây dựng cơ bản, bao gồm các widget tích hợp sẵn (built-in) như `Center` và `Text`, có thể lồng nhau (nested) để tạo giao diện phức tạp. Flutter sử dụng ngôn ngữ Dart, với các hàm như `main()` và `runApp()` để khởi chạy ứng dụng, truyền widget tree để hiển thị UI. Quá trình này được hỗ trợ bởi các widget như `MaterialApp`, `Scaffold`, và `Row`, cùng với khả năng tùy chỉnh thông qua các hàm và tham số.

| **Khái Niệm**       | **Mô Tả**                                  |
|---------------------|--------------------------------------------|
| Widget              | Khối xây dựng giao diện                    |
| Widget Tree         | Cấu trúc lồng nhau của widget              |
| Hàm và Tham số      | Định nghĩa hành vi và đầu vào của hàm      |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Khởi Chạy Ứng Dụng với `main()` và `runApp()`

Ứng dụng Flutter được kích hoạt tự động bởi hàm `main()`, gọi `runApp()` để hiển thị widget tree.

Ví dụ:
```dart
void main() {
  runApp(const MyApp()); // Gọi runApp() bên trong main()
}
```

-> Mô tả: `main()` được thực thi tự động, `runApp()` truyền widget tree để hiển thị UI.

### 2.2. Xây Dựng Widget Tree với Lồng Nhau

Widget được lồng vào nhau để tạo giao diện, ví dụ `Center` chứa `Text`.

Ví dụ:
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    const Center(
      child: Text('Hello World'), // Widget lồng nhau
    ),
  );
}
```

-> Mô tả: `Center` căn giữa nội dung (ngang và dọc), `Text` hiển thị văn bản trên màn hình.

### 2.3. Sử Dụng Hàm và Tham Số

Hàm trong Dart có thể nhận không, một, hoặc nhiều tham số (parameters/arguments).

Ví dụ:
```dart
void main() {} // Không tham số
void printText(String text) {} // Một tham số
void add(int a, int b) {} // Hai tham số, cách nhau bằng dấu phẩy
```

-> Mô tả: Tham số được định nghĩa trong hàm, hỗ trợ nhiều giá trị tùy theo nhu cầu.

### 2.4. Cấu Trúc Widget Tree Nâng Cao

Sử dụng các widget như `MaterialApp`, `Scaffold`, và `Row` để tạo giao diện phức tạp.

Ví dụ:
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MaterialApp(
    home: Scaffold(
      body: Row(
        children: const [
          Text('Text 1'),
          Text('Text 2'),
          Text('Text 3'),
        ],
      ),
    ),
  ));
}
```

-> Mô tả: `MaterialApp` là root widget, `Scaffold` thêm bố cục màn hình, `Row` hiển thị các widget con liền kề.

### 2.5. Tùy Chỉnh và Tạo Widget Riêng

Flutter cung cấp nhiều widget tích hợp và cho phép tạo widget tùy chỉnh.

Ví dụ:
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MaterialApp(
    home: Scaffold(
      body: OutlinedButton(
        onPressed: () {},
        child: Text('Start Quiz'),
      ),
    ),
  ));
}
```

-> Mô tả: `OutlinedButton` và `Text` là widget tích hợp, có thể kết hợp để tạo giao diện độc đáo.

---

## 📌 4. Tóm Tắt

✅ **Xây Dựng UI**: Dùng mã để tạo giao diện với sự kết hợp của widget trong Flutter.

✅ **Widget Tree**: Cấu trúc lồng nhau (nested) của widget, bắt đầu từ `runApp()`.

✅ **Hàm và Tham Số**: Hàm như `main()` và `runApp()` nhận tham số để định nghĩa hành vi.

✅ **Cấu Trúc Nâng Cao**: Sử dụng `MaterialApp`, `Scaffold`, `Row` để tổ chức giao diện.

✅ **Tùy Chỉnh Widget**: Dùng widget tích hợp (như `Center`, `Text`, `OutlinedButton`) và tạo widget riêng.

---