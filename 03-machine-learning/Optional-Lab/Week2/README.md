
# Machine Learning Specialization - Andrew Ng
## Course 1: Supervised Machine Learning
### Week 2: Regression with Multiple Input Variables

Kho mục này chứa các bài thực hành (Optional Labs) và ghi chú lý thuyết trọng tâm của Tuần 2. Nội dung chính xoay quanh việc mở rộng mô hình Hồi quy tuyến tính cho dữ liệu có nhiều đặc trưng (features) và các kỹ thuật tối ưu hóa đi kèm.

---

## 📂 Danh sách các bài thực hành (Labs)

| Tên File | Mục tiêu & Kiến thức đạt được |
| :--- | :--- |
| `C1_W2_Lab01` | **Python, NumPy & Vectorization**: Học cách sử dụng mảng NumPy để thay thế vòng lặp `for`, giúp code chạy nhanh hơn và gọn hơn. |
| `C1_W2_Lab02` | **Multiple Variable Linear Regression**: Triển khai hàm dự đoán $f_{w,b}(x) = w \cdot x + b$ và Gradient Descent cho nhiều biến. |
| `C1_W2_Lab03` | **Feature Scaling & Learning Rate**: Thực hành chuẩn hóa dữ liệu (Z-score) và quan sát cách chọn $\alpha$ ảnh hưởng đến sự hội tụ. |
| `C1_W2_Lab04` | **Feature Engineering & Polynomial Regression**: Cách biến đổi dữ liệu đầu vào (như $x^2, x^3$) để khớp với các đường cong phức tạp. |
| `C1_W2_Lab05` | **Linear Regression with Scikit-Learn**: Sử dụng thư viện chuẩn công nghiệp để huấn luyện mô hình thay vì viết code thủ công. |

---

## 🧠 Kiến thức cốt lõi cần nhớ

### 1. Vectorization (Vector hóa)
Trong Machine Learning, thay vì tính toán từng phần tử:
- **Cách cũ (Vòng lặp):** `for i in range(n): f += w[i] * x[i]`
- **Cách mới (Vector):** `f = np.dot(w, x) + b`
> **Tại sao?** NumPy sử dụng tính toán song song trong CPU/GPU, giúp tốc độ xử lý nhanh hơn gấp nhiều lần khi làm việc với tập dữ liệu lớn.

### 2. Feature Scaling (Chuẩn hóa đặc trưng)
Khi các đặc trưng có thang đo khác nhau (ví dụ: diện tích 2000 $m^2$ và số phòng ngủ là 3), mặt phẳng chi phí (Cost function) sẽ rất hẹp và dài, khiến Gradient Descent khó đi đến điểm tối ưu.
- **Giải pháp:** Sử dụng **Z-score Normalization** để đưa các biến về cùng một thang đo (thường quanh khoảng -1 đến 1).
- **Công thức:** $x^{(i)}_j = \frac{x^{(i)}_j - \mu_j}{\sigma_j}$

### 3. Feature Engineering & Polynomial Regression
Không phải mọi mối quan hệ đều là đường thẳng.
- **Feature Engineering:** Là quá trình dùng kiến thức thực tế để tạo ra biến mới (ví dụ: có chiều dài và chiều rộng thì tạo ra biến `Diện tích`).
- **Polynomial Regression:** Cho phép ta dùng mô hình tuyến tính để vẽ đường cong bằng cách thêm các bậc cao hơn của biến vào ma trận đầu vào.

### 4. Lựa chọn Learning Rate ($\alpha$)
- Nếu $\alpha$ quá lớn: Hàm Cost sẽ nhảy loạn xạ hoặc tăng dần (overshooting).
- Nếu $\alpha$ quá nhỏ: Quá trình huấn luyện cực kỳ chậm.
- **Mẹo:** Thử các giá trị theo cấp số nhân: $0.001, 0.003, 0.01, 0.03, 0.1, \dots$

---

## 🛠 Công cụ & Thư viện
- **NumPy**: Thư viện toán học nền tảng cho mảng đa chiều.
- **Matplotlib**: Trực quan hóa dữ liệu và biểu đồ hàm chi phí.
- **Scikit-Learn**: Thư viện ML chuyên dụng (sử dụng `SGDRegressor` và `StandardScaler`).

---
**Người thực hiện:** Nguyễn Bảo Duy
**Ngày hoàn thành:** 14 Tháng 4, 2026
