## So sánh: Chrome Password Manager vs Bitwarden

### Bảng so sánh

| Tiêu chí | Google Chrome | Bitwarden |
| :--- | :--- | :--- |
| **Khả năng chống Infostealer** | Yếu. Mật khẩu lưu trong file `Login Data`. Infostealer chạy với quyền User là giải mã được qua DPAPI và lấy hết mật khẩu. | Mạnh. Vault mã hóa AES-256. Lấy được file vault cũng chỉ là dữ liệu mã hóa, không có Master Password thì không đọc được. |
| **Zero-Knowledge Architecture** | Không có. Google nắm khóa và có khả năng giải mã. | Có. Bitwarden không lưu và không biết Master Password. Chỉ bạn mới giải mã được vault. |
| **Đồng bộ chéo nền tảng** | Chỉ tốt trong hệ sinh thái Google. Yếu khi dùng ngoài Chrome. | Tốt. Đồng bộ trên Windows, macOS, Linux, iOS, Android, mọi trình duyệt, App, CLI. |

### Tại sao Bitwarden thắng thế?

**1. Chrome tiện nhưng trần trụi**
- Chrome tự động điền vì đã giải mã sẵn cho User đang đăng nhập.
- Infostealer cũng là User đó, nên cũng hưởng sự tiện lợi đó.

**2. Bitwarden thêm 1 lớp khóa**
- Vault luôn ở trạng thái khóa.
- Chỉ khi nhập đúng Master Password, vault mới được giải mã tạm thời trong RAM.
- Infostealer quét ổ cứng sẽ không lấy được gì hữu ích.

**3. Chia tách rủi ro**
- Với Chrome: Hack 1 máy là lấy hết mật khẩu.
- Với Bitwarden: Hack 1 máy chưa đủ, còn phải có thêm Master Password, mà Master Password không hề lưu trên máy.

**Kết luận:** Chrome tối ưu cho tốc độ. Bitwarden tối ưu cho an toàn. Với yêu cầu chống Infostealer, phải chọn Bitwarden.
