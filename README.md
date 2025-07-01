<div align="center">

# ✈️ Tối ưu hóa Lịch trình Hồi hương cho Việt Nam ✈️

### _Nghiên cứu điển hình sử dụng Lập trình Nguyên Hỗn hợp (MILP) trong Chiến dịch COVID-19_

</div>

<div align="center">

![Project Status](https://img.shields.io/badge/status-completed-green)
![Language](https://img.shields.io/badge/language-Python-blue)
![Library](https://img.shields.io/badge/library-PuLP-orange)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

</div>

---

> Dự án này giải quyết **Bài toán Lập lịch Hồi hương (RSP)** bằng cách áp dụng mô hình toán học để tìm ra kế hoạch bay tối ưu, giúp đưa công dân Việt Nam về nước một cách hiệu quả và nhân đạo nhất trong bối cảnh khủng hoảng của đại dịch COVID-19.

<p align="center">
  <img src="https://i.pinimg.com/originals/3c/3d/8c/3c3d8c50e9a7e0c5242404f2d7a2b972.gif" alt="Animated Airplane" width="500"/>
</p>

## 🎯 Giới thiệu

Đại dịch COVID-19 đã tạo ra một cuộc khủng hoảng nhân đạo chưa từng có, khiến hàng triệu người bị mắc kẹt ở nước ngoài. Đáp lại, Chính phủ Việt Nam đã khởi động một chiến dịch hồi hương quy mô lớn. Tuy nhiên, với nhu cầu vượt xa khả năng đáp ứng của các chuyến bay và cơ sở cách ly, việc ra quyết định trở nên vô cùng phức tạp.

Dự án này sử dụng **Lập trình Nguyên Hỗn hợp (MILP)** để xây dựng một mô hình toán học, giúp các nhà hoạch định chính sách trả lời câu hỏi: *Làm thế nào để phân bổ nguồn lực hạn chế (máy bay, giường cách ly) nhằm tối đa hóa giá trị nhân đạo, ưu tiên những người dễ bị tổn thương nhất?*

---

## 🛠️ Kiến trúc Kỹ thuật & Công cụ

Mô hình được xây dựng và giải quyết bằng các công cụ mã nguồn mở, theo quy trình sau:

| Bước | Công cụ / Thư viện | Mục đích |
| :--- | :--- | :--- |
| **1. Tải & Xử lý Dữ liệu** | `Python`, `Pandas` | Đọc và cấu trúc dữ liệu từ file Excel. |
| **2. Xây dựng Mô hình** | `PuLP` | Dịch các công thức toán học (hàm mục tiêu, ràng buộc) thành mã Python. |
| **3. Giải bài toán** | `CBC Solver (COIN-OR)` | Tìm giải pháp tối ưu cho mô hình MILP đã xây dựng. |
| **4. Môi trường** | `Google Colab` | Môi trường đám mây để chạy mã nguồn mà không cần cài đặt phức tạp. |

## 📁 Cấu trúc Thư mục

## 🚀 Hướng dẫn Cài đặt & Chạy

Để tái tạo kết quả của dự án, hãy làm theo các bước sau:

1.  **Clone Repository**
    ```bash
    git clone [https://github.com/nauqcreen/optimization.git](https://github.com/nauqcreen/optimization.git)
    cd optimization
    cd repatriation scheduling
    ```

2.  **Cài đặt các thư viện cần thiết**
    ```bash
    pip install pandas pulp
    ```

3.  **Chạy mô hình**
    Mở file `notebooks/Repatriation_MILP_Model.ipynb` bằng Google Colab hoặc Jupyter Notebook và chạy tất cả các ô (cells). Đảm bảo rằng đường dẫn đến file dữ liệu trong `data/` là chính xác.

---

## 📈 Kết quả Nổi bật & Phân tích

Mô hình đã tìm ra một giải pháp tối ưu với các đặc điểm chính sau:

| Chỉ số | Giá trị | Phân tích |
| :--- | :--- | :--- |
| **Tổng điểm ưu tiên** | **22,110** | Điểm "giá trị nhân đạo" tối đa có thể đạt được. |
| **Tổng công dân hồi hương**| **2,211** | Số người được đưa về nước trong một đợt lập kế hoạch. |
| **Sử dụng đội bay** | **8 / 8 (100%)** | Toàn bộ máy bay được huy động và bay đầy tải. |
| **Sử dụng cơ sở cách ly** | **2,211 / 5,000 (44.22%)** | Năng lực cách ly còn dư thừa đáng kể. |

### 💡 Phát hiện Quan trọng nhất: Nút thắt nằm ở đâu?

<div align="center">

> Phân tích cho thấy **năng lực vận tải (số lượng máy bay) là nút thắt cổ chai chính** của hệ thống, không phải năng lực cách ly. Điều này có nghĩa là để hồi hương nhiều người hơn, việc tăng cường đội bay sẽ hiệu quả hơn là mở thêm khu cách ly.

</div>

---

## ⚠️ Hạn chế của Mô hình

1.  **Mô hình tĩnh**: Chỉ xem xét một giai đoạn lập kế hoạch duy nhất, không phản ánh tính chất động, kéo dài của chiến dịch thực tế.
2.  **Dữ liệu ước tính**: Dữ liệu đầu vào được tổng hợp từ các nguồn công khai, không phải dữ liệu vận hành chính thức.
3.  **Đơn giản hóa**: Mô hình bỏ qua các yếu tố phức tạp như chi phí, định tuyến bay, và thủ tục ngoại giao.

## 🧑‍💻 Tác giả

| Tên | Mã số sinh viên | Lớp |
| :--- | :--- | :--- |
| **Quan Manh NGUYEN** | `21070555` | BDA2021B |

---
<div align="center">
Báo cáo thuộc khuôn khổ môn học **INS3048 - Optimization in Quantitative Management** <br>
**Trường Quốc tế - Đại học Quốc gia Hà Nội** <br>
_Tháng 6, 2025_
</div>
