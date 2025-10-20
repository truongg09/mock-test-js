Dữ liệu: 
{
  "products": [
    {
      "id": 1,
      "name": "iPhone 16 Pro",
      "brand": "Apple",
      "image": "https://picsum.photos/id/1040/300/200",
      "status": "Còn hàng"
    },
    {
      "id": 2,
      "name": "Laptop ASUS ROG",
      "brand": "ASUS",
      "image": "https://picsum.photos/id/1041/300/200",
      "status": "Hết hàng"
    }
  ],
  "users": []
}

Yêu cầu chi tiết

Giao diện & Điều hướng (1 điểm)

Navbar: Trang chủ, Thêm khóa học, Đăng nhập / Đăng ký.

Giao diện responsive, rõ ràng.

Hiển thị danh sách khóa học (1 điểm)

Gọi GET /courses để hiển thị danh sách.

Hiển thị bằng card hoặc bảng gồm:

Tên khóa học (title)

Giảng viên (instructor)

Ảnh khóa học (image)

Trạng thái (status)

Mỗi khóa học có nút Sửa, Xóa.

Xóa khóa học (1 điểm)

Có confirm() trước khi xóa.

Gọi DELETE /courses/:id → cập nhật lại danh sách.

Thêm khóa học (2.5 điểm)

Form thêm khóa học mới.

Gọi POST /courses thành công → alert + quay về danh sách.

Validate (1 điểm):

title: bắt buộc.

instructor: bắt buộc.

image: là URL hợp lệ.

status: chọn từ select (Đang mở đăng ký, Đang học, Đã hoàn thành).

Chỉnh sửa khóa học (2.5 điểm)

GET /courses/:id để tải dữ liệu ban đầu.

Sửa xong gọi PUT /courses/:id → alert + điều hướng về danh sách.

Validate tương tự form thêm.

Đăng ký & Đăng nhập (1 điểm)

Đăng ký:

email: định dạng hợp lệ.

password: ≥ 6 ký tự.

Đăng nhập:

Đúng email/password → alert đăng nhập thành công.

Bonus – Bảo vệ truy cập (1 điểm)

Nếu chưa có token trong localStorage → tự động chuyển về trang đăng nhập khi truy cập trang quản lý, thêm/sửa.

Khi đăng nhập thành công → lưu token.

🧩 Đề 2: Quản lý Sản phẩm Công nghệ (Tech Products Management)
Dữ liệu mẫu
{
  "products": [
    {
      "id": 1,
      "name": "iPhone 16 Pro",
      "brand": "Apple",
      "image": "https://picsum.photos/id/1040/300/200",
      "status": "Còn hàng"
    },
    {
      "id": 2,
      "name": "Laptop ASUS ROG",
      "brand": "ASUS",
      "image": "https://picsum.photos/id/1041/300/200",
      "status": "Hết hàng"
    }
  ],
  "users": []
}

Yêu cầu chi tiết

Giao diện & Điều hướng (1 điểm)

Navbar: Trang chủ, Thêm sản phẩm, Đăng nhập / Đăng ký.

Giao diện hiện đại, tương thích mọi thiết bị.

Hiển thị danh sách sản phẩm (1 điểm)

Gọi GET /products để hiển thị.

Thể hiện bằng thẻ sản phẩm hoặc bảng gồm:

Tên sản phẩm (name)

Thương hiệu (brand)

Ảnh (image)

Trạng thái (status)

Có nút Sửa, Xóa.

Xóa sản phẩm (1 điểm)

Khi nhấn Xóa → confirm().

Gọi DELETE /products/:id → cập nhật lại danh sách.

Thêm sản phẩm (2.5 điểm)

Form thêm sản phẩm mới.

POST /products thành công → alert + quay về danh sách.

Validate (1 điểm):

name: bắt buộc.

brand: bắt buộc.

image: là URL hợp lệ.

status: chọn từ select (Còn hàng, Hết hàng, Ngừng kinh doanh).

Chỉnh sửa sản phẩm (2.5 điểm)

Dùng GET /products/:id để tải dữ liệu ban đầu.

Gọi PUT /products/:id để cập nhật.

Validate tương tự form thêm.

Đăng ký & Đăng nhập (1 điểm)

Đăng ký:

email: hợp lệ.

password: ≥ 6 ký tự.

Đăng nhập:

Kiểm tra email/password đúng → alert thành công.

Bonus – Bảo vệ truy cập (1 điểm)

Nếu chưa đăng nhập → chuyển về trang đăng nhập khi truy cập các trang quản trị.

Lưu token vào localStorage khi đăng nhập.
