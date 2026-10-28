# xKuro Wallet

Giao diện tham khảo cho trang web **xKuro Wallet**, viết bằng HTML/CSS/JavaScript thuần, chạy trên GitHub Pages. Không dùng framework, không cần cài đặt hay build.

## Xem trực tiếp

| Trang | Link |
|---|---|
| Trang chủ | https://xkurexsdev.github.io/ |
| Trình kiểm tra số dư | https://xkurexsdev.github.io/xkurochianlink/balance.html |
| Kết quả tra cứu | https://xkurexsdev.github.io/xkurochianlink/result.html |

## Nội dung

- **Trang chủ** (`index.html`): màn hình mở đầu với ảnh nền, logo, tên thương hiệu và hai ô nhập. Bố cục dựng theo thiết kế Figma, co giãn theo chiều rộng màn hình.
- **Trình kiểm tra số dư** (`xkurochianlink/balance.html`): form gồm Blockchain, Địa chỉ ví, Crypto và bộ lọc theo thời gian hoặc theo khối. Nút Search chỉ bật khi đã điền đủ các mục. Với chuỗi EVM (Ethereum, BNB Chain, Polygon, Arbitrum), địa chỉ phải đúng định dạng `0x` kèm 40 ký tự hex.
- **Kết quả tra cứu** (`xkurochianlink/result.html`): trang đích sau khi gửi form, hiện lại thông tin đã nhập, số dư và lịch sử số dư.

Trên trang kiểm tra số dư có nút **"Điền dữ liệu mẫu"** để thử nhanh toàn bộ luồng.

## Lưu ý

- Số dư và lịch sử trên trang kết quả là **dữ liệu minh họa**, được tạo từ thông tin bạn nhập. Dự án **chưa kết nối với dữ liệu blockchain thật**.
- Thông tin nhập vào form chỉ được lưu tạm trong trình duyệt (`sessionStorage`) để chuyển sang trang kết quả. Không có gì được gửi tới máy chủ.
- Đây là dự án giao diện để tham khảo. Đừng nhập khóa riêng tư, cụm từ khôi phục hay bất kỳ thông tin bí mật nào vào các ô nhập.

## Cấu trúc thư mục

```
.
├── index.html               # Trang chủ
├── images/
│   ├── hero-bg.jpg          # Ảnh nền
│   └── logo.jpg             # Logo xKuro
├── xkurochianlink/
│   ├── balance.html         # Trình kiểm tra số dư
│   └── result.html          # Kết quả tra cứu
└── README.md
```

## Chạy trên máy

Chỉ cần phục vụ thư mục này bằng một máy chủ tĩnh bất kỳ, ví dụ:

```bash
python3 -m http.server 8000
```

Rồi mở http://localhost:8000.

## Công nghệ

- HTML, CSS (đơn vị `cqw` để co giãn theo khung), JavaScript thuần
- Font [Inter](https://fonts.google.com/specimen/Inter) từ Google Fonts
