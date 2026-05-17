### PHẦN A:

CÂU A1:
1. Thẻ <meta viewport> chuẩn:
<meta name="viewport" content="width=device-width, initial-scale=1.0">

** Giải thích thuộc tính:
- `width=device-width`: Đặt chiều rộng của viewport bằng chiều rộng của thiết bị
- `initial-scale=1.0`: Đặt mức thu phóng ban đầu khi trang được tải lần đầu bởi trình duyệt

2. Nếu THIẾU thẻ này, iPhone sẽ hiển thị trang web có chiều rộng mặc định là khoảnh 980px và tự động thu nhỏ để vừa khít màn hình điện thoại

3. Mobile-First và Desktop-First khác nhau thế nào? Viết ví dụ CSS cho mỗi cách với breakpoint 768px. Tại sao Mobile-First được khuyên dùng?

- Mobile-First và Desktop-First:
+ Mobile-First: Viết CSS cho màn hình nhỏ trước, sau đó dùng `min-width` để ghi đè cho màn hình lớn
+ Desktop-First: Viết CSS cho màn hình lớn trước, sau đó dùng `max-width` để ghi đè cho màn hình nhỏ
- VD:
** Mobile-First:
```css
.content { width: 100%; }
@media (min-width: 768px) {
  .content { width: 50%; }
}

** Desktop-First:
```css
.content { width: 50%; }
@media (max-width: 767px) {
  .content { width: 100%; }
}
```

- Tại sao Mobile-First được khuyên dùng? Vì tải ít css hơn cho thiết bị di động, dễ quản lý logic kết thừa từ màn hình nhỏ lên màn hình lớn

CÂU A2:

| Kích thước (pixel) | Thiết bị đại diện | Ví dụ lưới sản phẩm (cột) |
|-------------------|-------------------|---------------------------|
| < 576px           | Điện thoại dọc    | 1 cột                     |
| ≥ 576px           | Điện thoại ngang  | 2 cột                     |
| ≥ 768px           | Máy tính bảng     | 2 hoặc 3 cột              |
| ≥ 992px           | Laptop nhỏ        | 4 cột                     |
| ≥ 1200px          | Desktop           | 4 cột                     |
| ≥ 1400px          | Màn hình lớn      | 4 hoặc 6 cột              |

CÂU A3:

| Chiều rộng màn hình | .container width |
|--------------------|------------------|
| 375px (iPhone SE)  | 100%             |
| 600px              | 540px            |
| 800px              | 720px            |
| 1000px             | 960px            |
| 1400px             | 1140px           |

CÂU A4:
1. Variables ($primary-color): Lưu trữ giá trị để tái sử dụng
- VD: `$primary: #ff0000; .btn { color: $primary; }`
2. Nesting (viết CSS lồng nhau): Viết CSS lồng nhau theo cấu trúc HTML
- VD: `nav { ul { list-style: none; } }`
3. Mixins (@mixin, @include): Nhóm code CSS để dùng lại kèm tham số
- VD: `@mixin flex { display: flex; } .box { @include flex; }`
4. @extend / Inheritance: Kế thừa các thuộc tính từ một selector khác
- VD: `.message { border: 1px solid; } .success { @extend .message; color: green; }`

**Tại sao trình duyệt không đọc được?: Vì trình duyệt chỉ hiểu CSS chuẩn. SCSS là ngôn ngữ tiền xử lý có cú pháp mở rộng
**Cần làm bước gì? Cần biên dịch (compile) bằng công cụ như SASS Compiler để chuyển thành file `.css`

**Lệnh compile SCSS:**
```bash
sass scss/style.scss scss/style.css
```
(Hoặc dùng chế độ --watch để tự động cập nhật: `sass --watch scss/style.scss:scss/style.css`)

### PHẦN C:

CÂU C1:
** Phân tích Layout:
1. Navigation: Trên Desktop là thanh tìm kiếm dài và các danh mục rõ ràng. Trên Mobile chuyền thành Icon Hamburger bên trái và thanh tìm kiếm thu gọn
2. Lưới content: Desktop hiển thị 5-6 sản phẩm. Tablet 3-4 sản phẩm. Mobile chỉ 2 sản phẩm
3. Ẩn/Hiện: Banner quảng cáo lớn cố định 2 bên biến mất trên Mobile. Các menu danh mục chi tiết bên trái cũng bị ẩn
4. Font size: Tiêu đề sản phẩm trên Mobile thường nhỏ hơn và bị cắt bớt để vừa diện tích


