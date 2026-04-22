PHẦN A:
Câu A1 (5đ) — HTTP & Browser (chương 01 - 01_introduction_html_universe.md)
1. Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, 5 bước xảy ra là:
- B1: Gửi Request qua hạ tầng mạng (DNS Lookup). D/c
- B2: Server tiếp nhận và xử lý.
- B3: Trả về Response.
- B4: Phân tích cấu trúc (Parse HTML & CSS).
- B5: Thực thi và Hiển thị (Execute JS & Render).
(Cuộc Hành Trình 0.3 Giây Xuyên Đại Dương/ Browser Rendering — Từ Code thành Hình ảnh)
2. Trong DevTools của Chrome, tab Network cho thấy các yêu cầu (requests) và phản hồi (responses) giữa trình duyệt và máy chủ
(4.3. Developer Tools (F12) — "Kính hiển vi" cho website)
![alt text](A1.PNG)

Câu A2 — Semantic HTML
- Trang web bị Google đánh giá SEO thấp vì trang web trên mắc lỗi "Div Soup" (Lạm dụng thẻ <div>). Google và các công cụ tìm kiếm sử dụng các robot (crawler) để đọc mã nguồn, khi dùng <div> cho mọi thứ, robot không thể phân biệt được đâu là phần đầu, đâu là nội dung chính, hay đâu là một sản phẩm cụ thể. ("Dùng đúng thẻ = Google hiểu nội dung = SEO tốt hơn." > ❌ "Div Soup" — Google không hiểu gì.")
** 4 lỗi semantic: 
1. <div class="header"> -> <header>
2. <div class="menu"> -> <nav>
3. <div class="main"> -> <main>
4. <div class="product"> -> <article>

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
- Lỗi 9: Dòng 40 - Thừa 1 thẻ <main></main> - Thay thành <aside></aside>
- Lỗi 10: Dòng 45 - Thẻ p chưa đóng - Thêm </p>
- Lỗi 11: Dưới dòng 47 - Thiếu thẻ đóng html - Thêm </html>