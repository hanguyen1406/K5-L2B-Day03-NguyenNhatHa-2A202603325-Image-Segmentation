# Báo cáo thực hành Day 3

- Mã học viên theo lớp: `2A202603325`
- Ngày / CVAT local: `12/11/2026`
- Công cụ đã dùng: CVAT thủ công, tool chạy model Yolo, SegFormer

## 1. Bài đã nộp

Đã kiểm tra cấu trúc và class của các ZIP bằng `scripts/inspect_submissions.py`. Cả 9 ZIP hiện đều đúng tên, đúng format và đúng schema class.

| Task | File ZIP đúng tên | Hoàn thành mấy ảnh | Điểm tối đa |
| --- | --- | ---: | ---: |
| easy_semantic | `easy_semantic.zip` | 3 / 3 | 20 |
| medium_instance | `medium_instance.zip` | 3 / 3 | 32 |
| hard_panoptic | `hard_panoptic.zip` | 2 / 2 | 30 |
| cp1_holes | `cp1_holes.zip` | 1 / 1 | 3 |
| cp2_slice | `cp2_slice.zip` | 1 / 1 | 3 |
| cp5_occlusion | `cp5_occlusion.zip` | 1 / 1 | 3 |
| cp3_thin | `cp3_thin.zip` — sai format, đang là COCO thay vì Segmentation mask 1.1 | 1 / 1 | 3 |
| cp4_curb | `cp4_curb.zip` — sai format, có `annotations.xml` thay vì Segmentation mask 1.1 | 1 / 1 | 3 |
| cp6_coverage | `cp6_coverage.zip` — sai format, đang là COCO thay vì Segmentation mask 1.1 | 1 / 1 | 3 |
| **Tổng tối đa** | | | **100** |

Các ZIP đều có dữ liệu, không có ZIP rỗng. Self-check xác nhận cả 9 task đúng format và schema. Chưa có điểm tự đánh giá hoặc metric từ reference.

## 2. Một quyết định trước khi dùng gợi ý

- Ảnh, vị trí và object Medium đầu tiên tự vẽ: **Chưa cung cấp thông tin để xác nhận.**
- Class và quy tắc tôi dùng để chọn biên: **Chưa cung cấp thông tin để xác nhận.**
- Nếu dùng gợi ý sau đó: **Chưa cung cấp thông tin; không tự suy diễn từ file export.**

## 3. Một lỗi tôi tìm thấy và sửa

- Task/ảnh/vùng: **Lỗi export trước đó ở ba tier chính: `easy_semantic`, `medium_instance`, `hard_panoptic`.**
- Lỗi thuộc loại: **khác — dùng nhầm schema hoặc format export.**
- Bằng chứng tôi nhìn thấy: **Self-check trước đó báo Easy có class ngoài schema, Medium thiếu COCO JSON và Hard có category ngoài schema.**
- Quy tắc và hành động sửa: **Mở lại đúng task CVAT, kiểm tra class list riêng, Save và export lại đúng format theo `docs/SUBMISSION.md`.**
- Sau sửa đã Save và export lại chưa? **Đã. Self-check hiện tại xác nhận cả ba tier đạt.**

Kết quả chạy self-check hiện tại: cả 9 task đều OK; Hard có cảnh báo cần kiểm trực quan chồng lấn và phủ vùng panoptic. Chưa có điểm.

## 4. Ba ca chưa chắc hoặc đã cân nhắc

Các chi tiết quan sát trực tiếp trong CVAT chưa được cung cấp nên không ghi nhận thay cho người làm bài.

| Ảnh/vị trí | Hai cách hiểu có thể | Quy tắc/chứng cứ | Quyết định hoặc câu hỏi cho coach |
| --- | --- | --- | --- |
| 1 | Chưa cung cấp | Chưa có ghi chú vùng cụ thể | Cần bổ sung từ ảnh/CVAT |
| 2 | Chưa cung cấp | Chưa có ghi chú vùng cụ thể | Cần bổ sung từ ảnh/CVAT |
| 3 | Chưa cung cấp | Chưa có ghi chú vùng cụ thể | Cần bổ sung từ ảnh/CVAT |
