# DeepFake Detection:
## Mô tả 
Dự án này áp dụng mô hình deep learning để xác định tính xác thực của video, phân biệt giữa nội dung thật và deepfake. Quá trình thực hiện bao gồm các bước xử lý dữ liệu video, nhận diện và trích xuất khuôn mặt, huấn luyện mô hình, thực hiện dự đoán và đánh giá hiệu suất hệ thống.## Cấu trúc thư mục
- best_model.pth       # Trọng số của mô hình đã huấn luyện
- detect_from_video.py # Trích xuất khuôn mặt từ video
- load_data.py         # Load dữ liệu cho huấn luyện
- model.py             # Định nghĩa mô hình deep learning
- predict.py           # Dự đoán trên ảnh hoặc video
- train.py             # Huấn luyện và đánh giá mô hình
## Cài đặt
Yêu cầu Python >= 3.8 và các thư viện cần thiết:
#### pip install torch torchvision timm facenet-pytorch opencv-python tqdm numpy pillow matplotlib scikit-learn
## Sử dụng
### 1. Trích xuất khuôn mặt từ video
python detect_from_video.py --video_path input.mp4 --output_folder extracted_faces
### 2. Huấn luyện mô hình
python train.py --epochs 20 --lr 0.001 --device cuda
### 3. Dự đoán trên video
python predict.py --video_path test_video.mp4 --model_path best_model.pth
### Mô hình sử dụng
Mô hình được sử dụng là Xception, tải sẵn trọng số ImageNet và tinh chỉnh trên tập dữ liệu deepfake.
### Liên hệ
Nếu có thắc mắc hoặc cần hỗ trợ, vui lòng liên hệ qua email: hungdovan838@gmail.com
### Kết quả huấn luyện
Biểu đồ dưới đây thể hiện quá trình huấn luyện mô hình:
![image](https://github.com/user-attachments/assets/d4a8d8a1-518a-43c9-b6b0-21d27e80e6ae)
