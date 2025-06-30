# 🖌️ Understanding Material Design

## 📝 1. Tổng Quan Về Material Design

Material Design là hệ thống thiết kế linh hoạt do Google phát triển, cung cấp một bộ gợi ý, quy tắc và hướng dẫn để xây dựng các giao diện người dùng đẹp mắt. Hệ thống này được thiết kế để dễ tùy chỉnh và mở rộng, giúp các nhà phát triển tạo ra trải nghiệm đồng nhất trên nhiều nền tảng, đặc biệt khi sử dụng trong Flutter. Material Design lấy cảm hứng từ thế giới thực, sử dụng các nguyên tắc như lớp phủ (layers), bóng đổ (shadows), và chuyển động (motion) để tạo giao diện trực quan.

| **Đặc Điểm**         | **Mô Tả**                           |
|-----------------------|-------------------------------------|
| Linh hoạt            | Dễ dàng tùy chỉnh theo nhu cầu      |
| Mở rộng              | Hỗ trợ mở rộng cho các nền tảng     |
| Hướng dẫn            | Gợi ý và quy tắc để xây dựng UI     |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Sử Dụng Material Design trong Flutter

Flutter tích hợp Material Design thông qua các widget như `MaterialApp`, `Scaffold`, và `AppBar`.

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
        appBar: AppBar(title: const Text('Material Design App')),
        body: const Center(child: Text('Chào mừng đến với Material Design!')),
      ),
    );
  }
}
```

-> Mô tả: Đoạn mã trên sử dụng `MaterialApp` và `Scaffold` để tạo giao diện theo phong cách Material Design.

### 2.2. Tùy Chỉnh Giao Diện

Điều chỉnh thuộc tính như màu sắc và chủ đề để tùy chỉnh.

Ví dụ:
```dart
MaterialApp(
  theme: ThemeData(primarySwatch: Colors.blue),
  home: Scaffold(
    appBar: AppBar(title: const Text('Custom Theme')),
    body: const Center(child: Text('Giao diện tùy chỉnh!')),
  ),
)
```

-> Mô tả: Sử dụng `ThemeData` để áp dụng màu chủ đạo (blue) cho ứng dụng.

---

## 📌 3. Tóm Tắt

✅ **Material Design**: Hệ thống thiết kế linh hoạt của Google với gợi ý, quy tắc, và hướng dẫn.

✅ **Đặc Điểm**: Dễ tùy chỉnh và mở rộng cho giao diện đẹp mắt.

---