PHẦN A:
Câu A1 (5đ) — HTTP & Browser (chương 01 - 01_introduction_html_universe.md)
1. Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, 5 bước xảy ra là:
- B1: Gửi Request qua hạ tầng mạng (DNS Lookup)
- B2: Server tiếp nhận và xử lý
- B3: Trả về Response
- B4: Phân tích cấu trúc (Parse HTML & CSS)
- B5: Thực thi và hiển thị (Execute JS & Render)
(Cuộc Hành Trình 0.3 Giây Xuyên Đại Dương/ Browser Rendering — Từ Code thành Hình ảnh)
2. Trong DevTools của Chrome, tab Network cho thấy các yêu cầu (requests) và phản hồi (responses) giữa trình duyệt và máy chủ
(4.3. Developer Tools (F12) — "Kính hiển vi" cho website)
![alt text](A1.PNG)

Câu A2 — Semantic HTML
- Trang web bị Google đánh giá SEO thấp vì trang web trên mắc lỗi "Div Soup". Google và các công cụ tìm kiếm sử dụng các robot crawler để đọc mã nguồn, khi dùng <div> cho mọi thứ, robot không thể phân biệt được đâu là phần đầu, đâu là nội dung chính, hay đâu là một sản phẩm cụ thể. ("Dùng đúng thẻ = Google hiểu nội dung = SEO tốt hơn." > ❌ "Div Soup" — Google không hiểu gì.")
** 4 lỗi semantic: 
1. <div class="header"> -> <header>
2. <div class="menu"> -> <nav>
3. <div class="main"> -> <main>
4. <div class="product"> -> <article>

<header>
    <div class="logo">ShopTLU</div>
    <nav>
        <div><a href="/">Trang chủ</a></div>
        <div><a href="/products">Sản phẩm</a></div>
    </nav>
</header>
<main>
    <article>
        <div class="title">iPhone 16 Pro</div>
        <div class="price">25.990.000đ</div>
        <div class="image"><img src="iphone.jpg"></div>
    </article>
</main>
<div class="footer">© 2026 ShopTLU</div>

Câu A3 — Block vs Inline
** Text Art: 
 Hộp 1                                             
 Text AText B                                      
 Hộp 2                                             
 Text CText D                                      
 Hộp 3
** Giải thích:
+<div>Hộp 1</div>,<div>Hộp 2</div>,<div>Hộp 1</div>: Là 1 block, chiếm riêng 1 dòng
+<span>Text A</span> <span>Text B</span>, <span>Text C</span> <strong>Text D</strong>: là inline, nằm cạnh nhau 

Câu A4 — Table
** Sự khác nhau giữa <thead>, <tbody>, <tfoot>:
- <thead> (Table Header): chứa các tiêu đề của cột (thường dùng kết hợp với thẻ <th>)
- <tbody> (Table Body): chứa nội dung dữ liệu chính của bảng
- <tfoot> (Table Footer): chứa thông tin tổng kết hoặc chú thích cuối bảng
** KHÔNG NÊN dùng table để tạo layout trang web vì:
1. Sai mục đích Semantic: nếu dùng để chia bố cục trang web (header, sidebar, footer), các công cụ tìm kiếm sẽ không hiểu được đâu là nội dung chính, dẫn đến SEO cực kỳ kém
2. Không linh hoạt: bảng có cấu trúc rất cứng nhắc. Khi xem trên điện thoại di động (màn hình nhỏ), một layout bằng table sẽ bị vỡ vụn hoặc bị tràn màn hình, rất khó để thu gọn hay sắp xếp lại
3. Tốc độ tải trang chậm: trình duyệt thường phải đợi tải xong toàn bộ code của thẻ <table> thì mới bắt đầu tính toán để hiển thị ra màn hình. Nếu layout trang web phức tạp với nhiều bảng lồng nhau, người dùng sẽ thấy một trang trắng tinh trong thời gian dài trước khi nội dung hiện ra

PHẦN B:
Câu B3 - Debug HTML
- Lỗi 1: Dòng 1 - <!DOCTYPE> thiếu html - thêm html
- Lỗi 2: Dòng 2 - html thiếu lang = "vi" - thêm lang = "vi"
- Lỗi 3: Dòng 4 - Thẻ title chưa có đóng - Thêm thẻ đóng </title>
- Lỗi 4: Dòng 5 - Giá trị charset sai - Sửa thành UTF-8
- Lỗi 5: Dòng 8 - Thẻ đóng h1 sai - Sửa thành </h1>
- Lỗi 6: Dòng 12 - Thẻ đóng a sai - Sửa thành </a>
- Lỗi 7: Dòng 20 - Thẻ <img> thiếu dấu "" và thiếu alt — Sửa thành <img src="iphone.jpg" alt="Hình ảnh iPhone">
- Lỗi 8: Dòng 22 - Sai vị trí thẻ đóng </b> - Thay vị trí thành <p>Giá: <b>25.990.000đ</b></p>
- Lỗi 9 Dòng 40 - Thừa 1 thẻ <main></main> - Thay thành <aside></aside>
- Lỗi 10: Dòng 45 - Thẻ p chưa đóng - Thêm </p>
- Lỗi 11: Dưới dòng 47 - Thiếu thẻ đóng html - Thêm </html>

Câu B4 - Phân tích trang web thật (Shopee)
1. ![alt text](B4.1.png)
** 3 thẻ Semantic được sử dụng đúng:
- Thẻ <header class="shopee-top...">: Nằm ở đầu trang chứa logo, thanh tìm kiếm
- Thẻ <footer role="contentinfo"...>: Nằm ở cuối trang chứa thông tin bản quyền, liên hệ
- Thẻ <section class="G9LJCq"...>: Dùng để phân chia một khu vực chức năng riêng biệt trên trang, cụ thể ở trang này là khu vực chứa form đăng nhập/đăng ký
** 1 thẻ lạm dụng:
- Dùng <div id="main"> thay vì thẻ <main>: Dùng để bọc toàn bộ nội dung chính của trang
2. ![alt text](B4.2.png)
- Bảng này hiển thị thông tin "Hướng Dẫn Chọn Size" của một sản phẩm thời trang. Nó chứa các số đo tương ứng với từng kích cỡ, giúp người mua đối chiếu và lựa chọn size
- Có dùng <thead>, <tbody>: <thead> dùng để chứa hàng tiêu đề trên cùng, <tbody> dùng để bọc toàn bộ các hàng
3. ![alt text](B4.3.png) (ô tìm kiếm)
- Form đó có action và method không?
    + Nhìn vào code: <form role="search" autocomplete="off" class="shopee-searchbar...">, ta thấy form này không khai báo hai thuộc tính action và method

- Input types nào được dùng?
    + Thẻ nhập liệu chính có mã code: <input aria-label="..." class="shopee-searchbar-input__input" maxlength="128" placeholder="GALAXY A57 | A37 5G" autocomplete="off"... role="combobox">
    + Code không ghi rõ thuộc tính type. Theo chuẩn HTML5, khi thẻ <input> bị khuyết thuộc tính này, trình duyệt sẽ tự động nhận diện mặc định đây là ô nhập văn bản: type="text"

PHẦN C:
Câu C1:
<!DOCUMENT html>
<html lang="vi">