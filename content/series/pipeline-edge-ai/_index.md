---
title: "Pipeline"
description: "Đưa model lên NPU, đo latency/RAM/CPU, tối ưu quanh model."
---

## Mục tiêu
Chạy model trên board, có số liệu so CPU với NPU và giải thích được nút thắt.

## Kiến thức cốt lõi
- Flow: train → xuất ONNX/TFLite → lượng tử hoá int8 → biên dịch cho NPU (ST Edge AI) → runtime trên board → ứng dụng C++.
- NPU cần model int8; operator không hỗ trợ sẽ bị đẩy về CPU và chạy chậm.
- Đo: latency (ms/lần suy luận), FPS, %CPU, RAM; chạy nhiều lần, bỏ lần khởi động đầu.
- Tối ưu quanh model: tách thread, giảm copy bộ nhớ, tiền/hậu xử lý nhanh.

## Danh sách bài
- [ ] Phần cứng AI của STM32MP25: CPU, GPU, NPU làm gì
- [ ] Từ ONNX đến NPU: các bước và lỗi hay gặp
- [ ] Lượng tử hoá int8: độ chính xác đổi lấy tốc độ
- [ ] Benchmark CPU và NPU (bảng số liệu)
- [ ] Tìm nút thắt: tiền xử lý hay suy luận?

## Câu tự kiểm tra
- Vì sao thêm thread không làm suy luận trên NPU nhanh hơn?
- Cách bạn đảm bảo số đo công bằng giữa CPU và NPU?
