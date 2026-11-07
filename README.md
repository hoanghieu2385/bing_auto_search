# Bing Auto Search for Microsoft Rewards

Công cụ tự động tìm kiếm trên Bing để kiếm điểm Microsoft Rewards, chạy hoàn toàn trong trình duyệt.

Dựa trên [gerisonsabino/bing_autosearch](https://github.com/gerisonsabino/bing_autosearch), đã sửa lỗi lưu cài đặt và bổ sung một số tùy chọn.

## Tính năng

- Tự động chạy 5–50 lần tìm kiếm với từ khóa ngẫu nhiên.
- Khoảng nghỉ: 5s, 10s, 15s, 30s, 60s, 2–5 phút, hoặc ngẫu nhiên **10–20s** / 10–60s.
- Chạy trong **một cửa sổ nhỏ duy nhất** ở góc màn hình (chế độ Multi-tab), cần **cho phép pop-up** cho trang; điểm được tính chắc chắn vì Bing chạy với phiên đăng nhập thật.
- Cài đặt được lưu bằng `localStorage`, áp dụng ngay khi đổi (không cần tải lại trang).
- Hiển thị tiến độ trên tiêu đề tab, có đếm ngược và thời gian dự kiến hoàn thành.
- Tự kiểm tra quyền pop-up trước khi chạy và báo nếu chưa được cấp.

## Cách dùng

1. Mở `index.html` bằng Chrome/Edge/Firefox, hoặc host lên GitHub Pages / web server bất kỳ.
2. Đăng nhập sẵn tài khoản Microsoft trong trình duyệt.
3. Mở **Need help? (Tutorial and Settings)** ở cuối trang để chọn số lần tìm và khoảng nghỉ.
4. Bấm **Click to Start Auto Search**.

Nếu chưa có quyền pop-up, bấm vào biểu tượng chặn pop-up trên thanh địa chỉ và chọn "Always allow pop-ups" cho trang này, rồi bấm Start lại.

## Lưu ý

- Đừng đóng tab trong lúc đang chạy; có thể chuyển sang tab khác nhưng trình duyệt có thể làm chậm timer sau vài phút.
- Khi chạy, trang bật **Wake Lock** giữ màn hình luôn sáng (máy tính và điện thoại); bấm Stop hoặc chạy xong là tự tắt, màn hình về chế độ tắt bình thường. Nếu bạn rời trang quá lâu Wake Lock có thể tạm mất, quay lại trang khi đang chạy là tự bật lại.
- Trên điện thoại, ở lần chạy đầu tiên tab của cửa sổ tìm kiếm có thể chiếm màn hình một lần duy nhất khi bấm Start; chỉ cần chuyển về tab chính, các lượt tìm sau chạy dưới nền.
- Dùng có trách nhiệm, tự chịu rủi ro nếu tài khoản bị Microsoft đánh dấu bất thường.

## Giấy phép

MIT — xem [LICENSE](LICENSE).
