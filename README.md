# 🛡️ AI Ethical Guardian

**Bài Capstone Học kỳ II - Lớp 9A6 - Vinschool**

---

## 📋 Giới Thiệu

**AI Ethical Guardian** là một dự án nghiên cứu toàn diện nhằm **đánh giá rủi ro đạo đức và an ninh** của các ứng dụng trí tuệ nhân tạo. Dự án sử dụng các phương pháp khoa học dữ liệu kết hợp với kiến thức pháp lý để cung cấp một framework đánh giá toàn diện về tính tuân thủ và an toàn đạo đức của hệ thống AI.

### 🎯 Mục Tiêu

- ✅ Xây dựng công cụ khảo sát người dùng về nhận thức rủi ro AI
- ✅ Phát triển mô hình dự báo rủi ro dựa trên phân tích hồi quy tuyến tính
- ✅ Kiểm định tuân thủ các tiêu chuẩn bảo vệ dữ liệu (GDPR)
- ✅ Cung cấp gợi ý cải thiện cho các ứng dụng AI

---

## ✨ Tính Năng Chính

### 1️⃣ Khảo Sát Người Dùng (User Survey Module)
- Tích hợp **Google Forms API** để thu thập dữ liệu từ người dùng
- Xử lý phản hồi tự động bằng Python
- Lưu trữ dữ liệu trong định dạng Excel để phân tích
- Tính toán thống kê mô tả về nhận thức rủi ro

### 2️⃣ Mô Hình Dự Báo Rủi ro (Risk Prediction Model)
- Sử dụng **hồi quy tuyến tính** để dự báo mức độ rủi ro
- Phân tích mối quan hệ giữa các yếu tố ảnh hưởng và rủi ro
- Tính toán độ chính xác dự báo thông qua sai số tuyệt đối
- Trực quan hóa kết quả bằng biểu đồ tương tác

### 3️⃣ Kiểm Định Tuân Thủ GDPR (GDPR Compliance Checker)
- Kiểm tra xem ứng dụng AI có tuân thủ các yêu cầu GDPR
- Danh sách kiểm tra (checklist) các tiêu chuẩn bảo vệ dữ liệu
- Báo cáo chi tiết về các lĩnh vực cần cải thiện
- Cung cấp đề xuất khắc phục

---

## 🔧 Công Nghệ Sử Dụng

| Công Nghệ | Mục Đích | Phiên Bản |
|-----------|---------|----------|
| **Python** | Ngôn ngữ lập trình chính | 3.8+ |
| **Streamlit** | Framework xây dựng giao diện web | 1.28.0+ |
| **Pandas** | Xử lý và phân tích dữ liệu | 1.5.0+ |
| **NumPy** | Tính toán số học | 1.24.0+ |
| **Matplotlib/Seaborn** | Trực quan hóa dữ liệu | 3.5.0+ |
| **Excel** | Định dạng lưu trữ dữ liệu | .xlsx |
| **Google Forms API** | Thu thập dữ liệu từ biểu mẫu | v1 |

---

## 📐 Cơ Sở Toán Học

### 1. Mô Hình Hồi Quy Tuyến Tính

**Phương trình hồi quy tuyến tính:**

$$y = mx + b$$

Trong đó:
- **y**: Biến phụ thuộc (mức độ rủi ro dự báo)
- **x**: Biến độc lập (các yếu tố ảnh hưởng)
- **m**: Hệ số dốc (độ thay đổi của y khi x tăng 1 đơn vị)
- **b**: Hằng số cắt trục (giá trị y khi x = 0)

**Ứng dụng:** Mô hình này giúp chúng tôi xác định mối quan hệ tuyến tính giữa các yếu tố như:
- Số lượng dữ liệu cá nhân được xử lý
- Độ nhạy cảm của dữ liệu
- Mức độ bảo mật của hệ thống

### 2. Sai Số Tuyệt Đối

**Công thức sai số tuyệt đối:**

$$\Delta x = |x - a|$$

Trong đó:
- **Δx**: Sai số tuyệt đối
- **x**: Giá trị dự báo (predicted value)
- **a**: Giá trị thực tế (actual value)

**Ứng dụng:** Đánh giá độ chính xác của mô hình dự báo rủi ro bằng cách tính độ lệch giữa dự báo và thực tế. Sai số càng nhỏ, mô hình càng chính xác.

---

## 📦 Hướng Dẫn Cài Đặt

### Yêu Cầu Hệ Thống
- Python 3.8 trở lên
- pip (Python package manager)
- Git

### Các Bước Cài Đặt

**1. Clone repository:**
```bash
git clone https://github.com/khanh027344-byte/AI-Ethical-Guardian.git
cd AI-Ethical-Guardian
```

**2. Tạo môi trường ảo (Virtual Environment):**
```bash
python -m venv venv
```

**3. Kích hoạt môi trường ảo:**

*Windows:*
```bash
venv\Scripts\activate
```

*macOS/Linux:*
```bash
source venv/bin/activate
```

**4. Cài đặt các dependency:**
```bash
pip install -r requirements.txt
```

**5. Chạy ứng dụng Streamlit:**
```bash
streamlit run src/main.py
```

**6. Mở trình duyệt:**
Ứng dụng sẽ tự động mở tại `http://localhost:8501`

---

## 📁 Cấu Trúc Thư Mục

```
AI-Ethical-Guardian/
│
├── 📂 data/                          # Thư mục dữ liệu
│   ├── raw/                          # Dữ liệu thô từ Google Forms
│   ├── processed/                    # Dữ liệu đã xử lý
│   └── survey_responses.xlsx         # File Excel lưu trữ phản hồi
│
├── 📂 models/                        # Thư mục mô hình
│   ├── risk_prediction_model.pkl     # Mô hình hồi quy tuyến tính
│   ├── model_training.py             # Script huấn luyện mô hình
│   └── model_evaluation.py           # Script đánh giá mô hình
│
├── 📂 src/                           # Thư mục code nguồn
│   ├── main.py                       # File chính chạy ứng dụng
│   ├── survey_module.py              # Module khảo sát người dùng
│   ├── risk_predictor.py             # Module dự báo rủi ro
│   ├── gdpr_checker.py               # Module kiểm định GDPR
│   └── utils.py                      # Hàm tiện ích chung
│
├── 📂 tests/                         # Thư mục kiểm thử
│   ├── test_survey.py                # Test khảo sát
│   ├── test_risk_model.py            # Test mô hình dự báo
│   └── test_gdpr_checker.py          # Test GDPR checker
│
├── 📄 requirements.txt               # Danh sách dependency
├── 📄 README.md                      # File hướng dẫn
├── 📄 LICENSE                        # Giấy phép dự án
└── 📄 .gitignore                     # File cấu hình Git

```

---

## 👤 Tác Giả

**Phạm Đình Gia Khánh**
- 🏫 Lớp: 9A6 - Vinschool
- 💻 GitHub: [@khanh027344-byte](https://github.com/khanh027344-byte)
- 📅 Năm học: 2025-2026 (Học kỳ II)
