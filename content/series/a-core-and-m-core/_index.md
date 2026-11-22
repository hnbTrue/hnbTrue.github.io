---
title: "Dual core A and M"
description: "Chia việc giữa Linux (Cortex-A) và real-time (Cortex-M33)."
---

## Mục tiêu
Lõi M33 làm việc có thời gian chặt chẽ, Linux nhận dữ liệu và xử lý.

## Kiến thức cốt lõi
- A-core chạy Linux (không real-time chặt); M-core chạy firmware riêng, phản hồi theo chu kỳ cố định.
- **remoteproc:** cách Linux nạp và khởi động firmware cho M-core.
- **RPMsg / OpenAMP:** kênh nhắn tin giữa Linux và M-core.
- Khi nào nên đẩy việc sang M-core: cần chu kỳ ổn định, độ trễ thấp.

## Danh sách bài
- [ ] Kiến trúc A/M của STM32MP25 trên một trang
- [ ] Nạp firmware M33 bằng remoteproc
- [ ] Gửi dữ liệu M33 → Linux qua RPMsg
- [ ] Đo độ ổn định chu kỳ lấy mẫu

## Câu tự kiểm tra
- Vì sao Linux thường không đảm bảo real-time chặt?
- Dữ liệu đi từ M33 sang Linux qua những lớp nào?
