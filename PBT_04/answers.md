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
- TH1: bố cục gồm 1 hàng ngang, 4 cột chia đều nhau
  [ Item 1 ] [ Item 2 ] [ Item 3 ] [ Item 4 ]

- TH2: 
  [      Item 1      ] [      Item 2      ]
  [      Item 3      ] [      Item 4      ]
  [      Item 5      ] [      Item 6      ]
  
- TH3: 

- TH4: 

- TH5: