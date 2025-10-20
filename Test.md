Dữ liệu:

```json
{
  "events": [
    {
      "id": 1,
      "title": "Workshop AI4Life 2025",
      "location": "Hà Nội",
      "image": "https://picsum.photos/id/1015/300/200",
      "status": "Sắp diễn ra"
    },
    {
      "id": 2,
      "title": "FPT Hackathon",
      "location": "Đà Nẵng",
      "image": "https://picsum.photos/id/1018/300/200",
      "status": "Đã kết thúc"
    }
  ],
  "users": []
}
```


Yêu cầu chi tiết

1. Giao diện & Điều hướng (1 điểm)

- Navbar: Trang chủ, Thêm khóa học, Đăng nhập / Đăng ký.

- Giao diện responsive, rõ ràng.

2. Hiển thị danh sách khóa học (1 điểm)

- Gọi GET /courses để hiển thị danh sách.

- Hiển thị bằng card hoặc bảng gồm:

  - Tên khóa học (title)

  - Giảng viên (instructor)

  - Ảnh khóa học (image)

  - Trạng thái (status)

- Mỗi khóa học có nút Sửa, Xóa.

3. Xóa khóa học (1 điểm)

- Có confirm() trước khi xóa.

- Gọi DELETE /courses/:id → cập nhật lại danh sách.

4. Thêm khóa học (2.5 điểm)

- Form thêm khóa học mới.

- Gọi POST /courses thành công → alert + quay về danh sách.

- Validate (1 điểm):

  - `title`: bắt buộc.

  - `instructor`: bắt buộc.

  - `image`: là URL hợp lệ.

  - `status`: chọn từ select (Đang mở đăng ký, Đang học, Đã hoàn thành).

5. Chỉnh sửa khóa học (2.5 điểm)

- GET /courses/:id để tải dữ liệu ban đầu.

- Sửa xong gọi PUT /courses/:id → alert + điều hướng về danh sách.

- Validate tương tự form thêm.

6. Đăng ký & Đăng nhập (1 điểm)

- Đăng ký:

  - `email`: định dạng hợp lệ.

  - `password`: ≥ 6 ký tự.

- Đăng nhập:

  - Đúng `email`/`password` → alert đăng nhập thành công.

Bonus – Bảo vệ truy cập (1 điểm)

- Nếu chưa có token trong localStorage → tự động chuyển về trang đăng nhập khi truy cập trang quản lý, thêm/sửa.

- Khi đăng nhập thành công → lưu token.


