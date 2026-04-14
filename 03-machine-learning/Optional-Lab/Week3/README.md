# Machine Learning Specialization - Andrew Ng
## Course 1: Supervised Machine Learning
### Week 3: Classification & Regularization

Kho mục này chứa các bài thực hành và kiến thức trọng tâm của Tuần 3. Trọng tâm của tuần này là chuyển từ dự đoán giá trị liên tục (Regression) sang dự đoán phân loại (Classification) và cách xử lý vấn đề Overfitting.

---

## 📂 Danh sách các bài thực hành (Labs)

| Tên File | Mục tiêu & Kiến thức đạt được |
| :--- | :--- |
| `C1_W3_Lab01` | **Classification**: Phân biệt giữa Hồi quy và Phân loại. Hiểu tại sao Hồi quy tuyến tính không phù hợp cho bài toán phân loại. |
| `C1_W3_Lab02` | **Sigmoid Function**: Tìm hiểu hàm Sigmoid - trái tim của Logistic Regression giúp chuyển đổi đầu ra thành xác suất từ 0 đến 1. |
| `C1_W3_Lab03` | **Decision Boundary**: Trực quan hóa đường biên quyết định (tuyến tính và phi tuyến) giúp phân tách các lớp dữ liệu. |
| `C1_W3_Lab04` | **Logistic Loss**: Tại sao không dùng Squared Error cho phân loại? Tìm hiểu hàm Loss "lồi" (convex) cho Logistic Regression. |
| `C1_W3_Lab05` | **Cost Function for Logistic Regression**: Triển khai hàm chi phí tổng quát trên toàn bộ tập dữ liệu huấn luyện. |
| `C1_W3_Lab06` | **Gradient Descent for Logistic Regression**: Cập nhật các tham số $w$ và $b$ để tối ưu hóa hàm chi phí cho bài toán phân loại. |
| `C1_W3_Lab07` | **Logistic Regression with Scikit-Learn**: Sử dụng thư viện chuyên nghiệp để huấn luyện mô hình phân loại nhanh chóng. |
| `C1_W3_Lab08` | **Overfitting**: Tìm hiểu về hiện tượng Underfitting (High Bias) và Overfitting (High Variance). |
| `C1_W3_Lab09` | **Regularization**: Sử dụng kỹ thuật chính quy hóa để giảm Overfitting cho cả mô hình Linear và Logistic Regression. |

---

## 🧠 Kiến thức cốt lõi cần nhớ

### 1. Hàm Sigmoid (Logistic Function)
Công thức: $g(z) = \frac{1}{1 + e^{-z}}$
- Khi $z$ lớn, $g(z) \approx 1$.
- Khi $z$ nhỏ, $g(z) \approx 0$.
- Mô hình Logistic Regression: $f_{w,b}(x) = g(w \cdot x + b)$.

### 2. Decision Boundary (Đường biên quyết định)
- Là đường phân chia nơi mô hình dự đoán lớp 1 và lớp 0.
- Dự đoán $y=1$ khi $f_{w,b}(x) \geq 0.5$ (tương đương $w \cdot x + b \geq 0$).

### 3. Vấn đề Overfitting (Quá khớp)
- **Underfitting (High Bias):** Mô hình quá đơn giản, không khớp tốt cả trên tập huấn luyện.
- **Overfitting (High Variance):** Mô hình quá phức tạp, khớp cực tốt trên tập huấn luyện nhưng không dự đoán tốt trên dữ liệu mới.
- **Giải pháp:**
    - Thu thập thêm dữ liệu.
    - Giảm bớt số lượng đặc trưng (Features).
    - **Regularization (Chính quy hóa):** Giữ lại các đặc trưng nhưng làm giảm độ lớn của các tham số $w_j$.

### 4. Regularization (Chính quy hóa)
- Thêm một tham số phạt (penalty) vào hàm Cost: $\frac{\lambda}{2m} \sum w_j^2$.
- **$\lambda$ (Lambda):** Điều khiển mức độ chính quy hóa. 
    - $\lambda$ quá lớn: Mô hình bị Underfit.
    - $\lambda$ quá nhỏ: Mô hình vẫn bị Overfit.

---

## 🛠 Công cụ sử dụng
- **NumPy & Matplotlib**: Tính toán ma trận và vẽ đồ thị Decision Boundary.
- **Scikit-Learn**: Sử dụng `LogisticRegression` để giải quyết bài toán phân loại nhanh chóng và hiệu quả.

---
**Người thực hiện:** Nguyễn Bảo Duy
**Ngày hoàn thành:** Tháng 4, 2026
