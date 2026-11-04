# 🚀 MVP Features & Impact-Effort Matrix — Hydra Tracker

> Tài liệu định nghĩa danh mục tính năng cho phiên bản khả dụng tối thiểu (Minimum Viable Product - MVP), lập luận tính cấp thiết và ma trận ưu tiên Impact-Effort làm căn cứ phân bổ công việc trên GitHub Scrum Board.

---

## 1. Triết lý xác định MVP

Theo nguyên lý Lean Startup (Khởi nghiệp tinh gọn), phiên bản MVP của **Hydra Tracker** không cố gắng ôm đồm mọi tính năng, mà tập trung giải quyết bài toán cốt lõi duy nhất với chất lượng xuất sắc: **Giúp người dùng ghi nhận nước uống nhanh nhất và duy trì động lực liên tục.**

Mọi tính năng nâng cao (như tích hợp cảm biến bình nước thông minh, phân tích thời tiết qua GPS, mạng xã hội bạn bè) đều được hoãn lại ở các phiên bản sau để đảm bảo MVP ra mắt nhanh, nhẹ và mượt mà.

---

## 2. Chi tiết 6 tính năng cốt lõi của MVP & Lập luận nghiệp vụ

### 🔹 Feature 1: Onboarding & Tính toán Mục tiêu Cá nhân (Dynamic Goal Setup)
- **Mô tả:** Luồng giới thiệu ban đầu thu thập 3 thông số cơ bản: Cân nặng (kg), Giới tính, Mức độ vận động (Ít / Vừa phải / Thường xuyên). Hệ thống tự động áp dụng công thức y học khuyến nghị để đưa ra mục tiêu lượng nước hàng ngày (ml/ngày), đồng thời cho phép người dùng tự điều chỉnh nếu có chỉ định riêng từ bác sĩ.
- **Công thức tham chiếu:**
  $$\text{Lượng nước (ml)} = (\text{Cân nặng (kg)} \times 35) + (\text{Phút tập luyện} \times 12)$$
- **Lập luận chọn vào MVP:** Nếu không có mục tiêu cá nhân rõ ràng ngay từ đầu, mọi thao tác ghi nhận sau đó đều trở nên vô nghĩa vì người dùng không biết mình đã uống đủ hay thiếu.

### 🔹 Feature 2: Ghi nhận 1-Chạm (1-Tap Quick Logging)
- **Mô tả:** Trên màn hình chính, bố trí các biểu tượng cốc nước phổ biến với dung tích chuẩn định sẵn:
  - Cốc nhỏ: **200 ml** (Tương đương tách trà/cà phê)
  - Cốc vừa: **350 ml** (Cốc thủy tinh gia đình/văn phòng)
  - Chai nước: **500 ml** (Chai nước suối tiêu chuẩn)
  - Nút cộng tùy chỉnh: Cho phép nhập số ml bất kỳ khi cần.
  - Người dùng chỉ cần chạm 1 lần vào biểu tượng cốc $\rightarrow$ Hệ thống ghi nhận ngay kèm hoạt ảnh sóng nước dâng lên và phản hồi rung nhẹ (Haptic feedback).
- **Lập luận chọn vào MVP:** Đây chính là **Unique Value Proposition (UVP)** cốt lõi của Hydra Tracker. Đây là tính năng được dùng nhiều lần nhất trong ngày.

### 🔹 Feature 3: Vòng tròn Tiến độ Trực quan (Visual Daily Progress Ring)
- **Mô tả:** Màn hình chính hiển thị một vòng tròn nước lớn (Progress Ring) thể hiện phần trăm mục tiêu đã đạt được trong ngày (ví dụ: `1500 / 2200 ml - 68%`). Màu sắc và mực nước bên trong vòng tròn sẽ tự động dâng lên tương ứng với lượng nước đã nạp.
- **Lập luận chọn vào MVP:** Cung cấp phản hồi thị giác tức thì (Instant Visual Feedback), tạo cảm giác thỏa mãn và thôi thúc người dùng hoàn thành nốt phần trăm còn lại trước khi kết thúc ngày.

### 🔹 Feature 4: Lịch Nhắc nhở Thông minh (Smart Interval Reminders)
- **Mô tả:** Cho phép người dùng bật thông báo nhắc nhở tự động theo chu kỳ (mỗi 1 giờ, 1.5 giờ, 2 giờ) trong khoảng thời gian thức (mặc định: `07:30 - 22:00`). Tự động tắt âm và ngừng gửi thông báo vào ban đêm để không làm phiền giấc ngủ.
- **Lập luận chọn vào MVP:** Hơn 75% người dùng không uống đủ nước là do "quên". Không có nhắc nhở, ứng dụng sẽ nhanh chóng bị lãng quên trong danh sách ứng dụng của điện thoại.

### 🔹 Feature 5: Thống kê & Lịch sử Theo Ngày/Tuần (Basic Daily/Weekly Analytics)
- **Mô tả:** Biểu đồ cột thể hiện lượng nước uống trong 7 ngày gần nhất so với đường mục tiêu chuẩn (Target line). Cho phép xem lại lịch sử các lần uống trong ngày (mấy giờ, bao nhiêu ml) và có nút xóa nếu lỡ tay bấm nhầm.
- **Lập luận chọn vào MVP:** Giúp người dùng nhìn thấy bức tranh tổng thể về thói quen của mình trong cả tuần, nhận biết ngày nào mình thường lười uống nước (ví dụ: cuối tuần) để tự điều chỉnh.

### 🔹 Feature 6: Bộ đếm Chuỗi ngày & Hiệu ứng Chúc mừng (Streak & Milestone Celebration)
- **Mô tả:** 
  - Khi đạt 100% mục tiêu ngày: Màn hình bắn pháo hoa confetti chúc mừng và tăng chuỗi ngày thành công (Streak +1).
  - Hiển thị huy hiệu chuỗi ngày kiên trì (3 ngày, 7 ngày, 21 ngày hình thành thói quen).
- **Lập luận chọn vào MVP:** Cơ chế tâm lý học kích thích tiết Dopamine, biến việc uống nước từ nhiệm vụ khô khan thành một trò chơi thú vị cần bảo vệ chuỗi liên tục.

---

## 3. Ma trận Đánh giá Impact — Effort (Tác động vs. Nỗ lực)

### Thang điểm đánh giá (1 đến 5):
- **Impact (Mức độ tác động đến trải nghiệm người dùng & mục tiêu sản phẩm):** 1 (Rất thấp) $\rightarrow$ 5 (Rất cao / Sống còn).
- **Effort (Độ phức tạp kỹ thuật & thời gian triển khai):** 1 (Rất nhanh/dễ) $\rightarrow$ 5 (Cực kỳ phức tạp/tốn công).

| Mã | Tính năng | Điểm Impact (1-5) | Điểm Effort (1-5) | Phân loại ma trận | Ưu tiên triển khai |
|---|---|:---:|:---:|---|:---:|
| **F2** | **1-Tap Quick Logging** | 5 | 2 | 🟢 **Quick Wins** (Thắng nhanh) | **P1 (Làm ngay)** |
| **F3** | **Visual Daily Progress Ring** | 5 | 2 | 🟢 **Quick Wins** (Thắng nhanh) | **P1 (Làm ngay)** |
| **F6** | **Streak & Celebration** | 4 | 2 | 🟢 **Quick Wins** (Thắng nhanh) | **P2 (Ưu tiên cao)** |
| **F1** | **Onboarding & Dynamic Goal** | 4 | 3 | 🟡 **Major Projects** (Dự án lớn) | **P2 (Ưu tiên cao)** |
| **F4** | **Smart Interval Reminders** | 4 | 3 | 🟡 **Major Projects** (Dự án lớn) | **P3 (Giai đoạn sau)**|
| **F5** | **Daily/Weekly Analytics** | 3 | 3 | 🟡 **Major Projects** (Dự án lớn) | **P3 (Giai đoạn sau)**|

---

## 4. Sơ đồ Ma trận Hành động (Action Matrix Diagram)

```
Impact (Tác động)
  ^
5 |     [F2: Quick Log]   [F3: Progress Ring]
  |
4 |     [F6: Streak]      [F1: Onboarding]    [F4: Reminders]
  |
3 |                       [F5: Analytics]
  |
2 |
  |
1 +----------------------------------------------------> Effort (Nỗ lực)
          1         2         3         4         5

Phân vùng:
• [Quick Wins] (Góc trên trái - Impact cao, Effort thấp): F2, F3, F6 -> Làm đầu tiên để tạo giá trị sớm nhất.
• [Major Projects] (Góc trên phải - Impact cao, Effort vừa): F1, F4, F5 -> Lên kế hoạch cẩn thận và thực hiện tuần tự.
• Không có tính năng nào rơi vào vùng [Thankless Tasks] (Impact thấp, Effort cao) nhờ đã cắt gọn scope chuẩn Lean.
```

---

## 5. Danh mục tính năng hoãn lại sau MVP (Out of Scope for MVP)

Để tránh hiện tượng trễ tiến độ (Feature Creep), các tính năng sau được ghi nhận vào Backlog phiên bản Beta / v2.0:
1. Đồng bộ dữ liệu lên Apple Health / Google Health Connect.
2. Tiện ích màn hình khóa & Dynamic Island (Lock screen interactive widgets).
3. Thêm các loại đồ uống nâng cao (Cà phê, trà, sinh tố với hệ số khử nước).
4. Tính toán bù nước tự động theo định vị thời tiết (GPS Weather API).
5. Bảng xếp hạng thi đua uống nước cùng nhóm bạn bè (Social Leaderboard).

