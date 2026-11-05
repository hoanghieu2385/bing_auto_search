# Bing Auto Search for Microsoft Rewards

Công cụ tự động tìm kiếm trên Bing để kiếm điểm Microsoft Rewards, chạy hoàn toàn trong trình duyệt.

Dựa trên [gerisonsabino/bing_autosearch](https://github.com/gerisonsabino/bing_autosearch), đã sửa lỗi lưu cài đặt và bổ sung một số tùy chọn.

## Tính năng

- Tự động chạy 5–50 lần tìm kiếm với từ khóa ngẫu nhiên.
- Khoảng nghỉ: 5s, 10s, 15s, 30s, 60s, 2–5 phút, hoặc ngẫu nhiên **10–20s** / 10–60s.
- Hai chế độ chạy:
  - **Iframe (mặc định)**: chạy ẩn trong trang, không cần quyền pop-up.
  - **Multi-tab**: mỗi lần tìm mở một tab thật rồi tự đóng. Cần **cho phép pop-up** cho trang.
- Cài đặt được lưu bằng `localStorage`, áp dụng ngay khi đổi (không cần tải lại trang).
- Hiển thị tiến độ trên tiêu đề tab, có đếm ngược và thời gian dự kiến hoàn thành.
- Tự kiểm tra quyền pop-up trước khi chạy Multi-tab và báo nếu chưa được cấp.

## Cách dùng

1. Mở `index.html` bằng Chrome/Edge/Firefox, hoặc host lên GitHub Pages / web server bất kỳ.
2. Đăng nhập sẵn tài khoản Microsoft trong trình duyệt.
3. Mở **Need help? (Tutorial and Settings)** ở cuối trang để chọn số lần tìm, khoảng nghỉ và chế độ chạy.
4. Bấm **Click to Start Auto Search**.

Nếu chọn Multi-tab, bấm vào biểu tượng chặn pop-up trên thanh địa chỉ và chọn "Always allow pop-ups" cho trang này, rồi bấm Start lại.

## Lưu ý

- Chế độ iframe có thể **không được tính điểm** nếu trình duyệt chặn cookie bên thứ ba (Bing không thấy phiên đăng nhập). Muốn chắc ăn thì dùng Multi-tab.
- Đừng đóng tab trong lúc đang chạy; có thể chuyển sang tab khác nhưng trình duyệt có thể làm chậm timer sau vài phút.
- Dùng có trách nhiệm, tự chịu rủi ro nếu tài khoản bị Microsoft đánh dấu bất thường.

## Giấy phép

MIT — xem [LICENSE](LICENSE).
