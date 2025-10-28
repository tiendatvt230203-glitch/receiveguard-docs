---
title: Tìm kiếm & Chức năng
sidebar_position: 5
description: Các chức năng tìm kiếm và thao tác với email
---

# Tìm kiếm & Chức năng

## 🔍 Tìm kiếm email

![Search Section](./images/search-section.png)

### Tìm kiếm cơ bản

**Các trường tìm kiếm:**

| Trường | Ví dụ | Mô tả |
|--------|-------|-------|
| **Sender** | admin@example.com | Email hoặc tên người gửi |
| **Title** | Invoice | Từ khóa trong tiêu đề |
| **Receiver** | user@company.com | Email người nhận |
| **Sender IP** | 192.168.1.1 | IP nguồn |
| **Period** | 7 Days | Khoảng thời gian |
| **Delivery** | Status | Trạng thái gửi |

**Cách dùng:**
1. Nhập thông tin vào trường
2. Chọn khoảng thời gian (calendar icon)
3. Click **Search**

---

### Tìm kiếm nâng cao

![Detail Search](./images/detail-search.png)

**Click nút "Detail ▼"** để mở tìm kiếm nâng cao

**Các bộ lọc:**

**Whether Ad or not**
- Lọc theo loại quảng cáo

**Filtering**
- Lọc theo kết quả phân loại

**Falsified**
- Lọc email giả mạo header

**Sender address Danger**
- Lọc theo địa chỉ nguy hiểm

**Similarity**
- Lọc theo domain tương tự

**☑️ first time mail**
- Chỉ hiển thị email lần đầu nhận

---

## ⚡ Chức năng xử lý email

![Function Buttons](./images/function-buttons.png)

### 1. Process 'Read' (Đánh dấu đọc)

**Chức năng:**
- Chuyển email đã đọc → chưa đọc
- Hoặc ngược lại

**Cách dùng:**
1. Chọn email (checkbox)
2. Click **Process 'Read'**

**Khi nào dùng:**
- Đánh dấu email cần xem lại
- Reset trạng thái đọc

---

### 2. Deliver (Gửi email)

![Deliver Function](./images/deliver-function.png)

**Chức năng:**
- Gửi email bị chặn đến người nhận

**Cách dùng:**
1. Chọn email cần gửi
2. Click **Deliver**
3. Xác nhận

**Lưu ý:**
- ⚠️ Chỉ gửi, **KHÔNG** học AI
- Email tương tự vẫn có thể bị chặn sau này
- Dùng cho trường hợp gửi 1 lần

**Khác với:**
- **Permit** - Học AI nhưng không gửi
- **Permit and deliver** - Vừa học AI vừa gửi

---

### 3. Delete (Xóa)

**Chức năng:**
- Xóa email vĩnh viễn

**Cách dùng:**
1. Chọn email cần xóa
2. Click **Delete**
3. Xác nhận

**⚠️ Cảnh báo:**
- Không thể khôi phục
- Xóa khỏi hệ thống hoàn toàn
- Cẩn thận với email bị chặn nhầm

---

### 4. Report (🚩 Báo cáo)

![Report Function](./images/report-function.png)

**Chức năng:**
- Gửi email đến VNETWORK để phân tích
- Hoặc gửi đến IT Manager công ty

**Cách dùng:**
1. Chọn email nghi ngờ
2. Click **🚩**
3. Email được chuyển đến team kỹ thuật

**Khi nào dùng:**
- Không chắc email an toàn hay không
- Phát hiện mối đe dọa mới
- Cần chuyên gia phân tích

**Ai nhận báo cáo:**
- **Normal mail** → VNETWORK technical team
- **Blocked mail** → IT Manager công ty

---

### 5. Download Excel (📥)

![Excel Download](./images/excel-download.png)

**Chức năng:**
- Tải danh sách email ra file Excel

**Cách dùng:**
1. Chọn email cần tải
2. Click **📥**
3. File Excel tự động tải xuống

**Nội dung file:**
- Sender
- Receiver
- Title
- Filter result
- Status
- Receive date

**Khi nào dùng:**
- Lưu trữ báo cáo
- Phân tích ngoại tuyến
- Chia sẻ với team

---

## 📊 Bộ lọc nhanh

![Quick Filter](./images/quick-filter.png)

**Thanh công cụ lọc:**

### Process 'Read'
- Xem email đã đọc/chưa đọc

### Deliver
- Xem email đã gửi/chưa gửi

### Delete
- Không có bộ lọc

---

## 🎯 Ví dụ sử dụng

### Tìm email từ người gửi cụ thể

```
Sender: admin@example.com
Period: 30 Days
→ Click Search
```

### Tìm email chứa từ khóa

```
Title: Invoice
Period: 7 Days
→ Click Search
```

### Lọc email bị chặn

```
Click "Detail ▼"
Filtering: Blocked (Warning)
→ Click Search
```

### Tìm email giả mạo

```
Click "Detail ▼"
Falsified: ✓ (chọn loại)
→ Click Search
```

---

## 💡 Mẹo tìm kiếm

### Tìm kiếm chính xác
- Nhập **đầy đủ email** thay vì một phần
- Dùng **Detail search** cho kết quả tốt hơn

### Tìm kiếm nhanh
- Dùng **Left Menu** click vào số
- Nhanh hơn tìm kiếm thủ công

### Kết hợp bộ lọc
- Có thể chọn nhiều bộ lọc cùng lúc
- Kết quả là giao của các điều kiện

### Lưu kết quả
- Dùng **Download Excel** để lưu
- Giữ lại bằng chứng

---

## ⚙️ Cấu hình hiển thị

**Tùy chỉnh số email hiển thị:**

![Pagination](./images/pagination.png)

- **Domain dropdown** - Lọc theo domain
- **Every 15** - Số email mỗi trang (15/30/50/100)
- **◀ ▶** - Chuyển trang

**Sắp xếp:**
- Click vào **tên cột** để sắp xếp
- Click lần 2 để đổi chiều sắp xếp
