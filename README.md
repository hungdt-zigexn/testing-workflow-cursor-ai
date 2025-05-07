# Hướng dẫn sử dụng Testing Workflow

## 📋 Tổng quan

Testing Workflow là quy trình kiểm thử được thiết kế nhằm chuẩn hóa việc test và báo cáo kết quả. Quy trình này giúp đảm bảo chất lượng sản phẩm thông qua các bước test có hệ thống.

## 🔄 Quy trình 6 bước

1. **Đọc issue từ GitHub** - Hiểu yêu cầu và phạm vi cần test
2. **Đọc codebase** - Phân tích code để xác định ảnh hưởng
3. **Viết test case** - Lập kế hoạch test cụ thể
4. **Tạo file kết quả** - Chuẩn bị file lưu kết quả
5. **Thực hiện test** - Tiến hành test theo kế hoạch
6. **Bổ sung comments** - Nhận xét và đề xuất cải tiến

## 🚀 Cách sử dụng

### Bắt đầu workflow
Nhập lệnh: `Thực hiện bước 1 của testing-workflow cho issue #123`

### Chuyển sang bước tiếp theo
Nhập lệnh: `Tiếp tục với bước 2 của testing-workflow cho issue #123`

### Thực hiện một bước cụ thể
Nhập lệnh: `Thực hiện bước 4 của testing-workflow cho issue #123`

## 🔍 Kiểm tra MCP tự động

Trước mỗi bước, AI sẽ tự động kiểm tra:
- MCP Github (cần thiết cho bước 1)
- MCP Playwright (cần thiết cho bước 5)

Nếu MCP chưa hoạt động, AI sẽ nhắc nhở bật chức năng tương ứng trước khi tiếp tục.

## 📚 Lưu trữ knowledge

Sau mỗi bước, AI sẽ:
1. Thu thập thông tin (knowledge)
2. Đề xuất lưu vào file: `.cursor/knowledges/issues/{issue_id}_{current_date}.md`
3. Xác nhận nội dung với bạn
4. Cho phép chỉnh sửa nếu cần
5. Sử dụng knowledge cho các bước tiếp theo

## 📝 Chi tiết từng bước

### Bước 1: Đọc issue từ GitHub
- AI sẽ truy cập issue qua MCP Github
- Phân tích yêu cầu
- Tóm tắt các điểm cần test

### Bước 2: Đọc codebase
- Xác định các file và module liên quan
- Phân tích cơ chế hoạt động
- Xác định phạm vi ảnh hưởng

### Bước 3: Viết test case
- Sử dụng template từ `.cursor/templates/test-case.md`
- Lập các bước test chi tiết
- Xác định kết quả mong đợi

### Bước 4: Tạo file kết quả test
- Tạo file `{issue_id}_result.md` 
- Lưu trong thư mục `.cursor/knowledges/testings/`

### Bước 5: Thực hiện test
- Thực hiện test với MCP Playwright
- Cập nhật kết quả vào Compatibility Matrix
- Thêm evidence (hình ảnh, logs)

### Bước 6: Bổ sung comments
- Thêm nhận xét về kết quả test
- Ghi lại vấn đề phát hiện
- Đề xuất cải tiến

## 🌟 Ví dụ thực tế

**Ví dụ 1:** Kiểm tra tính năng đăng nhập
