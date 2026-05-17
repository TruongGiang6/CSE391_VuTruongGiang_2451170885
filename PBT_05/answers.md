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