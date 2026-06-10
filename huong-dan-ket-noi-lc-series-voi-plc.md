---
title: "Hướng Dẫn Kết Nối LC Series Hanyoung Nux Với PLC | Wiring NPN/PNP"
slug: huong-dan-ket-noi-lc-series-voi-plc-wiring-npn-pnp
date: 2026-06-09
updated: 2026-06-09
category: huong-dan-ky-thuat
tags: [HanyoungNux, LCSeries, PLC, Wiring, NPN, PNP, KetNoi, TuDongHoa]
description: "Hướng dẫn kết nối bộ đếm LC Series Hanyoung Nux với PLC. Sơ đồ đấu dây ngõ vào NPN, PNP, kết nối ngõ ra relay, và nguồn phụ 12V DC cho cảm biến."
author: Hanyoung Nux Việt Nam
lang: vi
parent: lc-series-hanyoung-nux-bo-dem-dinh-thoi-lcd
---

# Hướng Dẫn Kết Nối LC Series Hanyoung Nux Với PLC | Wiring NPN/PNP

Bài hướng dẫn này dành cho kỹ sư điện và kỹ thuật viên tự động hóa cần tích hợp **LC Series Hanyoung Nux** vào hệ thống có PLC.

---

## Ngõ vào: NPN vs PNP — Chọn đúng loại

LC Series hỗ trợ cả 2 loại ngõ vào:

| Loại | Đặc điểm | Phổ biến tại |
|---|---|---|
| NPN (sink) | Tín hiệu kéo xuống GND | Châu Á (Nhật, Hàn, Việt Nam) |
| PNP (source) | Tín hiệu kéo lên nguồn dương | Châu Âu |

> **Lưu ý:** Chọn loại NPN hay PNP phải khớp với loại cảm biến đang dùng.

---

## Sơ đồ đấu dây cơ bản

### Ngõ vào từ cảm biến NPN

```
Cảm biến NPN:
  Brown (VCC) → +12V DC (nguồn phụ LC Series)
  Blue  (GND) → 0V (COM)
  Black (OUT) → Ngõ vào B/O của LC Series
```

### Ngõ vào từ cảm biến PNP

```
Cảm biến PNP:
  Brown (VCC) → +12V DC
  Blue  (GND) → 0V (COM)
  Black (OUT) → Ngõ vào B/O của LC Series (cấu hình PNP mode)
```

### Ngõ ra relay kết nối PLC

```
LC Series OUT1 (COM) → PLC Input (COM)
LC Series OUT1 (NO)  → PLC Digital Input
```

---

## Nguồn phụ 12V DC tích hợp

LC Series có **nguồn phụ 12V DC tích hợp** để cấp cho cảm biến, giúp tiết kiệm nguồn cấp ngoài trong tủ điện.

| Chân | Mô tả |
|---|---|
| +12V | Nguồn dương cấp cho cảm biến |
| COM | Chung (0V) |

> Lưu ý kiểm tra dòng tối đa của nguồn phụ theo datasheet từng model trước khi kết nối nhiều cảm biến song song.

---

## Các lỗi kết nối thường gặp

| Lỗi | Nguyên nhân | Cách khắc phục |
|---|---|---|
| LC Series không đếm | Sai loại ngõ vào NPN/PNP | Kiểm tra lại loại cảm biến, cấu hình lại mode |
| Đếm nhảy số bất thường | Nhiễu tín hiệu (cáp dài không có shield) | Dùng cáp có shield, nối đất shield tại tủ điện |
| Ngõ ra không kích hoạt | Chưa cài đặt giá trị preset | Kiểm tra và cài đặt lại giá trị preset |

---

## Câu hỏi thường gặp

**LC Series kết nối được với PLC nào?**
Hầu hết PLC phổ biến: Mitsubishi FX/Q, Omron CP/CJ, Siemens S7, Delta DVP, Panasonic FP... vì giao tiếp qua tín hiệu số thông thường.

**Cáp tín hiệu từ encoder đến LC Series nên dài tối đa bao nhiêu?**
Khuyến nghị dưới 10m với cáp thường. Nếu xa hơn, dùng cáp có shield và tốc độ đếm sẽ bị giới hạn theo tần số tín hiệu.

---

*Xem thêm: [LC Series — Tổng quan](lc-series-hanyoung-nux-bo-dem-dinh-thoi-lcd.html) · [Hướng dẫn cài đặt Pre-scale](huong-dan-cai-dat-pre-scale-lc-series.html)*
