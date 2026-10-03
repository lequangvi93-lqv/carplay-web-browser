# CarPlay Web Browser (Trình Duyệt Web Đồ Họa Đầy Đủ Cho CarPlay)

Dự án ứng dụng iOS & CarPlay cung cấp **Trình Duyệt Web Đồ Họa Tương Tác Đầy Đủ (`WKWebView`)** hiển thị trực tiếp trên màn hình CarPlay của xe ô tô.

---

## 🌟 Tính Năng Nổi Bật

1. **Hiển thị đồ họa trực tiếp trên màn hình CarPlay:**
   - Trình duyệt web full màn hình với khả năng tương tác cảm ứng.
   - Thanh công cụ điều hướng: Back (⏮), Forward (⏭), Reload (🔄), Trang chủ (🏠).
   - Thanh địa chỉ URL & Tìm kiếm Google tích hợp ngay trên xe.
   - Bảng truy cập nhanh các trang web phổ biến (Google, YouTube, VnExpress, Dân Trí, Zing MP3, Google Maps...).

2. **Bộ điều khiển từ xa & Bàn phím trên iPhone:**
   - Khi cắm iPhone vào xe, bạn hoặc người ngồi bên cạnh có thể nhập nhanh URL/từ khóa trên bàn phím iPhone.
   - Nhấn "Mở Trên Xe" để gửi ngay địa chỉ web sang màn hình CarPlay.

---

## 📁 Cấu Trúc Mã Nguồn (Swift / SwiftUI)

```text
carplay-web-browser/
└── CarPlayWebBrowser/
    ├── CarPlayWebBrowserApp.swift        # Entry point của ứng dụng iOS & đăng ký CarPlay Scene
    ├── CarPlaySceneDelegate.swift        # Quản lý kết nối UIWindow tới màn hình xe CarPlay
    ├── WebBrowserCarViewController.swift # Controller chứa WKWebView đồ họa hiển thị trên xe
    ├── iPhoneWebControlView.swift        # Giao diện điều khiển từ xa & bàn phím trên iPhone
    ├── Info.plist                        # Phân giải và cấu hình CPTemplateApplicationScene
    └── CarPlayWebBrowser.entitlements    # Khai báo quyền tương thích CarPlay
```

---

## 🛠️ Hướng Dẫn Biên Dịch & Thử Nghiệm

### 1. Thử nghiệm trên Xcode Simulator (macOS)
1. Mở Xcode, tạo một dự án iOS App tên `CarPlayWebBrowser`.
2. Sao chép các tệp mã nguồn trong thư mục này vào dự án.
3. Chọn thiết bị chạy là **iPhone 15 Pro (Simulator)**.
4. Chạy ứng dụng (`Cmd + R`).
5. Trên cửa sổ Simulator, chọn menu **`I/O` -> `External Displays` -> `CarPlay`**.
6. Cửa sổ màn hình xe CarPlay sẽ xuất hiện độc lập, hiển thị giao diện trình duyệt web đồ họa đầy đủ!

### 2. Cài đặt lên iPhone Thực tế (Để dùng trên Xe)
Do quy định kiểm duyệt của Apple không cho phép duyệt web thông thường khi lái xe, đối với xe thực tế bạn có các cách triển khai sau:

- **Cách 1 (Developer Mode / Xcode Sideloading):** 
  Kết nối iPhone vào máy tính, nạp trực tiếp ứng dụng qua Xcode bằng tài khoản Developer cá nhân. Đánh dấu Tin cậy nhà phát triển trong cài đặt iPhone (`Settings -> General -> VPN & Device Management`).
- **Cách 2 (Cài qua TrollStore / AltStore / Sideloadly):**
  Xuất file `.ipa` từ Xcode và cài đặt lên máy mà không lo bị thu hồi chứng chỉ.
- **Cách 3 (CarBridge / CarPay Tweak - Dành cho máy có TrollStore / Jailbreak):**
  Sử dụng CarBridge để mở rộng toàn bộ màn hình trình duyệt ứng dụng lên CarPlay với độ phân giải và tỉ lệ chuẩn của màn hình xe.

---

## 🔒 Lưu Ý An Toàn
Ứng dụng được thiết kế cho mục đích giải trí và tra cứu khi xe dừng đậu hoặc do hành khách thao tác. Vui lòng tập trung lái xe an toàn khi di chuyển trên đường.
