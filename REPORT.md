## 1. Dataset
- Dataset: **DOTA-mini** (subset của DOTA)
- Số ảnh train: 10
- Số ảnh test: 1
- Nhãn: file TXT chứa oriented bounding box, đã chuyển sang **axis-aligned bounding box** để dùng với Faster R-CNN

## 2. Mô hình
- Sử dụng **Faster R-CNN ResNet-50 FPN** pretrained từ torchvision
- Fine-tune trên 10 ảnh train (few-shot)

## 3. Huấn luyện
- Batch size: 1
- Epoch: 2
- Optimizer: SGD, lr=0.005, momentum=0.9, weight_decay=0.0005
- Thiết bị: GPU/CPU
- Quá trình Loss (mẫu):
Epoch 1, Loss: 0.8972
Epoch 2, Loss: 0.4313

## 4. Inference
- Model đánh giá trên ảnh test
- Vẽ bounding box dự đoán trên ảnh

## 5. Nhận xét
- Dù chỉ với 10 ảnh, model vẫn phát hiện xe khá tốt
- Demo few-shot cho thấy model học được localization bounding box nhanh chóng

## 6. Kết luận
- Few-shot object detection khả thi với pretrained Faster R-CNN
- Phù hợp với ảnh từ trên cao, nơi việc gán nhãn tốn nhiều công sức
- Dữ liệu nhãn dạng oriented bbox có thể chuyển sang axis-aligned bbox để dùng với detector chuẩn