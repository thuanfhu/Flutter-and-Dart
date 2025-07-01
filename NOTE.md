# 🛠️ Positional & Named Arguments

## 📝 1. Tổng Quan Về Tham Số Vị Trí và Tham Số Được Đặt Tên

Trong Dart (ngôn ngữ của Flutter), các hàm có thể sử dụng **tham số vị trí (positional arguments)** hoặc **tham số được đặt tên (named arguments)** để truyền dữ liệu. Tham số vị trí dựa vào thứ tự, trong khi tham số được đặt tên cho phép truyền giá trị theo tên, tăng tính rõ ràng và linh hoạt. Trong Flutter, `MaterialApp` là một ví dụ điển hình sử dụng tham số được đặt tên để cấu hình ứng dụng.

| **Loại Tham Số**    | **Mô Tả**                                  |
|----------------------|--------------------------------------------|
| Positional Arguments | Truyền theo thứ tự cố định                 |
| Named Arguments      | Truyền theo tên, có thể tùy chọn           |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Tham Số Vị Trí

Tham số vị trí yêu cầu giá trị theo thứ tự đã định nghĩa.

Ví dụ:
```dart
void greet(String name, int age) {
  print('Hello $name, you are $age years old!');
}

void main() {
  greet('Alice', 25); // Truyền theo thứ tự: name, age
}
```

-> Mô tả: `Alice` và `25` được truyền theo vị trí cố định.

### 2.2. Tham Số Được Đặt Tên

Tham số có thể được đặt theo tên thay vì thứ tự.

Ví dụ:

```dart
void greet(String name, int age) {
  print('Hello $name, you are $age years old!');
}

void main() {
  greet(age: 30, name: 'Bob', ); // Truyền theo tên
}
```

-> Mô tả: `name` và `age` được truyền theo tên, với giá trị mặc định nếu không cung cấp.

### 2.3. Liên Hệ với `MaterialApp`

`MaterialApp` trong Flutter sử dụng tham số được đặt tên để tùy chỉnh ứng dụng.

Ví dụ:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      title: 'My App', // Tham số được đặt tên
      theme: ThemeData(primarySwatch: Colors.blue), // Tham số được đặt tên
      home: const Scaffold(body: Center(child: Text('Hello!'))), // Tham số được đặt tên
    ),
  );
}
```

-> Mô tả: `title`, `theme`, và `home` là tham số được đặt tên, cho phép cấu hình linh hoạt mà không cần theo thứ tự cố định.

---

## 📌 3. Tóm Tắt

✅ **Positional Arguments**: Truyền giá trị theo thứ tự cố định.

✅ **Named Arguments**: Truyền giá trị theo tên, không quan trọng thứ tự cố định.

✅ **Liên Hệ với MaterialApp**: Sử dụng tham số được đặt tên như `title`, `theme`, `home` để tùy chỉnh ứng dụng.

---