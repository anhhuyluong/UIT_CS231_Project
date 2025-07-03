# 📘 Nhận diện xe ô tô trong ảnh sử dụng kĩ thuật HOG và mô hình học máy

## 🧠 Giới thiệu

* **Tên môn học**: Nhập môn Thị giác máy tính - Computer Vision
* **Mã môn học**: CS231 - **Lớp**: CS231.P11
* **Năm học**: Học kì 1 - Năm học: 2024 - 2025
* **Giảng viên**: TS. Mai Tiến Dũng
* **Mục tiêu đồ án**: Đồ án nhằm xây dựng một hệ thống phát hiện xe trong ảnh bằng cách
  * Trích xuất đặc trưng với kĩ thuật HOG (Histogram of Oriented Gradients)
  * Huấn luyện hai mô hình máy học là KNN và SVM
  * Tham khảo và áp dụng kĩ thuật Sliding Window để phát hiện xe trong một ảnh toàn cục

## 📂 Cấu trúc thư mục

| Tên file                             | Mô tả                                                                 |
|-------------------------------------|----------------------------------------------------------------------|
| 22520550_22520967_SourceCode.ipynb | Notebook chính thực hiện toàn bộ pipeline phát hiện xe trong ảnh |
| 22520550_22520967_Report.pdf | File báo cáo mô tả chi tiết quá trình thực hiện |

## Thành viên nhóm: 
| STT    | MSSV          | Họ và Tên              |Vai trò    | Email                   |
| ------ |:-------------:| ----------------------:|----------:|-------------------------:
| 1      |22520550|Lương Anh Huy|Trưởng nhóm| 22520550@gm.uit.edu.vn|
| 2      |22520967|Hồng Khải Nguyên|Thành viên| 22520967@gm.uit.edu.vn|


## 🛠️ Công nghệ và thư viện
Python 3.x | CV2 | Glob | Matplotlib | Skimage | Scikit-learn | Scipy | Numpy

## Các bước hoạt động
1. Import thư viện và load dữ liệu gồm các ảnh chứa xe và không chứa xe
2. Tiền xử lý và trực quan hóa dữ liệu:
  * Tạo hàm hiển thị ảnh mẫu từ dữ liệu
  * Trực quan hóa đặc trưng HOG từ ảnh mẫu
3. Trích xuất đặc trưng HOG
  * Viết hàm trích xuất đặc trưng HOG
  * Trích xuất toàn bộ đặc trưng từ bộ dữ liệu
4. Huấn luyện mô hình
  * Chia dữ liệu thành train/test
  * Huấn luyện mô hình KNN, SVM và đánh giá mô hình bằng độ chính xác
5. Phát hiện xe với kĩ thuật Sliding Window
  * Áp dụng kĩ thuật Sliding window ở 3 tỷ lệ khác nhau
  * Kết hợp với mô hình SVM để phát hiện xe trên ảnh mới


## 📊 Kết quả So sánh Mô hình
  
| Mô hình                     | Accuracy | Precision | Recall | 
|----------------------------|----------|-----------|--------|
| KNN + Histogram of Gradients (HOG) `k=5` | 0.9805 | 1.0 | 0.9601 | 
| SVM + Histogram of Gradients (HOG) | 0.9898 | 0.9898 | 0.9898 | 
