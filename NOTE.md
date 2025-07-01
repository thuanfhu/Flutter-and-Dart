# 🛠️ Building More Complex Widget Trees

## 📝 1. Tổng Quan Về Xây Dựng Cây Widget Phức Tạp

Trong Flutter, giao diện người dùng được xây dựng thông qua việc lồng các **widget** để tạo thành một **Widget Tree**. Đoạn mã mẫu sử dụng `MaterialApp`, `Scaffold`, `Center`, và `Text` để xây dựng một giao diện đơn giản. Mỗi widget đóng vai trò cụ thể trong việc tổ chức và hiển thị nội dung. Việc sử dụng dấu phẩy (`,`) sau mỗi dấu đóng ngoặc `)` (ví dụ: `),),),),)`) trong mã cho phép định dạng tự động bằng lệnh "Format Document" trong VSCode (View -> Command Palette... -> Format Document), giúp mã nguồn được sắp xếp gọn gàng theo chuẩn Dart.

| **Widget**         | **Mô Tả**                                  |
|--------------------|--------------------------------------------|
| `MaterialApp`      | Cấu hình ứng dụng theo phong cách Material |
| `Scaffold`         | Cung cấp bố cục màn hình cơ bản            |
| `Center`           | Căn giữa nội dung                          |
| `Text`             | Hiển thị văn bản trên màn hình             |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. `MaterialApp` và `home`

- **`MaterialApp`**: Là widget root cấp cao, được tài liệu Flutter xác định là điểm khởi đầu cho ứng dụng sử dụng Material Design. Nó cung cấp các thuộc tính toàn cục như chủ đề (`theme`), tiêu đề (`title`), và trang chủ (`home`) (xem [flutter.dev/docs/cookbook/design/themes](https://flutter.dev/docs/cookbook/design/themes)).
- **`home`**: Tham số được đặt tên (named parameter), chỉ định widget con làm trang chính của ứng dụng, thường là `Scaffold`.

Ví dụ:
```dart
const MaterialApp(
  home: Scaffold(
    body: Center(
      child: Text("Hello World!"),
    ),
  ),
),
```

-> Mô tả: `MaterialApp` thiết lập ứng dụng với `home` là `Scaffold`, định nghĩa giao diện chính.

### 2.2. `Scaffold` và `body`

- **`Scaffold`**: Theo tài liệu Flutter, đây là widget cung cấp cấu trúc cơ bản cho màn hình, bao gồm các khu vực như `appBar`, `body`, `floatingActionButton`, v.v. (xem [flutter.dev/docs/development/ui/layout](https://flutter.dev/docs/development/ui/layout)). Nó triển khai bố cục Material Design.
- **`body`**: Tham số được đặt tên, chứa widget con làm nội dung chính của màn hình, thường là `Center` hoặc các widget khác.

Ví dụ:
```dart
Scaffold(
  body: Center(
    child: Text("Hello World!"),
  ),
),
```

-> Mô tả: `Scaffold` tổ chức bố cục, `body` chứa `Center` làm nội dung trung tâm.

### 2.3. `Center` và `child`

- **`Center`**: Là một widget bố cục (layout widget) theo tài liệu Flutter, căn giữa widget con của nó (ngang và dọc) trong không gian có sẵn (xem [api.flutter.dev/flutter/widgets/Center-class.html](https://api.flutter.dev/flutter/widgets/Center-class.html)).
- **`child`**: Tham số được đặt tên, chỉ định widget con duy nhất (thường là `Text`) mà `Center` sẽ căn giữa.

Ví dụ:
```dart
Center(
  child: Text("Hello World!"),
),
```

-> Mô tả: `Center` căn giữa `Text`, đảm bảo "Hello World!" nằm ở vị trí trung tâm màn hình.

### 2.4. `Text`

- **`Text`**: Là widget hiển thị văn bản tĩnh, được mô tả trong tài liệu Dart/Flutter là một phần của thư viện `material` hoặc `widgets`, nhận chuỗi văn bản qua constructor `data` (xem [api.flutter.dev/flutter/widgets/Text-class.html](https://api.flutter.dev/flutter/widgets/Text-class.html)). Nó không có tham số con, chỉ hiển thị nội dung được cung cấp.
- Không yêu cầu tham số bổ sung ngoài văn bản.

Ví dụ:
```dart
Text("Hello World!"),
```

-> Mô tả: `Text` hiển thị chuỗi "Hello World!" tại vị trí do `Center` xác định.

---

## 📌 3. Tóm Tắt

✅ **MaterialApp và home**: `MaterialApp` là root widget theo Material Design, `home` định nghĩa trang chính (thường là `Scaffold`).

✅ **Scaffold và body**: `Scaffold` cung cấp bố cục cơ bản, `body` chứa nội dung chính (thường là `Center`).

✅ **Center và child**: `Center` căn giữa nội dung, `child` chỉ định widget con (thường là `Text`).

✅ **Text**: Hiển thị văn bản tĩnh, không có tham số con.

---