# Hướng dẫn sử dụng dự án

## Cấu trúc thư mục

```
.
├── datathon.ipynb              # Notebook phân tích chính
├── Phan1_MCQ-.ipynb            # Notebook phân tích MCQ
├── README.md                    # Tệp hướng dẫn này
├── requirements.txt             # Danh sách thư viện cần cài đặt
├── submission.csv               # Tệp kết quả dự tính cuối cùng
├── neurips_2025.sty             # File định dạng LaTeX
├── neurips_2025.tex             # File LaTeX báo cáo
├── Đề thi Vòng 1.pdf            # Yêu cầu cuộc thi
├── Dataset/                     # Thư mục chứa dữ liệu
│   ├── customers.csv
│   ├── geography.csv
│   ├── inventory.csv
│   ├── order_items.csv
│   ├── orders.csv
│   ├── payments.csv
│   ├── products.csv
│   ├── promotions.csv
│   ├── returns.csv
│   ├── reviews.csv
│   ├── sales.csv
│   ├── sample_submission.csv
│   ├── shipments.csv
│   └── web_traffic.csv
└── Figures/                     # Thư mục lưu hình ảnh và biểu đồ
```

## Hướng dẫn cài đặt và chạy

### 1. Tạo môi trường ảo

Sử dụng `venv`:

```bash
python -m venv .venv
```

### 2. Kích hoạt môi trường ảo

- Trên Windows (PowerShell):

```powershell
.\.venv\Scripts\Activate.ps1
```

- Trên Windows (Command Prompt):

```cmd
.venv\Scripts\activate
```

- Trên macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Cài đặt các thư viện cần thiết

```bash
pip install -r requirements.txt
```

Điều này sẽ cài đặt tất cả các thư viện cần thiết bao gồm: pandas, scikit-learn, lightgbm, shap, plotly, matplotlib, v.v.

### 4. Chạy Notebook

Mở Jupyter Notebook:

```bash
jupyter notebook
```

#### Bước 1: Chạy notebook phân tích chính

- Mở `datathon.ipynb` trong trình duyệt.
- Chạy tất cả các ô: `Cell` -> `Run All` hoặc `Ctrl+Shift+Enter`

Notebook này sẽ:
- Tải dữ liệu từ thư mục `Dataset/`
- Thực hiện phân tích khám phá
- Tiền xử lý và tạo đặc trưng
- Huấn luyện các mô hình LightGBM
- Tạo các hình ảnh và biểu đồ, lưu vào thư mục `Figures/`

#### Bước 2: Chạy notebook phân tích MCQ

- Mở `Phan1_MCQ-.ipynb` trong trình duyệt.
- Chạy tất cả các ô: `Cell` -> `Run All` hoặc `Ctrl+Shift+Enter`

Notebook này sẽ:
- Phân tích các câu hỏi trắc nghiệm
- Trích xuất và xác minh câu trả lời

## Ghi chú

- Các notebook được thiết kế để chạy tuần tự
- Tất cả các tệp dữ liệu phải nằm trong thư mục `Dataset/`
- Các hình ảnh và biểu đồ sẽ được lưu vào thư mục `Figures/`
- Kết quả dự đoán cuối cùng được lưu trong tệp `submission.csv`

## Khắc phục sự cố

- Nếu gặp lỗi thiếu thư viện, chạy lại: `pip install -r requirements.txt`
- Đảm bảo thư mục `Dataset/` chứa tất cả các tệp CSV cần thiết
- Nếu cần xóa kernel: `jupyter kernelspec list` và `jupyter kernelspec remove <kernel_name>`
- Để xóa cache Python: Xóa thư mục `__pycache__` hoặc tệp `.pyc`
