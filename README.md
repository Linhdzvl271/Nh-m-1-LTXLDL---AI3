# Nhóm 1 - Lập Trình Xử Lý Dữ Liệu Lớn & AI

Dự án xử lý dữ liệu và đánh giá mô hình LLM so với phương pháp đối chứng.

## Cấu trúc thư mục
- `configs/`: Chứa file cấu hình tham số cho từng thành phố (`<city>.yaml`).
- `data/`:
  - `raw/`: Dữ liệu thô (không đưa lên Git).
  - `processed/`: Dữ liệu sạch, kết quả KPI.
  - `samples/`: Mẫu nhỏ test nhanh + tệp gán nhãn tay (>= 100 mẫu).
- `src/`: Mã nguồn module hóa (`download.py`, `qa.py`, `kpi.py`, `llm.py`, `baseline.py`, `evaluate.py`, `viz.py`).
- `figures/`: Biểu đồ trực quan hóa sinh ra từ quy trình.
- `reports/`: Báo cáo, `qa_report.csv`, data dictionary.
- `run_pipeline.py`: Script điều phối chạy toàn bộ pipeline.

## Cài đặt môi trường
Phiên bản Python khuyến nghị: tham khảo `.python-version` (Python `3.10.x`).

```bash
# Tạo môi trường ảo
python -m venv .venv
source .venv/bin/activate  # Trên Linux/macOS
# hoặc: .venv\Scripts\activate  # Trên Windows

# Cài đặt thư viện
pip install -r requirements.txt

# Cấu hình biến môi trường
cp .env.example .env
# Điền các API Key vào file .env
```

## Chạy quy trình
```bash
python run_pipeline.py
```
