PHẦN A - KIỂM TRA ĐỌC HIỂU
Câu A1:
** 10 input types khác nhau trong HTML5:
1. type="email" - Ô nhập text, tự kiểm tra có @ - Dùng cho form đăng ký
2. type="password" - Ô nhập text, ẩn kí tự - Dùng cho form đăng nhập
3. type="number" - Nút tăng/giảm - Dùng cho đếm số lượng
4. type="tel" - Bàn phím số trên mobile - Dùng để bấm số
5. type="date" - Lịch (Date picker) - Dùng để nhập ngày
6. type="time" - Đồng hồ (Time picker) - Dùng để nhập thời gian
7. type="color" - Bảng chọn màu (Color picker) - Dùng để chọn màu
8. type="range" - Thanh trượt (Slider) - Dùng cho khoảng cách
9. type="checkbox" - Ô chọn có/không - Dùng cho lựa chọn
10. type="hidden" - Không hiển thị - Dùng cho sự riêng tư

Câu A2:
- TH1: Không submit được vì required bắt buộc phải điền, không được để trống
- TH2: Không submit đc vì type="email" bắt buộc phải có ký tự @ và tên miền
- TH3: Không submit đc vì value="15" lớn hơn giới hạn tối đa max="10"
- TH4: Không submit đc vì pattern="[0-9]{10}" bắt buộc nhập đúng 10 chữ số, nhưng user nhập sai định dạng
- TH5: Không submit đc vì minlength="8" bắt buộc tối thiểu 8 ký tự, nhưng user mới nhập 3

Câu A3:
1. <label for>: Nối text với ô input. Giúp máy đọc màn hình (Screen Reader) đọc to tên ô cho người khiếm thị biết để nhập.

2. <fieldset> + <legend>: Dùng để nhóm các input chung một chủ đề (<legend> là tiêu đề nhóm)
Ví dụ: Nhóm chọn giới tính
<fieldset>
    <legend>Giới tính</legend>
    <input type="radio" id="nam"> <label for="nam">Nam</label>
    <input type="radio" id="nu"> <label for="nu">Nữ</label>
</fieldset>

3. - aria-label: Dùng khi nút chỉ có icon, không có chữ
- không nên dùng aria-label khi đã có <label> vì sẽ gây đọc lặp, nhiễu thông tin cho máy đọc

Câu A4:
1. loading="lazy" trên <img>: trì hoãn tải ảnh đến khi gần xuất hiện trên màn hình → giúp trang load nhanh hơn, tiết kiệm băng thông. Không dùng cho ảnh quan trọng (logo, banner, ảnh đầu trang,...)
2. Nên dùng nhiều <source> trong <video>: để đảm bảo video chạy được trên nhiều trình duyệt khác nhau vì mỗi browser hỗ trợ format khác nhau
** Format phổ biến: MP4 (H.264), WebM (VP8/VP9), Ogg (Theora)
3. alt trên <img>: mô tả nội dung ảnh cho screen reader, SEO và khi ảnh bị lỗi
Ví dụ alt đúng:
- Ảnh iPhone 16: alt="iPhone 16 màu đen hiển thị mặt trước"
- Ảnh trang trí: alt="" (bỏ qua cho screen reader)
- Biểu đồ Q1/2026: alt="Biểu đồ doanh thu quý 1 năm 2026 tăng trưởng so với quý 4 năm 2025"

Câu A5:
1. Cách 1 (<img> đơn giản): dùng khi ảnh chỉ mang tính minh hoạ nhanh hoặc không cần mô tả/ghi chú thêm
- VD1: Ảnh icon giỏ hàng trong nút “Mua ngay”
- VD2: Ảnh avatar người dùng trong comment
Cách 2 (<figure> + <figcaption>): dùng khi ảnh có ý nghĩa nội dung + cần chú thích/giá trị bổ sung
VD1: Ảnh sản phẩm trong trang bán hàng kèm tên + giá (như iPhone 16 Pro Max)
VD2: Ảnh biểu đồ thống kê kèm chú thích “Doanh thu Q1/2026 tăng 20% so với Q4/2025”

PHẦN B:
Câu B1:
- HTML thuần không thể validate "Confirm Password" vì HTML thuần chỉ kiểm tra được từng ô nhập liệu riêng lẻ một cách độc lập. Nó không có khả năng so sánh giá trị giữa hai ô input khác nhau. Vì vậy, để kiểm tra hai ô mật khẩu có khớp nhau không, bắt buộc phải dùng JavaScript (===)