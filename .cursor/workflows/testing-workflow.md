# Testing Workflow Guide
### Quy trình test và báo cáo kết quả

## Tổng quan quy trình

Workflow này bao gồm 6 bước chính:
1. Đọc issue từ GitHub để hiểu requirement
2. Đọc codebase để xác định phạm vi ảnh hưởng
3. Viết test case dựa trên template
4. Tạo file kết quả test
5. Thực hiện test và cập nhật kết quả
6. Bổ sung comments (nếu cần)

## Kiểm tra MCP và lưu knowledge

Trong mỗi bước:
1. Tự động kiểm tra MCP cần thiết (Github/Playwright)
2. Thu thập thông tin (knowledge) từ bước đó
3. Lưu knowledge vào file `.cursor/knowledges/issues/{issue_id}_{current_date}.md`, hãy lưu đúng vào folder .cursor của dự án nhé
4. Xác nhận với user về tính chính xác của knowledge
5. Cho phép user chỉnh sửa knowledge nếu cần
6. Sử dụng knowledge đã xác nhận cho các bước tiếp theo
7. Báo cáo với user để user biết được là kiểm tra rồi

## Cách sử dụng

1. Nhắc đến workflow này khi muốn bắt đầu quy trình test: "Thực hiện bước 1 của testing-workflow cho issue #XXX"
2. Để chuyển sang bước tiếp theo: "Tiếp tục với bước X của testing-workflow cho issue #XXX"
3. Để thực hiện một bước cụ thể: "Thực hiện bước X của testing-workflow cho issue #XXX"

## Chi tiết các bước

### Bước 1: Đọc issue từ GitHub
**Lệnh mẫu:** "Thực hiện bước 1 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ:
- Truy cập issue #XXX trên GitHub thông qua MCP github
- Phân tích requirement
- Tóm tắt các điểm chính cần test

### Bước 2: Đọc codebase 
**Lệnh mẫu:** "Tiếp tục với bước 2 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ:
- Xác định các file và module có liên quan đến issue
- Phân tích code để hiểu cơ chế hoạt động
- Xác định phạm vi ảnh hưởng

### Bước 3: Viết test case
**Lệnh mẫu:** "Tiếp tục với bước 3 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ:
- Sử dụng template từ `.cursor/templates/test-case.md`
- Điền thông tin test case dựa trên requirement
- Xác định các bước test chi tiết
- Xác định kết quả mong đợi

### Bước 4: Tạo file kết quả test
**Lệnh mẫu:** "Tiếp tục với bước 4 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ:
- Tạo file markdown với tên: `{issue_id}_result.md`
- Lưu file trong cùng thư mục với file `.cursor/testings/issue_id_result.md`
- Copy nội dung test case đã viết vào file kết quả

### Bước 5: Thực hiện test
**Lệnh mẫu:** "Tiếp tục với bước 5 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ hỗ trợ bạn:
- Thực hiện test theo các bước đã định nghĩa
- Sử dụng MCP playwright
- Cập nhật kết quả vào phần "Compatibility Matrix"
- Thêm evidence nếu cần

### Bước 6: Bổ sung comments
**Lệnh mẫu:** "Tiếp tục với bước 6 của testing-workflow cho issue #XXX"

Khi được yêu cầu, tôi sẽ:
- Bổ sung comments nếu cần
- Ghi chú các vấn đề phát hiện
- Đề xuất cải tiến nếu cần

## Template mẫu

### Test Case ID: TC-XXX

Xem thêm ở file: .cursor/templates/test-case.md

**Test Type:** Feature
**Function:** - [Tóm tắt chức năng được test]

---

### 📝 Test Steps:
1. Go to URL: `[URL cụ thể]`
2. [Bước thao tác tiếp theo]
3. [Bước thao tác tiếp theo]
...
N. [Bước cuối: hành động kiểm tra]

---

### ✅ Expected Result:
- Step N: [Mô tả kết quả mong muốn]
  - Redirect URL (nếu có): `[URL sau redirect]`
  - HTTP status (nếu có): `xxx`
  - Evidence SP: [Link gyazo hoặc ảnh minh họa]
  - Evidence APP: [Link gyazo hoặc ảnh minh họa]
  - Evidence PC: [Link gyazo hoặc ảnh minh họa]

---

### 🎯 Target:
`SP`, `PC`, `APP` hoặc tổ hợp: `SP+PC+APP`

---

### ✅ Compatibility Matrix

| Browser / Device / OS       | Result  |
|-----------------------------|---------|
| Chrome vXXX                 | Pass/NG |
| Firefox vXXX                | Pass/NG |
| Safari vXXX                 | Pass/NG |
| iOS vXXX                    | Pass/NG |
| Android [Link if available] | Pass/NG |

---

### 🛠️ Production Check:
**Status:** Pass

---

### 💬 Comments:
[Comment nếu có]