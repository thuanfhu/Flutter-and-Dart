# 🛠️ How Programming Languages Work?

## 📝 1. Tổng Quan Về Cách Hoạt Động Của Ngôn Ngữ Lập Trình

Ngôn ngữ lập trình, như Dart được sử dụng trong Flutter, hoạt động dựa trên hai loại từ cơ bản: **Keywords** và **Identifiers**. Keywords là các từ được tích hợp sẵn trong ngôn ngữ, mang ý nghĩa rõ ràng và cụ thể, trong khi Identifiers là các tên do lập trình viên định nghĩa để xác định các "đối tượng" trong mã (như biến, hàm, hoặc lớp).

| **Loại**          | **Mô Tả**                                  |
|-------------------|--------------------------------------------|
| Keywords          | Từ tích hợp sẵn, có ý nghĩa cố định        |
| Identifiers       | Tên do lập trình viên định nghĩa           |

---

## ⚙️ 2. Cú Pháp và Cách Sử Dụng

### 2.1. Keywords

Keywords là các từ khóa cố định trong Dart, không thể sử dụng làm tên biến hoặc hàm.

Ví dụ:
```dart
void main() {
  var x = 10; // "void" là keyword
  print(x);   // "print" là keyword
}
```

-> Mô tả: `void`, `var`, và `print` là keywords có ý nghĩa cụ thể trong Dart.

### 2.2. Identifiers

Identifiers được tạo bởi lập trình viên để đặt tên cho biến, hàm, hoặc lớp.

Ví dụ:
```dart
int myVariable = 5; // "myVariable" là identifier
void myFunction() {} // "myFunction" là identifier
```

-> Mô tả: `myVariable` và `myFunction` là identifiers do lập trình viên định nghĩa.

---

## 📌 3. Tóm Tắt

✅ **Keywords**: Từ tích hợp sẵn trong ngôn ngữ, có ý nghĩa rõ ràng và cố định.

✅ **Identifiers**: Tên do lập trình viên tạo, dùng để xác định các đối tượng trong mã.

---