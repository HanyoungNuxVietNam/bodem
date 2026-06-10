---
title: "Hướng Dẫn Cài Đặt Pre-Scale LC Series Hanyoung Nux | Từng Bước"
slug: huong-dan-cai-dat-pre-scale-lc-series-hanyoung-nux
date: 2026-06-09
updated: 2026-06-09
category: huong-dan-ky-thuat
tags: [HanyoungNux, LCSeries, PreScale, CaiDat, HuongDan, BoDem]
description: "Hướng dẫn từng bước cài đặt Pre-scale trên LC Series Hanyoung Nux. Công thức tính Pre-scale cho ứng dụng đo chiều dài, đo tốc độ và đếm theo tỷ lệ."
author: Hanyoung Nux Việt Nam
lang: vi
parent: lc-series-hanyoung-nux-bo-dem-dinh-thoi-lcd
---

# Hướng Dẫn Cài Đặt Pre-Scale LC Series Hanyoung Nux | Từng Bước

**Pre-scale** là tính năng quan trọng nhất của LC Series, cho phép quy đổi số xung đầu vào thành đơn vị thực tế (mét, kg, sản phẩm...). Dải Pre-scale của LC Series: **0.00001 đến 999999**.

---

## Pre-scale là gì?

Pre-scale là hệ số nhân được áp dụng cho từng xung đầu vào trước khi cộng vào giá trị hiển thị.

```
Giá trị hiển thị = Số xung nhận được × Pre-scale
```

**Ví dụ đơn giản:**
- Encoder phát 500 xung/mét
- Pre-scale = 1/500 = **0.002**
- Sau 500 xung → màn hình hiển thị **1.000** (1 mét)

---

## Công thức tính Pre-scale theo ứng dụng

### Ứng dụng đo chiều dài (encoder + con lăn)

```
Pre-scale = Chu vi con lăn (m) / Số xung/vòng của encoder
```

| Chu vi con lăn | Encoder | Pre-scale |
|---|---|---|
| 0.314 m (D=100mm) | 1000 xung/vòng | 0.000314 |
| 0.5 m | 500 xung/vòng | 0.001 |
| 1.0 m | 1000 xung/vòng | 0.001 |

### Ứng dụng đếm sản phẩm (tỷ lệ 1:1)

```
Pre-scale = 1
```
Mỗi xung = 1 sản phẩm. Không cần quy đổi.

### Ứng dụng đếm theo lô (1 xung = N sản phẩm)

```
Pre-scale = N (số sản phẩm mỗi lô)
```

---

## Các bước cài đặt Pre-scale trên LC Series

1. Nhấn và giữ nút **MD** để vào menu cài đặt
2. Chọn mục **Pre-scale** (ký hiệu P.SC trên màn hình)
3. Dùng nút **▲ ▼** để thay đổi từng chữ số
4. Dùng nút **►** để di chuyển sang chữ số tiếp theo
5. Nhấn **MD** để xác nhận và lưu

---

## Kiểm tra sau khi cài đặt

Sau khi cài Pre-scale, chạy thử:
- Đặt 1 mét vải qua con lăn → màn hình phải hiển thị **1.000**
- Nếu lệch, tính lại Pre-scale theo đúng chu vi con lăn thực tế (dùng thước đo lại)

---

## Câu hỏi thường gặp

**Pre-scale có thể thay đổi khi máy đang chạy không?**
Không khuyến nghị. Nên dừng máy, reset bộ đếm về 0 trước khi thay đổi Pre-scale để tránh lỗi tích lũy.

**Tôi cần hiển thị kg thay vì mét, tính Pre-scale thế nào?**
Nguyên tắc tương tự: tìm hệ số quy đổi giữa số xung cảm biến và đơn vị kg cần hiển thị, rồi nhập vào Pre-scale.

---

*Xem thêm: [LC Series — Tổng quan](lc-series-hanyoung-nux-bo-dem-dinh-thoi-lcd.html) · [Hướng dẫn kết nối LC Series với PLC](huong-dan-ket-noi-lc-series-voi-plc.html)*
