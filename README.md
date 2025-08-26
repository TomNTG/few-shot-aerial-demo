# few-shot-aerial-demo

## Cấu trúc dự án

few-shot-aerial-demo/
│
├─ data/
│ ├─ train/ # ảnh train
│ ├─ test/ # ảnh test
│ └─ labels/ # file TXT nhãn tương ứng
├─ demo.ipynb
├─ REPORT.md # báo cáo kỹ thuật
└─ README.md # file mô tả repo này

## Hướng dẫn chạy

1. Cài đặt dependencies:

Mở demo.ipynb bằng Jupyter Notebook hoặc Google Colab

Cập nhật đường dẫn data/train, data/test, data/labels

Chạy toàn bộ notebook:

Huấn luyện model few-shot trên 10 ảnh

Chạy inference và hiển thị kết quả
