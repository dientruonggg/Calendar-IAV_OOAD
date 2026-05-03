# Calendar System - OOAD Project

Đây là hệ thống Lịch (Calendar System) được xây dựng theo kiến trúc **Clean Architecture (N-Layer)**, tích hợp thiết kế hiện đại **Organic Productivity**. Hệ thống sử dụng Blazor WebAssembly cho frontend và ASP.NET Core Web API cho backend với cơ sở dữ liệu SQLite.

## 🌿 Design System: Organic Productivity

Dự án đã được cập nhật giao diện hoàn toàn mới dựa trên triết lý "Organic Productivity", tập trung vào trải nghiệm người dùng nhẹ nhàng, hiệu quả và thẩm mỹ:
- **Bảng màu Earthy**: Sử dụng các tông màu xanh lá cây đậm (Primary: `#3d532b`), xanh olive (Secondary: `#526438`) và màu kem (Surface: `#faf3e7`).
- **Typography**: Sử dụng font **Inter** hiện đại cho khả năng đọc tối ưu.
- **Micro-interactions**: Các hiệu ứng hover, chuyển cảnh mượt mà và bo góc lớn (Radius: 12px-24px) tạo cảm giác cao cấp.
- **Dashboard**: Trang chủ tích hợp widgets thống kê, lịch trình sắp tới và biểu đồ năng suất.

## 🚀 Công nghệ sử dụng (Tech Stack)

- **Frontend**: Blazor WebAssembly (.NET 10)
- **UI Framework**: [MudBlazor 9.2.0](https://mudblazor.com/)
- **Backend**: ASP.NET Core Web API
- **Database**: SQLite with Entity Framework Core
- **Authentication**: JWT-based Auth (Bearer Token)
- **Styling**: Vanilla CSS + MudBlazor Theme Provider

## 📁 Cấu trúc thư mục

- `src/Calendar.API`: Backend API xử lý logic và điều hướng.
- `src/Calendar.Client`: Frontend App chứa toàn bộ giao diện người dùng và trạng thái.
- `src/Calendar.Core`: Domain Entities, Interfaces và Enums cốt lõi.
- `src/Calendar.Infrastructure`: Data Access (EF Core, SQLite) và External Services (Email).
- `src/Calendar.Service`: Business Logic Layer xử lý nghiệp vụ.
- `src/Calendar.Shared`: DTOs dùng chung giữa API và Client.

## 🛠️ Hướng dẫn cài đặt và chạy ứng dụng

### 1. Phục hồi Packages
```bash
dotnet restore Calendar_OOAD.sln
```

### 2. Cập nhật Cơ sở dữ liệu
```bash
cd src/Calendar.API
dotnet ef database update --project ../Calendar.Infrastructure
```

### 3. Chạy Backend API (Terminal 1)
```bash
cd src/Calendar.API
dotnet run
```
*Mặc định lắng nghe tại: `http://localhost:5031` (hoặc cổng cấu hình trong launchSettings.json)*

### 4. Chạy Frontend Client (Terminal 2)
```bash
cd src/Calendar.Client
dotnet run
```
*Mặc định truy cập tại: `http://localhost:5137`*

## ✨ Các chức năng chính
- **Dashboard thông minh**: Thống kê cuộc hẹn, xem nhanh lịch trình và lời nhắc.
- **Calendar Views đa dạng**: Hỗ trợ xem theo Ngày (Daily), Tuần (Weekly) và Tháng (Monthly) với logic hiển thị sự kiện cả ngày (All-day) chuyên nghiệp.
- **Quản lý cuộc hẹn**: Tạo, chỉnh sửa, xóa và tham gia các cuộc họp nhóm.
- **Thông báo & Nhắc nhở**: Hệ thống email tự động và thông báo trong ứng dụng.
- **Cài đặt cá nhân**: Tùy chỉnh màu sắc lịch và thông tin tài khoản.

---
*Dự án được thực hiện cho môn học OOAD (Object-Oriented Analysis and Design).*
