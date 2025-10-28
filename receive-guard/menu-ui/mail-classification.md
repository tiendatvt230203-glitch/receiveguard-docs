---
title: Phân loại email
sidebar_position: 6
description: Chi tiết các cách phân loại email trong ReceiveGuard
---

# Phân loại email

ReceiveGuard tự động phân loại email vào các hộp thư theo mức độ nguy hiểm.

## 📊 Tổng quan phân loại

![Mail Classification Overview](./images/classification-overview.png)

**3 nhóm chính:**

1. **✅ Normal** - Email an toàn
2. **⚠️ Blocked (Caution)** - Email nguy hiểm
3. **🔍 Falsified Mail Inspection** - Email giả mạo

---

## ✅ Normal (Email an toàn)

![Normal Classification](./images/normal-classification.png)

### Normal Mail Box

**Đặc điểm:**
- ✓ Kiểm tra hoàn toàn an toàn
- ✓ Tất cả test đều pass
- ✓ Gửi trực tiếp đến người nhận

**Khi nào email vào đây:**
- Từ người gửi đã học
- Không có dấu hiệu nguy hiểm
- Header hợp lệ
- Không có virus/malware

---

### Normal Reliability

**Đặc điểm:**
- ✓ Độ tin cậy > 80%
- ✓ Qua kiểm tra độ tin cậy
- ✓ An toàn nhưng theo dõi

**Khi nào email vào đây:**
- Người gửi mới
- Chưa đủ lịch sử để học
- Không có dấu hiệu rõ ràng nguy hiểm

---

## ⚠️ Blocked (Caution) - Email nguy hiểm

![Blocked Classification](./images/blocked-classification.png)

### Work (Ad - Work)

**Đặc điểm:**
- Nội dung giống email công việc
- Nhưng có đặc điểm spam
- Quảng cáo ngụy trang

**Ví dụ:**
- Email yêu cầu cập nhật thông tin
- Đề nghị kinh doanh không mong muốn

---

### Advertisement (Ad - Normal)

**Đặc điểm:**
- Email quảng cáo rõ ràng
- Spam thông thường
- Nội dung marketing

**Ví dụ:**
- Khuyến mãi
- Newsletter không đăng ký
- Quảng cáo sản phẩm

---

### Virus Mail

![Virus Detection](./images/virus-detection.png)

**Đặc điểm:**
- ⚠️ Phát hiện virus trong file đính kèm
- ⚠️ Link nguy hiểm
- ⚠️ Executable file độc hại

**Phát hiện:**
- Quét file đính kèm
- Kiểm tra URL
- Phân tích trong sandbox

**Hành động:**
- Chặn hoàn toàn
- KHÔNG gửi đến user
- Thông báo trong report

---

### Ransomware

![Ransomware Detection](./images/ransomware-detection.png)

**Đặc điểm:**
- ⚠️⚠️ Phát hiện ransomware
- ⚠️⚠️ File mã hóa dữ liệu
- ⚠️⚠️ Mối đe dọa nghiêm trọng

**Phát hiện:**
- Phân tích hành vi file
- Sandbox testing
- Signature matching

**Hành động:**
- Chặn ngay lập tức
- Alert cao nhất
- Báo cáo security team

---

## 🔍 Falsified Mail Inspection

![Falsified Inspection](./images/falsified-inspection.png)

### Falsified Header (Header giả mạo)

**4 loại:**

#### 1. Falsified Address
![Falsified Address](./images/falsified-address.png)

**Phát hiện:**
- Email address bị sửa đổi
- Display name ≠ actual address

**Ví dụ:**
```
Hiển thị: CEO <ceo@company.com>
Thực tế: hacker@fake.com
```

---

#### 2. Falsified ID
![Falsified ID](./images/falsified-id.png)

**Phát hiện:**
- ID người gửi thay đổi khi reply
- Reply-to khác sender

**Ví dụ:**
```
From: support@bank.com
Reply-To: hacker@gmail.com
```

---

#### 3. Falsified Domain
![Falsified Domain](./images/falsified-domain.png)

**Phát hiện:**
- Domain bị giả mạo
- Không match SPF/DKIM

**Ví dụ:**
```
Giả: paypa1.com (số 1)
Thật: paypal.com (chữ l)
```

---

#### 4. Falsified the others
![Falsified Others](./images/falsified-others.png)

**Phát hiện:**
- Header khác bị sửa
- Metadata không khớp

---

## 🚨 Sender Address - Nguy hiểm địa chỉ

![Sender Danger](./images/sender-address-danger.png)

### First (IP thay đổi)

**Phát hiện:**
- IP người gửi khác so với trước
- Sender từ location mới

**Ví dụ:**
```
Trước: 192.168.1.1 (Vietnam)
Nay: 10.0.0.1 (Russia)
```

---

### Final (Mail server thay đổi)

**Phát hiện:**
- Mail server cuối cùng khác
- Route path thay đổi

**Ví dụ:**
```
Trước: mail.company.com
Nay: smtp.unknown.com
```

---

### The others (Đường đi thay đổi)

**Phát hiện:**
- Path routing khác
- Intermediate hops thay đổi

---

## 🎭 Similar Domain

![Similar Domain Detection](./images/similar-domain-detection.png)

### All (So với công ty)

**Phát hiện:**
- Domain giống domain trong công ty
- Phishing attempt

**Ví dụ:**
```
Thật: vnetwork.vn
Giả: vnetw0rk.vn (chữ o → số 0)
```

---

### Personal (So với cá nhân)

**Phát hiện:**
- Domain giống email đã nhận cá nhân
- Targeted phishing

---

## 📧 FakeMailer

![FakeMailer Detection](./images/fakemailer-detection.png)

**Phát hiện:**
- Email từ fake mail server
- Không dùng SMTP chính thức
- Tool gửi email hàng loạt

**Ví dụ:**
- PHPMailer không config đúng
- Script spam
- Bulk email tools

---

## 🎯 Filtering (Lọc nâng cao)

![Advanced Filtering](./images/advanced-filtering.png)

### Các cấp độ lọc

#### Normal Mail Box
- 100% khớp thông tin đã học
- Trusted sender

#### Blocked (Caution)
- Trong permission list
- Nhưng thông tin không khớp

#### Normal Reliability
- Độ tin cậy > 80%

#### Blocked (Warning)
- Có khả năng nguy hiểm
- Chưa 100% normal

#### Low Reliability
- Độ tin cậy < 80%

#### Danger
- Không hoàn toàn bình thường
- Chưa phát hiện threat cụ thể

#### Virus
- Virus trong attachment

#### Danger URL
- URL nguy hiểm phát hiện

#### Ransomware
- Ransomware detected

#### Danger Action
- File kích hoạt hành động nguy hiểm

#### Link Document
- URL nguy hiểm trong document

---

## 👤 User Option

![User Option](./images/user-option.png)

**Blacklist do user tự đăng ký:**

**Chặn theo:**
- ✉️ Mail address
- 🌐 Domain
- 🔢 IP
- 📝 Title
- 📄 Body text

---

## 📎 Extension Blocked Option

![Extension Blocked](./images/extension-blocked.png)

**File bị chặn theo extension:**

**Ví dụ extension nguy hiểm:**
- `.exe` - Executable
- `.js` - JavaScript
- `.vbs` - VBScript
- `.bat` - Batch file
- `.cmd` - Command file

**Cấu hình:** Option → Filter → Extension Blocked

---

## 📊 Bảng tóm tắt

| Loại | Mức độ | Gửi đến user | Hành động |
|------|--------|--------------|-----------|
| Normal Mail Box | ✅ An toàn | ✓ Có | Không cần |
| Normal Reliability | ✅ Tin cậy | ✓ Có | Theo dõi |
| Work/Ad | ⚠️ Spam | ✗ Không | Review |
| Virus | 🔴 Nguy hiểm | ✗ Không | Chặn |
| Ransomware | 🔴🔴 Rất nguy hiểm | ✗ Không | Chặn + Alert |
| Falsified | 🔴 Giả mạo | ✗ Không | Review |
| Similar Domain | ⚠️ Phishing | ✗ Không | Xác minh |

---

## 💡 Mẹo đọc phân loại

### Màu sắc
- 🟢 Xanh = An toàn
- 🟡 Vàng = Cảnh báo
- 🔴 Đỏ = Nguy hiểm

### Số liệu
- Số lớn ở Normal = Tốt
- Số lớn ở Blocked = Cần kiểm tra
- Số ở Virus/Ransomware > 0 = Cảnh báo cao

### Kiểm tra hàng ngày
1. Normal - nên cao
2. Blocked - review xem có false positive
3. Virus/Ransomware - kiểm tra nguồn
4. Similar Domain - xác minh ngay
