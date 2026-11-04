# 📝 Project Overview — Hydra Tracker

> **Slogan:** *"Mỗi ngụm nước — Một thói quen lành mạnh"*  
> *(English: "Track every drop, boost your health effortlessly")*

---

## 1. Bối cảnh & Vấn đề thực tế (Problem Statement)

Nước chiếm khoảng 60–70% trọng lượng cơ thể người và đóng vai trò sống còn đối với quá trình trao đổi chất, lưu thông máu và chức năng não bộ. Theo nhiều nghiên cứu y tế, một người trưởng thành cần trung bình từ 2.0 – 2.5 lít nước mỗi ngày tùy thể trạng và mức độ vận động.

Tuy nhiên, trong thực tế hiện nay:
- **Hơn 75% người trưởng thành (đặc biệt là sinh viên và nhân viên văn phòng)** không uống đủ lượng nước khuyến nghị hàng ngày.
- **Rào cản chính:**
  1. **Hay quên:** Công việc cuốn đi, chỉ uống khi cơ thể đã phát tín hiệu "khát" (khi đó cơ thể đã mất 1-2% lượng nước).
  2. **Không biết nhu cầu thực tế:** Không biết rõ cơ thể mình cần chính xác bao nhiêu ml/ngày dựa trên cân nặng và cường độ thể lực.
  3. **Ứng dụng hiện tại quá rườm rà:** Các app theo dõi trên thị trường thường bắt mở ứng dụng qua nhiều bước, tràn ngập quảng cáo pop-up khó chịu, hoặc quá lạm dụng tính năng phức tạp khiến người dùng nản lòng sau 3-5 ngày.

---

## 2. Mục đích ứng dụng (Vision & Solution)

**Hydra Tracker** ra đời với sứ mệnh: **"Biến việc uống đủ nước thành một phản xạ tự nhiên, không tốn nỗ lực."**

### Giải pháp cốt lõi:
- **Tối giản hóa thao tác (1-Tap Logging):** Người dùng có thể ghi nhận ly nước vừa uống chỉ với 1 chạm duy nhất thông qua các kích thước cốc phổ biến (preset cups) ngay trên màn hình chính hoặc widget.
- **Cá nhân hóa mục tiêu khoa học:** Tự động tính toán lượng nước khuyến nghị mỗi ngày dựa trên thông số sinh học (cân nặng, giới tính, cường độ vận động hàng ngày).
- **Nhắc nhở thông minh & tế nhị:** Phân bổ các khoảng thời gian uống nước hợp lý trong khung giờ sinh hoạt (không làm phiền vào ban đêm hoặc giờ nghỉ ngơi).
- **Nuôi dưỡng động lực:** Thống kê tiến độ trực quan với vòng tròn nước (Progress Ring) và duy trì chuỗi ngày liên tiếp (Streak Counter).

---

## 3. Mục tiêu dự án (Project Goals — SMART)

| Tiêu chí | Mục tiêu cụ thể |
|---|---|
| **Specific (Cụ thể)** | Xây dựng ứng dụng di động Hydra Tracker hoàn chỉnh ở giai đoạn MVP với đầy đủ 6 tính năng cốt lõi: Onboarding, Dynamic Goal, 1-Tap Logging, Smart Notification, Daily/Weekly Stats, Streak Counter. |
| **Measurable (Đo lường được)** | - Thời gian hoàn thành thao tác ghi nhận nước: **< 3 giây**.<br/>- Tỉ lệ người dùng hoàn thành Onboarding: **> 90%**.<br/>- Duy trì chuỗi streak trung bình của người dùng thử nghiệm: **≥ 14 ngày**. |
| **Achievable (Khả thi)** | Scope tính năng được gói gọn trong mô hình MVP tối giản, sử dụng công nghệ hiện đại, tập trung vào trải nghiệm mượt mà không rườm rà. |
| **Relevant (Liên quan)** | Giải quyết trực tiếp bài toán sức khỏe thiết thực, đáp ứng đầy đủ yêu cầu học phần từ phân tích nghiệp vụ, thiết kế UI/UX đến prototype. |
| **Time-bound (Thời hạn)** | - Hoàn thành Assignment 1 (Wiki & Project setup): Tuần 1.<br/>- Hoàn thành Assignment 2 (UI/UX Figma & Landing Page): Tuần 3.<br/>- Triển khai & Hoàn thiện báo cáo: Đúng tiến độ môn học. |

---

## 4. Chân dung người dùng mục tiêu (User Personas)

### 👤 Persona 1: Nguyễn Minh Trí — Dân văn phòng bận rộn
- **Độ tuổi:** 24 tuổi | **Nghề nghiệp:** Lập trình viên / Nhân viên văn phòng.
- **Thói quen:** Ngồi máy lạnh 8 tiếng/ngày, uống nhiều cà phê, thường xuyên quên uống nước lọc.
- **Pain Point:** Mắt mỏi, da khô, đau đầu vào buổi chiều nhưng ngại cài các app theo dõi vì ghét xem quảng cáo và thao tác lâu.
- **Kỳ vọng:** Một ứng dụng sạch sẽ, có widget bấm 1 phát ghi nhận luôn 250ml mà không gián đoạn công việc.

### 👤 Persona 2: Trần Thị Lan Anh — Sinh viên & Thể thao
- **Độ tuổi:** 20 tuổi | **Nghề nghiệp:** Sinh viên đại học, thích tập Gym / Yoga.
- **Thói quen:** Vận động nhiều, đổ mồ hôi, cần bù nước liên tục để duy trì thể lực và làn da đẹp.
- **Pain Point:** Không biết ngày có tập gym thì phải uống thêm bao nhiêu lít nước so với ngày nghỉ.
- **Kỳ vọng:** App tự tính lượng nước chuẩn theo mức độ tập luyện và có đồ thị trực quan để theo dõi xem mình đã đạt mục tiêu tuần hay chưa.

---

## 5. Điều hướng tài liệu Wiki

- 🔍 **[Market Research (Nghiên cứu thị trường)](Market-Research.md)**
- 🧩 **[Business Model Canvas (Mô hình kinh doanh)](Business-Model-Canvas.md)**
- 🚀 **[MVP Features & Ma trận ưu tiên](MVP-Features.md)**
- 🔄 **[User Flows & Sơ đồ tương tác](User-Flows.md)**

