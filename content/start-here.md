---
title: "Bắt đầu từ đây"
draft: false
ShowToc: false
---

## Blog này nói về gì
Ghi chép quá trình mình học Embedded Linux và Edge AI trên board STM32MP2:
cái gì làm được, cái gì lỗi, và số liệu đo được.

## Lộ trình
1. [Start](/series/start-and-image/): board, image Yocto, SDK, vòng lặp build và chạy.
2. [Embedded Linux](/series/embedded-linux/): device tree, driver, systemd, debug.
3. [Pipeline](/series/pipeline-edge-ai/): đưa model lên NPU, đo và tối ưu.
4. [Dual core A and M](/series/a-core-and-m-core/): chia việc giữa Linux và M33.

## Cách đọc
- Bài **kien-thuc** giải thích khái niệm, bài **huong-dan** có lệnh làm theo, bài **ket-qua** có số liệu.
- Mỗi bài ghi rõ môi trường (board, phiên bản) để bạn tự lặp lại được.

## Phần cứng và công cụ
STM32MP257F-DK, Yocto (scarthgap), SDK cross-compile, C++ và Shell.
