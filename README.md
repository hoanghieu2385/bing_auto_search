# Bing Auto Search for Microsoft Rewards

Công cụ tự động tìm kiếm trên Bing để kiếm điểm Microsoft Rewards, chạy hoàn toàn trong trình duyệt.

Dựa trên [gerisonsabino/bing_autosearch](https://github.com/gerisonsabino/bing_autosearch), đã sửa lỗi lưu cài đặt và bổ sung một số tùy chọn.

## Tính năng

- Tự động chạy 5–50 lần tìm kiếm với từ khóa ngẫu nhiên.
- Khoảng nghỉ: 10s, 15s, 30s, 60s, 2–5 phút, hoặc ngẫu nhiên **10–20s** / 10–60s.
- Chạy trong **một cửa sổ nhỏ duy nhất** ở góc màn hình (chế độ Multi-tab), cần **cho phép pop-up** cho trang; điểm được tính chắc chắn vì Bing chạy với phiên đăng nhập thật.
- Lập lịch **nối tiếp lượt trước – lượt sau** với độ vênh ngẫu nhiên (±20%), nghỉ dài 60–120s mỗi 8–10 lượt và lệch giờ bấm Start 0–30s → chống dồn dập search khi tab bị ẩn/máy ngủ, khó bị đánh dấu bot hơn.
- Mặc định khoảng nghỉ **10–20s random**; cài 10s cố định cũ của các phiên trước tự đổi sang mặc định mới (một lần duy nhất).
- Cài đặt được lưu bằng `localStorage`, áp dụng ngay khi đổi (không cần tải lại trang).
- Hiển thị tiến độ trên tiêu đề tab; đếm ngược tới lượt kế tiếp và thời gian dự kiến hoàn thành (cả chế độ random).
- Tự kiểm tra quyền pop-up trước khi chạy và báo nếu chưa được cấp.

## Cách dùng

1. Mở `index.html` bằng Chrome/Edge/Firefox, hoặc host lên GitHub Pages / web server bất kỳ.
2. Đăng nhập sẵn tài khoản Microsoft trong trình duyệt.
3. Mở **Need help? (Tutorial and Settings)** ở cuối trang để chọn số lần tìm và khoảng nghỉ.
4. Bấm **Click to Start Auto Search**.

Nếu chưa có quyền pop-up, bấm vào biểu tượng chặn pop-up trên thanh địa chỉ và chọn "Always allow pop-ups" cho trang này, rồi bấm Start lại.

## Lưu ý

- Đừng đóng tab khi đang chạy: trên máy tính, trình duyệt sẽ hỏi xác nhận trước khi tắt/refresh tab để chống bấm nhầm mất trắng (iOS không hỗ trợ hộp thoại này).
- Tab ẩn trong nền lâu, Chrome có thể giãn nhịp timer xuống ~1 lượt/phút; do lập lịch nối tiếp nên các lượt **không bao giờ dồn thành chùm** — chỉ chậm hơn thôi, không điểm nào bị mất vì dồn.
- Khi chạy, trang bật **Wake Lock** giữ màn hình luôn sáng (máy tính và điện thoại Android); bấm Stop hoặc chạy xong là tự tắt, màn hình về chế độ tắt bình thường. Nếu bạn rời trang quá lâu Wake Lock có thể tạm mất, quay lại trang khi đang chạy là tự bật lại.
- **iPhone/iOS:** từ iOS 16.4, Safari và Chrome trên iOS đã hỗ trợ Wake Lock API nên trang dùng API này (iOS 18.4 trở lên hỗ trợ đầy đủ). Chỉ máy iOS cũ hơn mới rơi xuống NoSleep.js (video ẩn) — kém tin cậy hơn; nếu màn hình vẫn tắt, hãy tạm đặt **Cài đặt → Hiển thị & Độ sáng → Auto-Lock → Never** khi chạy. Máy đang dùng cách nào thì xem ở [`wake-test.html`](wake-test.html). Giữ tab chính ở tiền cảnh: iOS tạm dừng tab nền (tab tìm kiếm) nên lượt search có thể bị hoãn tới khi bạn quay lại; đừng chuyển sang app khác giữa lúc chạy.
- **Máy tính và điện thoại chạy khác nhau** (phân biệt theo kiểu nhập liệu, không theo độ rộng màn hình; máy tính bảng cảm ứng chạy như điện thoại):
  - **Máy tính:** chạy ẩn trong một cửa sổ nhỏ ở góc màn hình, dùng lại cửa sổ đó cho mọi lượt nên không chiếm focus; bạn làm việc khác bình thường.
  - **Điện thoại:** bấm Start là mở ngay lượt đầu trong tab mới. Mỗi tab tự đóng khoảng 3 giây sau khi Bing trả trang (chậm nhất 15 giây nếu mạng yếu), bạn quay về tab chính để xem số lượt và đếm ngược, hết khoảng nghỉ thì tab mới tự mở. Cần **cho phép pop-up**, nếu bị chặn thì app dừng và báo. Trên iPhone, Safari có thể tạm dừng tab chính khi nó nằm nền (chưa kiểm trên máy thật); khi đó tab tìm kiếm chỉ đóng lúc bạn tự quay lại tab chính.
- Dùng có trách nhiệm, tự chịu rủi ro nếu tài khoản bị Microsoft đánh dấu bất thường.

## Giấy phép

MIT — xem [LICENSE](LICENSE).
