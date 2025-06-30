# 🛠️ What Is Flutter?

## 📝 1. Tổng Quan Về Flutter

Flutter là một công nghệ phát triển ứng dụng đa nền tảng do Google phát triển, kết hợp giữa một **UI Framework** và một **bộ sưu tập công cụ** để xây dựng các ứng dụng chất lượng cao. UI Framework cung cấp các gói mã và hàm tiện ích để viết mã ứng dụng đa nền tảng, trong khi bộ sưu tập công cụ bao gồm CLI và phần mềm hỗ trợ phát triển, thử nghiệm và xây dựng ứng dụng. Flutter cho phép phát triển ứng dụng trên nhiều nền tảng (iOS, Android, web, và desktop) từ một mã nguồn duy nhất sử dụng một ngôn ngữ lập trình.

| **Thành Phần**  | **Mô Tả**                                      |
|-----------------|------------------------------------------------|
| UI Framework    | Cung cấp gói mã và hàm tiện ích cho ứng dụng   |
| Bộ Công Cụ      | Hỗ trợ CLI, phát triển, thử nghiệm và xây dựng |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. UI Framework

Flutter sử dụng ngôn ngữ lập trình **Dart** để xây dựng giao diện người dùng. UI Framework bao gồm các widget có thể tái sử dụng, cho phép phát triển giao diện đồng nhất trên nhiều nền tảng.

Ví dụ:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Flutter App')),
        body: const Center(child: Text('Hello, Flutter!')),
      ),
    );
  }
}
```

-> Mô tả: Đoạn mã trên tạo một ứng dụng Flutter cơ bản với thanh ứng dụng và văn bản trung tâm.

### 2.2. Bộ Sưu Tập Công Cụ

Flutter cung cấp công cụ dòng lệnh (`flutter`) để khởi tạo dự án, thêm gói, và xây dựng ứng dụng.

Ví dụ:
```sh
flutter create my_flutter_app
cd my_flutter_app
flutter run
```

-> Mô tả: Tạo một dự án mới và chạy ứng dụng trên thiết bị mô phỏng hoặc thiết bị thực.

---

## 💡 3. Use Case Thực Tế

- **Phát triển ứng dụng đa nền tảng**: Xây dựng ứng dụng cho cả iOS và Android từ một mã nguồn duy nhất, ví dụ: ứng dụng thương mại điện tử.

  ```dart
  // Widget cho sản phẩm trên cả iOS và Android
  class ProductWidget extends StatelessWidget {
    const ProductWidget({super.key});
    @override
    Widget build(BuildContext context) {
      return Card(child: Text('Sản phẩm'));
    }
  }
  ```

- **Thử nghiệm và triển khai**: Sử dụng `flutter test` để chạy các bài kiểm tra đơn vị và `flutter build` để tạo bản phát hành cho nhiều nền tảng.

- **Ứng dụng web và desktop**: Mở rộng ứng dụng di động sang web hoặc desktop mà không cần viết lại mã.

---

## 📌 4. Tóm Tắt

✅ **UI Framework**: Cung cấp gói mã và hàm tiện ích để viết mã ứng dụng đa nền tảng.

✅ **Bộ Công Cụ**: Hỗ trợ CLI, phát triển, thử nghiệm và xây dựng ứng dụng.

✅ **Lợi Ích**: Phát triển ứng dụng đa nền tảng từ một mã nguồn duy nhất bằng Dart.

✅ **Use Case**: Ứng dụng thương mại điện tử, thử nghiệm đa nền tảng, mở rộng web/desktop.

---