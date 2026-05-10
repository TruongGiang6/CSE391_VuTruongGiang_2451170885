PHẦN A:
Câu A1:
| Position | Vẫn chiếm chỗ trong flow? | Tham chiếu vị trí | Cuộn theo trang? | Use case |
|---|---|---|---|---|
| `static` | Có | Theo flow bình thường của document | Có | Theo flow bình thường của document |
| `relative` | Có | Chính vị trí gốc của nó | Có | Dịch nhẹ element, làm mốc cho absolute con |
| `absolute` | Không | nearest positioned ancestor (parent gần nhất có position != static), nếu không có thì theo viewport/html | Không cố định, cuộn cùng page | Không cố định, cuộn cùng page |
| `fixed` | Không | Viewport (màn hình trình duyệt) | Không (cố định) | Navbar cố định, nút chat, back-to-topHeader/overlay cố định trên viewport |
| `sticky` | Có | Nearest scrolling ancestor | Phụ thuộc vào container | Header dính, menu dính khi scroll |


