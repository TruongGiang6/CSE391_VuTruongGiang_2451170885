PHẦN A:
Câu A1:

| Position | Vẫn chiếm chỗ trong flow? | Tham chiếu vị trí | Cuộn theo trang? | Use case |
|---|---:|---|---:|---|
| `static` | Có | Theo flow bình thường của document | Có | Mặc định |
| `relative` | Có | Chính vị trí gốc của nó | Có | Dịch nhẹ element, làm mốc cho absolute con |
| `absolute` | Không | Nearest positioned ancestor (cha có position khác `static`) | Không (gắn vào container) | Lấy phần tử ra khỏi flow, dùng cho popup/tooltip |
| `fixed` | Không | Viewport | Không (cố định) | Header/overlay cố định trên viewport |
| `sticky` | Có (cho đến khi dính) | Nearest scrolling ancestor | Phụ thuộc vào container | Thanh điều hướng dính khi cuộn |


