Dữ liệu:
```json
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
```
Yêu cầu chi tiết

1. Giao diện & Điều hướng (1 điểm)

- Navbar: Trang chủ, Thêm sản phẩm, Đăng nhập / Đăng ký.

- Giao diện hiện đại, tương thích mọi thiết bị.

2. Hiển thị danh sách sản phẩm (1 điểm)

- Gọi GET /products để hiển thị.

- Thể hiện bằng thẻ sản phẩm hoặc bảng gồm:

  - Tên sản phẩm (name)

  - Thương hiệu (brand)

  - Ảnh (image)

  - Trạng thái (status)

- Có nút Sửa, Xóa.

3. Xóa sản phẩm (1 điểm)

- Khi nhấn Xóa → confirm().

- Gọi DELETE /products/:id → cập nhật lại danh sách.

4. Thêm sản phẩm (2.5 điểm)

- Form thêm sản phẩm mới.

- POST /products thành công → alert + quay về danh sách.

- Validate (1 điểm):

  - `name`: bắt buộc.

  - `brand`: bắt buộc.

  - `image`: là URL hợp lệ.

  - `status`: chọn từ select (Còn hàng, Hết hàng, Ngừng kinh doanh).

5. Chỉnh sửa sản phẩm (2.5 điểm)

- Dùng GET /products/:id để tải dữ liệu ban đầu.

- Gọi PUT /products/:id để cập nhật.

- Validate tương tự form thêm.

6. Đăng ký & Đăng nhập (1 điểm)

- Đăng ký:

  - `email`: hợp lệ.

  - `password`: ≥ 6 ký tự.

- Đăng nhập:

  - Kiểm tra `email`/`password` đúng → alert thành công.

Bonus – Bảo vệ truy cập (1 điểm)

- Nếu chưa đăng nhập (không có `token` trong `localStorage`) → chuyển về trang đăng nhập khi truy cập các trang quản trị.

- Nếu đăng nhập → lưu token vào `localStorage`.
