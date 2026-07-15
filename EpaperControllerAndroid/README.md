# Ứng dụng Android Điều khiển E-Paper

Dự án này đóng gói giao diện HTML tiếng Việt thành ứng dụng Android.

## Vì sao ứng dụng mở Chrome?

Giao diện gốc sử dụng **Web Bluetooth** (`navigator.bluetooth`). Android WebView thường không hỗ trợ đầy đủ API này. Ứng dụng vì vậy chạy giao diện từ máy chủ nội bộ `http://127.0.0.1` rồi mở bằng Chrome. `localhost` được Chrome xem là ngữ cảnh an toàn, phù hợp để gọi Web Bluetooth.

## Build APK bằng Android Studio

1. Cài Android Studio bản mới.
2. Chọn **Open** và mở thư mục `EpaperControllerAndroid`.
3. Chờ Gradle Sync hoàn tất.
4. Chọn **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. APK debug nằm tại `app/build/outputs/apk/debug/app-debug.apk`.
6. Chép APK sang điện thoại Android và cài đặt.

## Sử dụng

1. Bật Bluetooth và Vị trí trên điện thoại.
2. Mở ứng dụng **Điều khiển E-Paper**.
3. Giao diện sẽ mở trong Chrome.
4. Bấm **Quét thiết bị** và cho phép quyền Bluetooth khi Chrome hỏi.

## Yêu cầu

- Android 8.0 trở lên.
- Google Chrome hoặc trình duyệt Android hỗ trợ Web Bluetooth.
- Internet chỉ cần khi dùng thư viện QR tải từ CDN; các chức năng chính chạy từ file nội bộ.
