# Intel Image Classification (CNN - Keras)

## Giới thiệu

Dự án này thực hiện bài toán **phân loại ảnh (Image Classification)** trên bộ dữ liệu **Intel Image Classification** bằng các phương pháp học sâu với **Convolutional Neural Network (CNN)** và **Transfer Learning**.

Các phương pháp được triển khai bao gồm:

- Xây dựng một mô hình CNN cơ bản bằng **Keras/TensorFlow**.
- Tiền xử lý và trực quan hóa dữ liệu ảnh.
- Đánh giá hiệu suất mô hình thông qua tập kiểm tra.
- Phân tích lỗi để tìm hiểu các trường hợp mô hình dự đoán sai.
- Sử dụng mô hình **VGG16 được huấn luyện trước trên ImageNet** để trích xuất đặc trưng (feature extraction).
- Huấn luyện mạng nơ-ron trên các đặc trưng được trích xuất từ VGG16.
- Trực quan hóa không gian đặc trưng bằng **PCA**.
- Fine-tuning VGG16 để cải thiện khả năng phân loại.

Bộ dữ liệu bao gồm 6 nhóm cảnh quan:

- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

---

## Results

Các mô hình được đánh giá dựa trên độ chính xác (accuracy) trên tập kiểm tra.

Kết quả quan sát:

- Mô hình CNN cơ bản có khả năng học được các đặc trưng quan trọng từ ảnh.
- Các lớp **Forest** được nhận diện với độ chính xác cao.
- Một số lớp có đặc điểm hình ảnh tương đồng gây khó khăn cho mô hình:
  - Glacier và Mountain.
  - Building và Street.
  - Sea và Glacier.

Việc sử dụng **VGG16 pretrained on ImageNet** giúp mô hình tận dụng các đặc trưng đã được học từ tập dữ liệu lớn, từ đó cải thiện khả năng phân loại so với việc huấn luyện CNN từ đầu.

---

## Images

Một số hình ảnh minh họa trong quá trình thực hiện:

- Phân bố dữ liệu trong các lớp.
- Các ảnh mẫu từ bộ dữ liệu.
- Kết quả trực quan hóa đặc trưng bằng PCA.
- Ma trận nhầm lẫn (Confusion Matrix).
- Ví dụ các dự đoán đúng và sai của mô hình.

---

## Cài đặt

Clone repository:

bash:
git clone https://github.com/nguyenhoanghuy34/cnn-intel-image-classification.git
cd intel-image-classification-cnn

pip install -r requirements.txt

Các thư viện chính được sử dụng:

Python
TensorFlow / Keras
NumPy
OpenCV
Scikit-learn
Matplotlib
Seaborn

Chạy notebook:

jupyter notebook

Sau đó mở file notebook để thực hiện quá trình huấn luyện và đánh giá mô hình.
