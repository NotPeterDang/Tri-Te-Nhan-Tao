# 🧠 LAB 02 – ARTIFICIAL INTELLIGENCE  
## 🔬 THỰC HÀNH 06 & 07: Bài toán N-Queens

---

## 🎯 Mục tiêu

- Hiểu và mô tả bài toán **N-Queens** trong Trí tuệ Nhân tạo.
- Cài đặt thuật toán giải bài toán bằng kỹ thuật **quay lui (backtracking)**.
- Sinh tất cả các cấu hình hợp lệ.
- Xác định số lượng lời giải hợp lệ.
- In ra lời giải cùng với vị trí quân hậu trên bàn cờ.

---

## 📌 Nội dung thực hành

### 1. Bài toán 4-Queens (TH06)

- **Mô tả**:  
  Đặt 4 quân hậu lên bàn cờ 4x4 sao cho không có 2 quân hậu nào tấn công lẫn nhau.  
  Quân hậu có thể tấn công theo:
  - Cùng hàng (ngang)
  - Cùng cột (dọc)
  - Đường chéo chính và phụ

- **Yêu cầu**:
  - Sinh tất cả các cấu hình có thể cho 4 quân hậu.
  - Kiểm tra tính hợp lệ của từng cấu hình.
  - In ra các lời giải thỏa mãn và hiển thị theo cả dạng bảng và tọa độ.

- **Kết quả mong đợi**:
  - Số lời giải hợp lệ: `2`
  - In ra lời giải theo vị trí chỉ số và theo tọa độ `(cột, hàng)`  
  - Ví dụ:

    ```
    Lời giải 1: [1, 3, 0, 2]
    Vị trí: [(1, 0), (3, 1), (0, 2), (2, 3)]

    Lời giải 2: [2, 0, 3, 1]
    Vị trí: [(2, 0), (0, 1), (3, 2), (1, 3)]
    ```

---

### 2. Bài toán 8-Queens (TH07)

- **Mô tả**:  
  Mở rộng từ bài toán 4-Queens lên bàn cờ 8x8. Đặt 8 quân hậu sao cho không quân nào tấn công quân khác.

- **Yêu cầu**:
  - Cài đặt thuật toán backtracking để tìm mọi lời giải.
  - In ra tổng số lời giải tìm được.
  - In ra một vài lời giải mẫu minh họa (dưới dạng ma trận bàn cờ và danh sách tọa độ).

- **Kết quả mong đợi**:
  - Tổng số lời giải hợp lệ: `92`
  - Ví dụ lời giải:

    ```
    Lời giải: [0, 4, 7, 5, 2, 6, 1, 3]
    Vị trí: [(0, 0), (4, 1), (7, 2), (5, 3), (2, 4), (6, 5), (1, 6), (3, 7)]
    ```

---

## 🛠 Công nghệ & Kỹ thuật sử dụng

- **Ngôn ngữ**: Python
- **Thư viện**: `numpy`
- **Thuật toán**: Backtracking (Quay lui)

---

## ▶️ Hướng dẫn chạy chương trình

1. Cài đặt Python và thư viện numpy (nếu chưa có):

   ```bash
   pip install numpy
   ```

2. Chạy file Python:

   ```bash
   python queens.py
   ```

3. Nhập số lượng quân hậu (`N = 4` hoặc `N = 8`) khi được yêu cầu.

---

## 📋 Ghi chú

- Bài toán N-Queens là một ví dụ điển hình trong các bài toán tìm kiếm không gian trạng thái.
- Khi `N` tăng, độ phức tạp tăng theo cấp số nhân.
- Giải pháp sử dụng quay lui đảm bảo tìm được tất cả cấu hình hợp lệ.

---
