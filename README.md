# EV Smart Parking — Web Dashboard

Trang web điều khiển và giám sát hệ thống khóa giữ chỗ sạc xe điện.

## Các trang

| File | Mô tả | QR tại |
|---|---|---|
| `index.html` | Trang điều khiển ô sạc #01 (hạ/nâng khóa) | Dán tại ô đỗ xe |
| `overview.html` | Dashboard tổng quan 8 ô đỗ | Dán tại cổng vào bãi |

## Hướng dẫn deploy lên GitHub Pages (5 phút)

### Bước 1 — Tạo repository trên GitHub

1. Vào https://github.com → nhấn **New repository**
2. Đặt tên repo: `ev-parking` (hoặc tên tùy ý)
3. Chọn **Public**
4. Nhấn **Create repository**

### Bước 2 — Upload file

1. Trong repo vừa tạo, nhấn **Add file → Upload files**
2. Kéo thả 3 file: `index.html`, `overview.html`, `README.md`
3. Nhấn **Commit changes**

### Bước 3 — Bật GitHub Pages

1. Vào **Settings** → **Pages** (menu bên trái)
2. Mục **Source**: chọn **Deploy from a branch**
3. Branch: chọn **main**, folder: **/ (root)**
4. Nhấn **Save**
5. Chờ ~2 phút → GitHub sẽ hiện link dạng:
   `https://TEN_BAN.github.io/ev-parking/`

### Bước 4 — Lấy link cố định

Sau khi deploy xong, hai link cố định vĩnh viễn là:

```
https://TEN_BAN.github.io/ev-parking/index.html
https://TEN_BAN.github.io/ev-parking/overview.html
```

### Bước 5 — Tạo QR code

Dùng một trong các trang sau để tạo QR **miễn phí, không hết hạn**:

- https://qr.io (không cần đăng ký)
- https://www.qrcode-monkey.com (tùy chỉnh màu sắc, logo)
- https://goqr.me

Nhập link `index.html` → tải QR về → in và dán tại ô đỗ xe.

---

## Cấu hình Blynk

Token và Virtual Pin được khai báo trong từng file HTML:

**index.html** — điều khiển ô sạc #01:
```
Token: N7OFNh5W2bXFpSDSCxZQjLaaL64z9GCi
V0: Trạng thái tổng hợp
V1: Khoảng cách (cm)
V2: Có xe (0/1)
V3: Đang sạc (0/1)
V6: Trạng thái khóa
V7: Vi phạm
V8: An toàn
V9: Lệnh hạ khóa (ghi 1 để hạ)
```

**overview.html** — dashboard tổng quan:
```
Token: 8kMyasAuHrqFZRGrk_dA-K4VJI1i6EIN
V2: Trạng thái ô 1 (thời gian thực)
Ô 2-8: Dữ liệu mô phỏng (demo)
```
