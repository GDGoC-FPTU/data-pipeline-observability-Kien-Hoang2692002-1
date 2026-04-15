# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-00077
**Name:** Hoàng Văn Kiên
**Date:** 15/4/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) |  Based on my data, the best choice is Laptop at $1200. | 9 | Data hợp lệ, giá hợp lý |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 2 | Outlier, dữ liệu sai lệch |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Agent trả lời sai khi sử dụng Garbage Data vì dữ liệu đầu vào chứa nhiều vấn đề nghiêm trọng. Thứ nhất là outliers (giá trị bất thường), ví dụ như “Nuclear Reactor” với giá cực cao không thực tế, khiến model ưu tiên lựa chọn sai. Thứ hai là duplicate IDs, có thể gây nhầm lẫn hoặc ghi đè dữ liệu. Ngoài ra, wrong data types (kiểu dữ liệu sai, ví dụ giá là string thay vì số) làm cho việc xử lý và so sánh bị lỗi. Các null values hoặc category rỗng cũng làm mất thông tin quan trọng. Những lỗi này khiến Agent học từ dữ liệu sai, dẫn đến quyết định không chính xác.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Đống ý. Dữ liệu chất lượng cao quan trọng hơn prompt vì AI chỉ có thể đưa ra kết quả tốt nếu dữ liệu đầu vào chính xác và đáng tin cậy. Một prompt tốt không thể cứu được dữ liệu sai, nhưng dữ liệu tốt có thể giúp Agent hoạt động hiệu quả ngay cả với prompt đơn giản.
