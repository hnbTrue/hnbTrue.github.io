---
title: "Embedded Linux"
description: "Device tree, driver cơ bản, systemd, và công cụ debug."
---

## Mục tiêu
Hiểu cách Linux nhận biết phần cứng và cách chạy/debug một dịch vụ trên board.

## Kiến thức cốt lõi
- **Device tree:** file `.dts` mô tả phần cứng, biên dịch bằng `dtc` ra `.dtb`; kernel đọc lúc khởi động để biết có thiết bị nào.
- **Kernel module:** `Makefile` với `obj-m`, nạp bằng `insmod`, gỡ bằng `rmmod`, xem log bằng `dmesg`.
- **systemd:** viết file `.service`, `systemctl enable/status`, `journalctl -u`.
- **Debug:** `gdbserver` trên board + gdb của SDK trên laptop; `strace` xem system call; `perf` xem CPU tốn ở đâu.

## Danh sách bài
- [ ] Device tree là gì? Đọc dts của board
- [ ] Viết kernel module đầu tiên (LED/GPIO)
- [ ] Chạy ứng dụng như một service systemd
- [ ] Debug từ xa bằng gdbserver
- [ ] strace và perf: tìm vì sao ứng dụng chậm

## Câu tự kiểm tra
- Khác nhau giữa driver trong kernel và ứng dụng chạy ở user space?
- Service bị restart liên tục thì xem log ở đâu?
