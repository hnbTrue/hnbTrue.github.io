---
title: "Start and flash mini image onto Stm32mp2"
description: "Dựng môi trường STM32MP2, hiểu ba lớp image / SDK / ứng dụng."
---

## Mục tiêu
Từ board trắng đến chạy được ứng dụng C++ cross-compile, nạp lên board trong vài giây.

## Kiến thức cốt lõi
- Ba lớp: **image** (Yocto, nạp SD), **SDK** (cross-compile trên laptop), **ứng dụng** (deploy nhanh bằng scp).
- Layer Yocto: poky, meta-st, layer riêng của bạn (meta-myapp).
- `.bbappend` + `FILESEXTRAPATHS:prepend`: ghi đè file mà không sửa layer gốc.
- Flash: chỉ nạp đúng phân vùng, kiểm tra bằng `lsblk` trước khi `dd`.
- Mạng trực tiếp laptop-board: IP tĩnh, tách khỏi WiFi.

## Danh sách bài (điền link khi viết xong)
- [ ] Ba lớp trong Yocto: image, SDK, ứng dụng
- [ ] bbappend: ghi đè file mà không sửa poky
- [ ] Nạp thẻ SD an toàn (và những lỗi suýt ghi nhầm ổ)
- [ ] Mạng trực tiếp laptop-board với IP tĩnh
- [ ] Cross-compile hello world bằng SDK và deploy.sh

## Câu tự kiểm tra
- Khi nào phải build lại image, khi nào chỉ cần build lại ứng dụng?
- Vì sao scp thẳng vào file đang chạy báo "Text file busy"?
