# 📈 Week 1: Introduction to Machine Learning & Linear Regression

Chào mừng bạn đến với kho lưu trữ bài học tuần 1. Trong tuần này, mình đã tìm hiểu về những khái niệm cơ bản nhất của Machine Learning và cách xây dựng mô hình hồi quy đầu tiên.

## 📝 Kiến thức trọng tâm

### 1. Machine Learning là gì?
- **Supervised Learning (Học có giám sát):** Học từ dữ liệu đã được gán nhãn (Labeled data). Ví dụ: Dự đoán giá nhà dựa trên diện tích.
- **Unsupervised Learning (Học không giám sát):** Tìm cấu trúc hoặc khuôn mẫu ẩn trong dữ liệu không nhãn.

### 2. Linear Regression with One Variable (Hồi quy tuyến tính đơn biến)
Mô hình dự đoán giá trị đầu ra dựa trên một tính năng đầu vào đơn lẻ.
- **Model Function:** $$f_{w,b}(x) = wx + b$$
  *(Trong đó $w$ là trọng số/weight, $b$ là sai số/bias)*

### 3. Cost Function (Hàm chi phí)
Sử dụng **Squared Error Cost Function** để đo lường độ sai lệch giữa dự đoán và thực tế:
$$J(w,b) = \frac{1}{2m} \sum_{i=1}^{m} (f_{w,b}(x^{(i)}) - y^{(i)})^2$$

### 4. Gradient Descent
Thuật toán tối ưu hóa để tìm $w$ và $b$ sao cho hàm chi phí $J$ đạt giá trị nhỏ nhất:
- Cập nhật đồng thời (Simultaneous update):
  $$w = w - \alpha \frac{\partial}{\partial w} J(w,b)$$
  $$b = b - \alpha \frac{\partial}{\partial b} J(w,b)$$
- **Learning Rate ($\alpha$):** Tốc độ học. Nếu quá lớn sẽ gây phân kỳ, nếu quá nhỏ sẽ chạy rất chậm.

---

## 💻 Lab thực hành
Trong thư mục này bao gồm các file Notebook:
- `Model_Representation.ipynb`: Cách biểu diễn mô hình tuyến tính trên đồ thị.
- `Cost_Function.ipynb`: Trực quan hóa cách hàm chi phí thay đổi theo các thông số.
- `Gradient_Descent.ipynb`: Triển khai thuật toán tối ưu hóa từ con số 0 bằng NumPy.

## 🛠 Công cụ sử dụng
- **Python**: Ngôn ngữ chính.
- **NumPy**: Thư viện tính toán vector hóa.
- **Matplotlib**: Vẽ đồ thị trực quan hóa dữ liệu và hàm dự đoán.
