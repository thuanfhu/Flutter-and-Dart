# 🕵️ Analyzing A New Flutter Project

## 📝 1. Tổng Quan Về Phân Tích Dự Án Flutter Mới

Khi sử dụng lệnh `flutter create <my-app>` để tạo một dự án Flutter mới, một cấu trúc thư mục được tự động sinh ra với các file và thư mục quan trọng hỗ trợ phát triển ứng dụng. Cấu trúc này bao gồm mã nguồn Dart/Flutter, cấu hình, và tài nguyên, được thiết kế để giúp phát triển ứng dụng đa nền tảng.

| **Thành Phần**      | **Mô Tả**                                  |
|----------------------|--------------------------------------------|
| Thư mục `lib`        | Chứa mã nguồn Dart chính                  |
| File `pubspec.yaml`  | Cấu hình phụ thuộc và tài nguyên           |
| Thư mục `android`    | Mã nguồn và cấu hình cho Android           |
| Thư mục `ios`        | Mã nguồn và cấu hình cho iOS               |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Tạo Dự Án và Cấu Trúc Thư mục

Sử dụng lệnh để tạo dự án và khám phá cấu trúc.

Ví dụ:
```sh
flutter create my_app
cd my_app
```

-> Mô tả: Sau lệnh này, thư mục `my_app` sẽ chứa các file và thư mục sau:

- **`android/`**: Chứa mã và cấu hình native cho Android (ví dụ: `AndroidManifest.xml`).

- **`ios/`**: Chứa mã và cấu hình native cho iOS (ví dụ: `Runner.xcodeproj`).

- **`lib/`**: Thư mục chính chứa mã Dart.

- **`test/`**: Chứa mã kiểm tra đơn vị.

- **`web/`**: Chứa tài nguyên cho ứng dụng web.

- **`windows/`, `macos/`, `linux/`**: Chứa cấu hình cho các nền tảng desktop.

- **`.gitignore`**: Xác định file không theo dõi bởi Git.

- **`pubspec.yaml`**: Quản lý phụ thuộc và tài nguyên.

- **`README.md`**: Tài liệu hướng dẫn cơ bản.

### 2.2. Ý Nghĩa Của Các File Dart/Flutter Trong `lib`

- **`lib/main.dart`**:
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
        title: 'Flutter Demo',
        theme: ThemeData(primarySwatch: Colors.blue),
        home: const MyHomePage(title: 'Flutter Demo Home Page'),
      );
    }
  }

  class MyHomePage extends StatefulWidget {
    const MyHomePage({super.key, required this.title});
    final String title;

    @override
    State<MyHomePage> createState() => _MyHomePageState();
  }

  class _MyHomePageState extends State<MyHomePage> {
    int _counter = 0;
    void _incrementCounter() {
      setState(() {
        _counter++;
      });
    }

    @override
    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(title: Text(widget.title)),
        body: Center(child: Text('$_counter')),
        floatingActionButton: FloatingActionButton(
          onPressed: _incrementCounter,
          tooltip: 'Increment',
          child: const Icon(Icons.add),
        ),
      );
    }
  }
  ```
  -> Mô tả: File khởi chạy ứng dụng, định nghĩa `MyApp` (giao diện chính) và `MyHomePage` (trang chủ với nút tăng đếm).

---

## 📌 3. Tóm Tắt

✅ **Cấu Trúc Thư mục**: Bao gồm `lib` (mã Dart), `android`/`ios` (cấu hình native), `pubspec.yaml` (phụ thuộc).

✅ **File Quan Trọng**: `main.dart` (khởi chạy), `pubspec.yaml` (quản lý), `test` (kiểm tra).

---