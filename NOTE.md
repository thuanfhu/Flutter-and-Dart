# 🛠️ One Codebase, Multiple Platforms

## 📝 1. Tổng Quan Về One Codebase, Multiple Platforms

Flutter cho phép phát triển ứng dụng trên nhiều nền tảng (Mobile Apps, Web, Desktop Apps) từ một mã nguồn duy nhất bằng ngôn ngữ Dart. Ban đầu, Flutter chỉ hỗ trợ ứng dụng di động (iOS và Android), nhưng nay đã mở rộng sang web (trên trình duyệt hiện đại) và desktop (Windows, macOS, Linux). Mặc dù mã nguồn có thể được viết trên cùng một máy, việc thử nghiệm và chạy ứng dụng yêu cầu máy tính tương thích với nền tảng cụ thể (macOS cho iOS/macOS, Windows cho Windows, Linux cho Linux), ngoại trừ Android và web có thể được xây dựng trên tất cả các hệ điều hành.

| **Danh Mục**    | **Nền Tảng**           |
|------------------|-------------------------|
| Mobile Apps      | iOS, Android            |
| Web              | Modern browsers         |
| Desktop Apps     | Windows, macOS, Linux   |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Viết Mã Cho Nhiều Nền Tảng

Flutter sử dụng một mã nguồn duy nhất để nhắm mục tiêu nhiều nền tảng. Các widget và cấu hình có thể được điều chỉnh theo nền tảng.

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
        appBar: AppBar(title: const Text('Cross-Platform App')),
        body: const Center(child: Text('Chạy trên iOS, Android, Web, Desktop')),
      ),
    );
  }
}
```

-> Mô tả: Ứng dụng trên có thể chạy trên iOS, Android, web, và desktop với cùng mã nguồn.

### 2.2. Xây Dựng và Chạy Ứng Dụng

Sử dụng lệnh `flutter` để xây dựng và chạy ứng dụng trên các nền tảng.

Ví dụ:
```sh
# Xây dựng cho Android
flutter build apk

# Xây dựng cho web
flutter build web

# Chạy trên macOS
flutter run -d macos
```

-> Mô tả: Các lệnh trên xây dựng ứng dụng cho các nền tảng khác nhau. Lưu ý rằng iOS/macOS chỉ chạy trên máy macOS, Windows trên máy Windows, và Linux trên máy Linux.

--- 

## 📌 3. Tóm Tắt

✅ **One Codebase**: Viết mã nguồn duy nhất cho Mobile (iOS, Android), Web (trình duyệt hiện đại), và Desktop (Windows, macOS, Linux).

✅ **Yêu Cầu Hệ Thống**: iOS/macOS cần máy macOS, Windows cần máy Windows, Linux cần máy Linux; Android và web có thể xây dựng trên mọi hệ điều hành.

✅ **Use Case**: Ứng dụng thương mại điện tử, công cụ desktop nội bộ, kiểm thử đa nền tảng.

---