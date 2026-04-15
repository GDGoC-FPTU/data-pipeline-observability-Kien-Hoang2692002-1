[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574196&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** hoatruongquay@gmail.com
**Name:** Hoàng Văn Kiên

---

## Mo ta

Trong bài lab này, tôi xây dựng một ETL Pipeline đơn giản bằng Python để xử lý dữ liệu sản phẩm. Pipeline bao gồm 4 bước chính: Extract (đọc dữ liệu từ file JSON), Validate (lọc dữ liệu không hợp lệ), Transform (chuẩn hóa dữ liệu và áp dụng business logic), và Load (lưu kết quả ra file CSV).

Ngoài ra, tôi thực hiện thêm một thí nghiệm với AI Agent để so sánh ảnh hưởng của dữ liệu sạch (clean data) và dữ liệu lỗi (garbage data) đến kết quả đầu ra. Qua đó, đánh giá tầm quan trọng của chất lượng dữ liệu trong hệ thống AI.
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
Chạy với clean data (processed_data.csv) để kiểm tra kết quả đúng
Chạy với garbage data (garbage_data.csv) để kiểm tra độ sai lệch
```
---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
Validation summary: 3 kept, 2 dropped
Pipeline completed! 3 records saved.