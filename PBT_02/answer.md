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
