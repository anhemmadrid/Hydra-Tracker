# 🔄 User Flows — Luồng Trải nghiệm Người dùng

> Tài liệu mô tả trực quan và chi tiết các bước tương tác của người dùng đối với các tính năng trọng tâm của **Hydra Tracker** thông qua sơ đồ luồng Mermaid tiêu chuẩn.

---

## 🌊 Flow 1: Thiết lập Mục tiêu Ban đầu (Onboarding & Goal Calculation)

### 1. Sơ đồ tương tác (Mermaid Flowchart)

```mermaid
flowchart TD
    Start(["🚀 Mở ứng dụng lần đầu"]) --> Welcome["👋 Màn hình Welcome\n(Giới thiệu giá trị cốt lõi)"]
    Welcome --> TapGetStarted["Bấm nút 'Bắt đầu ngay'"]
    
    TapGetStarted --> StepWeight["⚖️ Bước 1: Nhập Cân nặng\n(Đơn vị: kg)"]
    StepWeight --> StepGender["⚧️ Bước 2: Chọn Giới tính\n(Nam / Nữ / Khác)"]
    StepGender --> StepActivity["🏃 Bước 3: Chọn Mức độ Vận động\n• Ít vận động (Văn phòng)\n• Vừa phải (30-60p tập/ngày)\n• Cường độ cao (Vận động viên)"]
    
    StepActivity --> Calculate["🧮 Thuật toán tự động tính toán\nLượng nước khuyến nghị (ml/ngày)"]
    Calculate --> DisplayGoal["🎯 Màn hình Hiển thị Mục tiêu Đề xuất\n(Ví dụ: 2,300 ml/ngày)"]
    
    DisplayGoal --> GoalDecision{"Người dùng có muốn\nđiều chỉnh mục tiêu?"}
    
    GoalDecision -- "Muốn sửa" --> CustomGoal["✏️ Nhập con số tùy biến mong muốn"]
    CustomGoal --> StepReminder
    
    GoalDecision -- "Đồng ý đề xuất" --> StepReminder["⏰ Bước 4: Thiết lập Nhắc nhở\n• Chọn giờ thức & giờ ngủ\n• Chọn chu kỳ nhắc (mỗi 1.5h - 2h)"]
    
    StepReminder --> RequestPermission{"Cấp quyền Thông báo\n(Notification Permission)"}
    RequestPermission -- "Cho phép" --> FinishOnboard["Lưu cài đặt vào Local Storage / Cloud"]
    RequestPermission -- "Từ chối" --> Warning["Hiển thị ghi chú: Có thể bật lại trong Cài đặt"]
    Warning --> FinishOnboard
    
    FinishOnboard --> EnterHome(["🏠 Điều hướng thẳng vào Màn hình chính (Home)"])

    style Start fill:#E1F5FE,stroke:#0288D1,stroke-width:2px
    style EnterHome fill:#E8F5E9,stroke:#388E3C,stroke-width:2px
    style DisplayGoal fill:#FFF9C4,stroke:#FBC02D,stroke-width:2px
```

### 2. Mô tả chi tiết từng bước:
1. **Màn hình Welcome:** Hiển thị hình ảnh minh họa trẻ trung, slogan *"Mỗi ngụm nước — Một thói quen lành mạnh"* và nút kêu gọi hành động (CTA) nổi bật.
2. **Nhập thông số thể trạng:** Giao diện dạng trượt số (wheel picker) mượt mà, hạn chế tối đa việc phải gõ bàn phím số.
3. **Hiển thị mục tiêu khoa học:** Giải thích ngắn gọn cách tính dựa trên cân nặng và vận động để người dùng an tâm về tính khoa học.
4. **Cài đặt nhắc nhở & Xin quyền:** Nhấn mạnh lợi ích: *"Bật thông báo để Hydra nhắc bạn đúng lúc khát, không làm phiền khi bạn ngủ"*.

---

## 🥤 Flow 2: Ghi nhận Nước Uống 1-Chạm & Đạt Mốc Ngày (Quick Logging & Celebration)

### 1. Sơ đồ tương tác (Mermaid Flowchart)

```mermaid
flowchart TD
    Home(["🏠 Màn hình chính (Home)\n(Hiển thị Vòng tròn tiến độ % và Mục tiêu)"]) --> ChooseLogMethod{"Người dùng chọn hình thức ghi nhận"}
    
    ChooseLogMethod -- "Chạm 1 lần vào Cốc mẫu" --> TapPreset["👉 Chạm vào biểu tượng Preset Cup:\n• 200 ml (Tách nhỏ)\n• 350 ml (Cốc chuẩn)\n• 500 ml (Chai nước)"]
    ChooseLogMethod -- "Nhập lượng nước khác" --> TapCustom["👉 Chạm nút '+ Tùy chỉnh'"]
    
    TapCustom --> KeypadModal["Bàn phím nhập nhanh số ml\n(Ví dụ: 180 ml)"]
    KeypadModal --> ConfirmCustom["Bấm 'Xác nhận'"]
    
    TapPreset --> TriggerLogging["⚡ Ghi nhận lượng nước vào dữ liệu ngày"]
    ConfirmCustom --> TriggerLogging
    
    TriggerLogging --> MicroFeedback["🔊 Âm thanh rót nước sảng khoái\n📳 Haptic feedback rung nhẹ\n🌊 Hiệu ứng sóng nước dâng lên trên Progress Ring"]
    
    MicroFeedback --> UpdateProgress["Cập nhật số ml hiện tại\nvà % tiến độ ngày"]
    
    UpdateProgress --> Check100Percent{"Đã đạt 100% mục tiêu ngày?"}
    
    Check100Percent -- "Chưa đạt (< 100%)" --> StayHome["Hiển thị số ml còn lại cần uống\n(Ví dụ: 'Còn 450 ml nữa thôi!')"]
    StayHome --> ReturnToHome(["Chờ lần uống kế tiếp"])
    
    Check100Percent -- "Đã đạt (≥ 100%)" --> CelebrationOverlay["🎉 Màn hình Chúc mừng Toàn diện\n• Pháo hoa Confetti tung bay\n• Huy hiệu: 'Đã hoàn thành mục tiêu hôm nay!'\n• Cập nhật Chuỗi thói quen: Streak +1 ngày!"]
    
    CelebrationOverlay --> PostAction{"Hành động tiếp theo"}
    PostAction -- "Đóng chúc mừng" --> ReturnToHome
    PostAction -- "Chia sẻ thành tích" --> ShareModal["Tạo ảnh đẹp để đăng Story Facebook / Instagram"]
    ShareModal --> ReturnToHome

    style Home fill:#E1F5FE,stroke:#0288D1,stroke-width:2px
    style TriggerLogging fill:#B3E5FC,stroke:#03A9F4,stroke-width:2px
    style CelebrationOverlay fill:#FFF3E0,stroke:#FF9800,stroke-width:2px
    style ReturnToHome fill:#E8F5E9,stroke:#388E3C,stroke-width:2px
```

### 2. Xử lý các tình huống biên (Edge Cases):
- **Trường hợp bấm nhầm cốc:** Ngay sau khi ghi nhận, ở góc dưới màn hình luôn xuất hiện một thanh thông báo dạng Toast: *"Đã thêm 350 ml • [Hoàn tác / Undo]"* tồn tại trong 4 giây để người dùng bấm hủy ngay lập tức nếu lỡ tay.
- **Trường hợp uống vượt 100% mục tiêu:** Vòng tròn tiến độ sẽ chuyển sang màu xanh ngọc rực rỡ và hiển thị `115% - Vượt mục tiêu! Rất tuyệt vời nhưng hãy chú ý không uống quá tải`.

---

## ⏰ Flow 3 (Phụ trợ): Nhận Thông báo Nhắc nhở & Quick Log từ Notification

```mermaid
flowchart LR
    PushNoti["🔔 Thông báo nhắc nhở:\n'Đã 2 tiếng rồi! Uống một ngụm nước nhé bạn ơi 💧'"] --> UserAction{"Tương tác của người dùng"}
    
    UserAction -- "Chạm vào Action Button trên thông báo" --> DirectLog["⚡ Ghi nhận ngay 250ml\n(Không cần mở ứng dụng)"]
    DirectLog --> SuccessNoti["Thông báo cập nhật: Đã ghi nhận 250ml!"]
    
    UserAction -- "Chạm vào thân thông báo" --> OpenApp["Mở thẳng vào màn hình Home Hydra Tracker"]
    OpenApp --> TapPreset["Thực hiện Flow ghi nhận 1-chạm"]
    
    UserAction -- "Bỏ qua / Bận" --> AutoDismiss["Tự động lên lịch nhắc lại sau 30 phút"]
```

