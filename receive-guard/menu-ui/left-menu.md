---
title: Menu trái
sidebar_position: 3
description: Phân loại email theo các hộp thư
---

# Menu trái (Left Menu)

![Left Menu](./images/left-menu.png)

Menu bên trái hiển thị email được phân loại tự động bởi AI.

---

## 📬 All Mail Box

![All Mail Box](./images/all-mailbox.png)

**Hiển thị tổng số email** nhận được trong ngày

**Các số liệu:**
- **Ad (Work)** - Spam dạng công việc
- **Ad (Normal)** - Quảng cáo thông thường
- **Virus Mail** - Email chứa virus
- **Ransomware** - Email chứa ransomware

---

## ✅ Normal (Email an toàn)

![Normal Mail](./images/normal-mail.png)

**Tổng số email an toàn**

### Phân loại:

**Normal Mail Box**
- Email hoàn toàn an toàn
- Đã kiểm tra kỹ

**Normal Reliability**
- Độ tin cậy trên 80%
- Qua kiểm tra độ tin cậy

---

## ⚠️ Blocked (Caution) - Email nguy hiểm

![Blocked Mail](./images/blocked-mail.png)

**Tổng số email nguy hiểm bị chặn**

### Các loại:

**Work** (0)
- Nội dung giống công việc nhưng là spam

**Advertisement** (4)
- Email quảng cáo
- Spam

**Virus Mail** (1)
- Phát hiện virus
- Link/file nguy hiểm

**Ransomware** (0)
- Phát hiện ransomware
- File mã hóa dữ liệu

---

## 🔍 Falsified Header - Header giả mạo

![Falsified Header](./images/falsified-header.png)

**Email có thông tin header bị sửa đổi**

### Các loại:

**Falsified Address**
- Địa chỉ email bị giả mạo

**Falsified ID**
- ID người gửi bị thay đổi

**Falsified Domain**
- Domain bị giả mạo

**Falsified the others**
- Thông tin header khác bị sửa

---

## 🚨 Sender Address - Địa chỉ gửi nguy hiểm

![Sender Address](./images/sender-danger.png)

**Email gửi từ địa chỉ khác so với trước**

### Các loại:

**First**
- IP người gửi thay đổi

**Final**
- Mail server thay đổi

**The others**
- Đường đi email thay đổi

---

## 🎭 Similar Domain - Domain tương tự

![Similar Domain](./images/similar-domain.png)

**Email từ domain giống domain hợp lệ**

### Phân loại:

**All**
- Giống domain trong công ty

**Personal**
- Giống domain cá nhân đã nhận

---

## 📧 FakeMailer

![FakeMailer](./images/fakemailer.png)

**Email gửi từ mail server giả**
- Không phải từ mail server chính thức
- Dùng fake mail server

---

## 🎯 Filtering - Lọc nâng cao

![Filtering](./images/filtering.png)

### Normal

**Normal Mail Box**
- Khớp 100% thông tin đã học

**Normal Reliability**
- Độ tin cậy > 80%

### Blocked

**Blocked (Caution)**
- Trong danh sách cho phép nhưng thông tin không khớp

**Blocked (Warning)**
- Có khả năng nguy hiểm

**Low Reliability**
- Độ tin cậy < 80%

### Threat (Mối đe dọa)

**Danger**
- Không hoàn toàn bình thường

**Virus**
- Phát hiện virus trong file đính kèm

**Danger URL**
- Phát hiện link nguy hiểm

**Ransomware**
- Phát hiện ransomware

**Danger Action**
- File kích hoạt hành động nguy hiểm

**Link Document**
- Phát hiện URL nguy hiểm trong tài liệu

### User Options

**User Option**
- Danh sách đen do user đăng ký
- Chặn theo: email, domain, IP, tiêu đề, nội dung

**Extension Blocked Option**
- File đính kèm bị chặn theo phần mở rộng
- Cấu hình bởi admin

---

## 📊 Cách đọc số liệu

**Ví dụ:**
```
All Mail Box         763
  Ad (Work)            0
  Ad (Normal)          4
  Virus Mail           1
  Ransomware           0
```

**Ý nghĩa:**
- Tổng 763 email trong ngày
- 0 spam công việc
- 4 quảng cáo thường
- 1 email có virus
- 0 ransomware

---

## Mẹo sử dụng

### Kiểm tra hàng ngày
1. Xem **All Mail Box** - tổng số email
2. Kiểm tra **Blocked (Caution)** - email bị chặn
3. Xem **Virus Mail** - có virus không
4. Kiểm tra **Similar Domain** - có giả mạo không

### Click vào số để xem chi tiết
- Click vào bất kỳ category nào
- Danh sách email sẽ hiển thị bên phải
- Click vào email để xem chi tiết

### Màu sắc
- **Xanh** - Normal (An toàn)
- **Đỏ** - Blocked (Nguy hiểm)
- **Vàng** - Caution (Cảnh báo)
