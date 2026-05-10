PHẦN A:
Câu A1:

| Position | Vẫn chiếm chỗ trong flow? | Tham chiếu vị trí | Cuộn theo trang? | Use case |
|---|---|---|---|---|
| `static` | Có | Theo flow bình thường của document | Có | Theo flow bình thường của document |
| `relative` | Có | Chính vị trí gốc của nó | Có | Dịch nhẹ element, làm mốc cho absolute con |
| `absolute` | Không | nearest positioned ancestor (parent gần nhất có position != static), nếu không có thì theo viewport/html | Không cố định, cuộn cùng page | Không cố định, cuộn cùng page |
| `fixed` | Không | Viewport (màn hình trình duyệt) | Không (cố định) | Navbar cố định, nút chat, back-to-topHeader/overlay cố định trên viewport |
| `sticky` | Có | Nearest scrolling ancestor | Phụ thuộc vào container | Header dính, menu dính khi scroll |

** Khi nào absolute tham chiếu body? 
- Khi nó không có bất kỳ thẻ cha/tổ tiên nào được set position khác static

** Khi nào tham chiếu parent? 
- Khi thẻ parent đó được set position khác static

** "Nearest positioned ancestor" là gì? 
- Là thẻ cha hoặc tổ tiên gần nhất có thuộc tính position khác static
  
Câu A2:
- TH1: bố cục gồm 1 hàng ngang (display: flex), 4 item chia đều nhau (flex: 1)

+---------------------------------------------------+
|  [Item 1]  |  [Item 2]  |  [Item 3]  |  [Item 4]  |
+---------------------------------------------------+

- TH2: mỗi item chiếm tổng cộng 50% không gian (45% width + 2.5% margin trái + 2.5% margin phải). Do có flex-wrap: wrap, các item tự động xuống dòng, tạo thành lưới 3 hàng, 2 cột

+---------------------------------------+
|  [ Item 1 ] (2.5%) [ Item 2 ]         | 
|                                       |
|  [ Item 3 ]        [ Item 4 ]         | 
|                                       |
|  [ Item 5 ]        [ Item 6 ]         | 
+---------------------------------------+

- TH3: gồm 1 hàng ngang. Item 1 dính sát mép trái, Item 3 dính sát mép phải, Item 2 nằm chính giữa (space-between). Tất cả được căn giữa theo chiều dọc (align-items: center)

+--------------------------------------------------------+
| [Item 1]               [Item 2]               [Item 3] |
+--------------------------------------------------------+

- TH4: dạng lưới (display: grid) gồm 1 hàng, 3 cột. Cột hai bên có kích thước cố định là 200px, cột ở giữa chiếm toàn bộ không gian còn lại (1fr)

+--------------------------------------------------------+
| [ Item 1 ] |         [ Item 2]             | [ Item 3] |
+--------------------------------------------------------+

- TH5: lưới gồm 3 cột bằng nhau (repeat(3, 1fr)). Do có 7 item nên sẽ tạo thành 3 hàng. Item cuối cùng (thứ 7) bị đẩy xuống hàng thứ 3 và nằm ở vị trí cột đầu tiên bên trái

+-------------------------------------------------------+
|  [ Item 1 ]  |  [ Item 2 ]  |  [ Item 3 ] |           |
|                                                       |
|  [ Item 4 ]  |  [ Item 5 ]  |  [ Item 6 ] |           |
|                                                       |
|  [ Item 7 ]  |              |             |           |
+-------------------------------------------------------+