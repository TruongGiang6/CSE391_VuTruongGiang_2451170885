PHẦN A:
Câu A1:

| Position | Vẫn chiếm chỗ trong flow? | Tham chiếu vị trí | Cuộn theo trang? | Use case |
|---|---:|---|---:|---|
| `static` | Có | Normal flow | Có | Mặc định |
| `relative` | Có | Chính phần tử (flow) | Có | Dịch vị trí nhưng vẫn giữ chỗ |
| `absolute` | Không | Nearest positioned ancestor (cha có position khác `static`) | Không (gắn vào container) | Lấy phần tử ra khỏi flow, dùng cho popup/tooltip |
| `fixed` | Không | Viewport | Không (cố định) | Header/overlay cố định trên viewport |
| `sticky` | Có (cho đến khi dính) | Nearest scrolling ancestor | Phụ thuộc vào container | Thanh điều hướng dính khi cuộn |

---

Ngắn gọn về cú pháp: dùng dấu `|` để phân tách cột và hàng tiêu đề cần một hàng phân cách (ví dụ `---` hoặc `:---:` để căn trái/giữa/phải`).


