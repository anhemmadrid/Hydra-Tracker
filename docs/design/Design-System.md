# 🎨 Hydra Tracker — Design System Specification

> Phân tích từ **WaterMinder** (iOS 26 / Liquid Glass) → Design System chuẩn cho **Hydra Tracker** trên Figma.

---

## 📸 Màn hình tham chiếu (WaterMinder iOS 26)

````carousel
![Home — Nhân vật nước & Progress Bar](/C:/Users/thanh/.gemini/antigravity/brain/56236b54-6fa7-454a-95d4-e07fd5929c1b/screen-home.jpg)
<!-- slide -->
![History — Biểu đồ & Today's Logs](/C:/Users/thanh/.gemini/antigravity/brain/56236b54-6fa7-454a-95d4-e07fd5929c1b/screen-history.jpg)
<!-- slide -->
![Sharing — Card bạn bè & Progress](/C:/Users/thanh/.gemini/antigravity/brain/56236b54-6fa7-454a-95d4-e07fd5929c1b/screen-sharing.jpg)
<!-- slide -->
![Settings — Profile & Preferences](/C:/Users/thanh/.gemini/antigravity/brain/56236b54-6fa7-454a-95d4-e07fd5929c1b/screen-settings.jpg)
<!-- slide -->
![Handbook — Challenge Cards Grid](/C:/Users/thanh/.gemini/antigravity/brain/56236b54-6fa7-454a-95d4-e07fd5929c1b/screen-handbook.jpg)
````

---

## 1. 🔤 Typography

App WaterMinder sử dụng hệ thống font **SF Pro** chuẩn Apple Human Interface Guidelines, kết hợp hai biến thể **SF Pro Display** (cho heading lớn) và **SF Pro Text** (cho body & caption).

### Font Scale (Figma Variables)

| Token Name | Font Family | Weight | Size (pt) | Line Height | Letter Spacing | Ví dụ sử dụng trong app |
|---|---|---|:---:|:---:|:---:|---|
| `type/largeTitle` | SF Pro Display | **Bold (700)** | **34** | 41pt (120%) | 0.37 | "Sharing", "Settings" — Tiêu đề trang |
| `type/title1` | SF Pro Display | **Bold (700)** | **28** | 34pt (121%) | 0.36 | — Không thấy trực tiếp, dự phòng |
| `type/title2` | SF Pro Display | **Bold (700)** | **22** | 28pt (127%) | 0.35 | "Stay hydrated together", "Profile", "Today's Logs" |
| `type/title3` | SF Pro Display | **Semibold (600)** | **20** | 25pt (125%) | 0.38 | "Reminders & Drinks", "Needs Attention" |
| `type/headline` | SF Pro Text | **Semibold (600)** | **17** | 22pt (129%) | -0.41 | "Tansan (Me)", "Tansan", Nav title "History", "Handbook" |
| `type/body` | SF Pro Text | **Regular (400)** | **17** | 22pt (129%) | -0.41 | "Daily Goal: 2.700 ml", "Water - 500ml" |
| `type/callout` | SF Pro Text | **Regular (400)** | **16** | 21pt (131%) | -0.32 | "Upgrade to Premium", tên item Settings |
| `type/subheadline` | SF Pro Text | **Regular (400)** | **15** | 20pt (133%) | -0.24 | "Here's how Sharing looks...", "adjust daily goal and more" |
| `type/footnote` | SF Pro Text | **Regular (400)** | **13** | 18pt (138%) | -0.08 | "Friends you invite will see this", "Recommended Goal", "15:17" (timestamps) |
| `type/caption1` | SF Pro Text | **Regular (400)** | **12** | 16pt (133%) | 0 | "CHALLENGE" label, axis labels "00", "12" |
| `type/caption2` | SF Pro Text | **Medium (500)** | **11** | 13pt (118%) | 0.07 | Tab bar labels, "daily goal" nhỏ |

### Gợi ý Weight mapping cho Figma:

| Weight Name | Numeric | Khi nào dùng |
|---|:---:|---|
| Regular | 400 | Body text, description, caption, placeholder |
| Medium | 500 | Tab labels, badge text, small emphasis |
| Semibold | 600 | Section headers (title3), headline, nav bar title |
| Bold | 700 | Large title, title1-2, số liệu nổi bật ("3.350 ml") |

> [!TIP]
> **Cho Hydra Tracker:** Sử dụng **SF Pro** nếu target iOS, hoặc **Inter** (Google Fonts, miễn phí, visual gần giống SF Pro) nếu cần cross-platform. Khi build Figma, tạo các Text Styles map 1:1 theo bảng trên.

---

## 2. 🎨 Color Tokens

### 2.1 Bảng màu nền (Backgrounds & Surfaces)

| Token Name | Hex | Opacity | Mô tả | Nơi sử dụng trong app |
|---|---|:---:|---|---|
| `color/bg/primary` | `#EBF2FA` | 100% | Nền chính toàn app — xanh xám rất nhạt | Background của mọi màn hình |
| `color/bg/secondary` | `#D6E6F5` | 100% | Nền nhấn nhẹ hơn — xanh nhạt hơn 1 bậc | Background Home (gradient top) |
| `color/bg/home-gradient-top` | `#DAEAF8` | 100% | Gradient nền Home phía trên | Phần trên Home screen |
| `color/bg/home-gradient-bottom` | `#C4DCF2` | 100% | Gradient nền Home phía dưới | Phần dưới Home screen |

### 2.2 Surfaces & Cards

| Token Name | Hex | Opacity | Mô tả | Nơi sử dụng |
|---|---|:---:|---|---|
| `color/surface/card` | `#FFFFFF` | 95% | Card chính — trắng gần nguyên, viền mờ siêu nhẹ | Profile card, Upgrade Premium card, Chart card |
| `color/surface/card-elevated` | `#FFFFFF` | 100% | Card nổi bật (có shadow rõ hơn) | Friend card (active, có viền xanh lá) |
| `color/surface/glass` | `#FFFFFF` | 45–55% | Lớp Liquid Glass — bán trong suốt | Tab bar, icon button nhỏ (✨, 🔄) |
| `color/surface/segmented-bg` | `#E8EFF6` | 90% | Nền Segmented Control (inactive area) | Segmented "D W M Y" và "Challenges / Achievements" |
| `color/surface/input` | `#F5F7FA` | 100% | Nền input/skeleton placeholder | Placeholder card bạn bè, skeleton loading |

### 2.3 Text Colors

| Token Name | Hex | Mô tả | Ví dụ |
|---|---|---|---|
| `color/text/primary` | `#1C1C1E` | Text chính — near-black chuẩn iOS | "Settings", "Sharing", "Tansan", tiêu đề trang |
| `color/text/secondary` | `#3C3C43` | Text phụ — xám đậm dịu hơn | "Daily Goal: 2.700 ml", body text |
| `color/text/tertiary` | `#8A8A8E` | Text mức 3 — xám trung bình | "adjust daily goal and more", mô tả nhỏ |
| `color/text/muted` | `#AEAEB2` | Text rất nhạt — placeholder, hint | "Your friend here", caption phụ, axis labels |
| `color/text/on-accent` | `#FFFFFF` | Text trên nền accent (nút bấm, tab active) | "Share Your Progress", "D" trên tab active, "Details" |
| `color/text/on-dark` | `#FFFFFF` | Text trên nền tối | "CHALLENGE", "No Coffee" trên card tối |
| `color/text/link` | `#007AFF` | Text link / text tương tác | "Invite", "Set Times", "Recommended Goal" |

### 2.4 Accent / Brand Colors (Màu chủ đạo)

| Token Name | Hex | Mô tả | Nơi sử dụng |
|---|---|---|---|
| `color/accent/primary` | `#2196F3` | **Xanh dương chủ đạo** — Dodger Blue | FAB button (+), Progress bar, Active tab icon, Segmented active, nút "Details" |
| `color/accent/primary-dark` | `#1976D2` | Xanh dương đậm hơn — cho pressed/hover state | FAB shadow, gradient tiến độ |
| `color/accent/primary-light` | `#64B5F6` | Xanh dương nhạt — soft highlight | Progress bar track nhạt, glow effect |
| `color/accent/primary-surface` | `#E3F2FD` | Xanh dương rất nhạt — surface tint | Background nhẹ cho icon containers |
| `color/accent/character-fill` | `#1E88E5` | Màu đổ đặc nhân vật nước | Body fill của character illustration (Home) |
| `color/accent/character-outline` | `#1565C0` | Viền đậm nhân vật | Outline & shadow của character |

### 2.5 Semantic / Status Colors

| Token Name | Hex | Mô tả | Nơi sử dụng |
|---|---|---|---|
| `color/semantic/success` | `#4CAF50` | Xanh lá — đạt mục tiêu, hoàn thành | Viền xanh lá quanh card "Goal reached!", viền log card đạt mục tiêu |
| `color/semantic/success-light` | `#E8F5E9` | Xanh lá nhạt — bg success subtle | Background tint cho log card đã hoàn thành |
| `color/semantic/warning` | `#FF9800` | Cam — cảnh báo, cần chú ý | Badge "1" trên "Needs Attention", icon iCloud warning |
| `color/semantic/warning-light` | `#FFF3E0` | Cam nhạt | Nền warning badge |
| `color/semantic/danger` | `#F44336` | Đỏ — lỗi nghiêm trọng | Text "Error:" trên iCloud sync failed |
| `color/semantic/danger-light` | `#FFEBEE` | Đỏ nhạt | — Dự phòng |
| `color/semantic/info` | `#2196F3` | = accent primary | Lặp lại accent cho consistency |

### 2.6 Challenge Card Palette (Handbook)

| Token Name | Hex | Mô tả |
|---|---|---|
| `color/challenge/green` | `#66BB6A` | Card "No Alcohol" |
| `color/challenge/gold` | `#FFC107` | Card "Cup o' Tea a Day" |
| `color/challenge/brown` | `#8D6E63` | Card "No Coffee" |
| `color/challenge/teal` | `#80DEEA` | Card "Vitamin Boost", "No Sugar" |
| `color/challenge/coral` | `#FF7043` | Card "No Caffeine" |
| `color/challenge/sky` | `#4FC3F7` | Card background variation |

---

## 3. 🪟 Liquid Glass — Phân tích & Đề xuất

### 3.1 Phân tích cách WaterMinder đang dùng Liquid Glass

App WaterMinder đã cập nhật theo **iOS 26 Liquid Glass** guidelines. Dưới đây là phân tích chi tiết từng thành phần:

#### Tab Bar (Quan sát rõ nhất ở mọi màn hình)

| Thuộc tính | Giá trị quan sát | Ghi chú |
|---|---|---|
| **Material** | Frosted glass translucent | Nền phía sau xuyên qua được |
| **Background Blur** | ~30–40px Gaussian blur | Làm mờ content phía dưới tab bar đủ để đọc icon |
| **Tint Color** | `#FFFFFF` @ 45–55% opacity | Lớp trắng phủ lên vùng blur |
| **Border** | 0.5px solid `#FFFFFF` @ 30% | Viền trắng siêu mỏng ở rìa trên, tạo cảm giác kính |
| **Corner Radius** | ~26–28px (capsule-like) | Bo tròn lớn, gần dạng pill |
| **Shadow** | 0 2px 12px `#000000` @ 5% | Drop shadow rất nhẹ phía dưới |
| **Active Tab** | Icon fill `#2196F3`, nền circle `#FFFFFF` @ 70% | Tab đang chọn có halo trắng bao quanh icon |
| **Inactive Tab** | Icon fill `#8A8A8E` @ 60% | Icon xám mờ |
| **Position** | Floating — cách bottom edge ~8px | Không dính sát đáy, bay lơ lửng |

#### Icon Buttons góc (✨, 🔄 trên Home)

| Thuộc tính | Giá trị |
|---|---|
| **Shape** | Circle 40×40pt |
| **Background** | `#FFFFFF` @ 50% + blur 20px |
| **Border** | 0.5px `#FFFFFF` @ 40% |
| **Icon Color** | `#3C3C43` @ 70% |

#### Cards (Settings, History, Sharing)

| Thuộc tính | Giá trị |
|---|---|
| **Background** | `#FFFFFF` @ 92–95% (gần opaque, subtle glass) |
| **Blur** | Minimal — 8–10px (chỉ thấy khi scroll) |
| **Corner Radius** | 16px |
| **Border** | 0.5px `#E5E5EA` (separator nhẹ) |
| **Shadow** | 0 1px 4px `#000000` @ 4% |
| **Padding** | 16px all sides |

#### Segmented Control ("D W M Y" / "Challenges / Achievements")

| Thuộc tính | Giá trị |
|---|---|
| **Container BG** | `#E8EFF6` @ 85% + blur 10px |
| **Container Radius** | 10px |
| **Active Segment BG** | `#2196F3` solid (opaque) |
| **Active Segment Radius** | 8px |
| **Active Text** | `#FFFFFF` Bold |
| **Inactive Text** | `#8A8A8E` Regular |

---

### 3.2 Đề xuất áp dụng Liquid Glass cho Hydra Tracker

> [!IMPORTANT]
> Liquid Glass hiệu quả nhất khi có **content phía sau di chuyển** (scroll). Không nên lạm dụng cho mọi element — chỉ dùng cho **tab bar, floating buttons, và overlay** để giữ sự trang nhã.

#### Tab Bar — Hydra Tracker

```
┌─────────────────────────────────────────────┐
│  background:    rgba(255,255,255, 0.50)     │
│  backdrop-blur: 40px                        │
│  border:        0.5px solid rgba(255,255,255, 0.30) │
│  border-radius: 28px                        │
│  shadow:        0 2px 16px rgba(0,0,0, 0.06)│
│  margin-bottom: 8px (floating)              │
│  padding:       8px 12px                    │
│                                             │
│  Active icon:   fill #2196F3                │
│                 bg circle rgba(255,255,255, 0.70) │
│  Inactive icon: fill rgba(138,138,142, 0.60)│
└─────────────────────────────────────────────┘
```

#### Cards — Hydra Tracker

```
┌─────────────────────────────────────────────┐
│  Light glass card (cho nội dung tĩnh):      │
│  background:    rgba(255,255,255, 0.92)     │
│  backdrop-blur: 10px                        │
│  border:        0.5px solid rgba(0,0,0, 0.04)│
│  border-radius: 16px                        │
│  shadow:        0 1px 4px rgba(0,0,0, 0.04) │
│  padding:       16px                        │
│                                             │
│  Heavy glass card (cho floating/modal):     │
│  background:    rgba(255,255,255, 0.55)     │
│  backdrop-blur: 30px                        │
│  border:        0.5px solid rgba(255,255,255, 0.35)│
│  border-radius: 20px                        │
│  shadow:        0 4px 20px rgba(0,0,0, 0.08)│
└─────────────────────────────────────────────┘
```

#### Floating Action Button (FAB) — Hydra Tracker

```
┌─────────────────────────────────────────────┐
│  background:    #2196F3 (opaque — brand)    │
│  size:          56 × 56pt                   │
│  border-radius: 28px (full circle)          │
│  shadow:        0 4px 16px rgba(33,150,243, 0.35) │
│  icon:          "+" white, 24pt stroke 2.5  │
│                                             │
│  ⚠ FAB KHÔNG dùng glass — giữ solid màu    │
│  accent để nổi bật nhất trên màn hình.      │
└─────────────────────────────────────────────┘
```

---

## 4. 📏 Spacing Scale (Base 4px)

| Token Name | Value (px) | Ví dụ sử dụng |
|---|:---:|---|
| `space/2xs` | **2** | Gap giữa icon & badge nhỏ, border width hint |
| `space/xs` | **4** | Spacing siêu nhỏ, gap giữa text lines, inner padding chip |
| `space/sm` | **8** | Gap giữa icon và label trong card, padding nhỏ |
| `space/md` | **12** | Gap giữa các items trong list, padding segmented control |
| `space/base` | **16** | 🟢 **Padding chuẩn** — card padding, section margin, horizontal screen margin |
| `space/lg` | **20** | Gap giữa section header và content |
| `space/xl` | **24** | Gap giữa các sections (groups), top/bottom safe area spacing |
| `space/2xl` | **32** | Vertical spacing lớn giữa các nhóm nội dung khác nhau (Settings sections) |
| `space/3xl` | **40** | Gap trên Large Title với cạnh trên |
| `space/4xl` | **48** | Khoảng trống thoáng giữa hero element và nội dung kế tiếp |
| `space/5xl` | **64** | Spacing lớn nhất — top margin cho content bên dưới floating tab bar |

### Screen Margin chuẩn

| Vùng | Giá trị |
|---|---|
| Horizontal padding (trái-phải) | 16px |
| Tab bar bottom margin (floating) | 8px |
| Tab bar height | 52–56px |
| Safe area top (dynamic island) | 59px |
| Safe area bottom | 34px |

---

## 5. 🔘 Border Radius Scale

| Token Name | Value (px) | Nơi sử dụng |
|---|:---:|---|
| `radius/xs` | **4** | Checkbox, tiny tag/badge, inner element nhỏ |
| `radius/sm` | **8** | Active segment pill trong Segmented Control, small chip |
| `radius/md` | **12** | Button (secondary/ghost), input field, Toast notification |
| `radius/lg` | **16** | 🟢 **Card chuẩn** — Card Settings, Card History, Card Profile, Log item |
| `radius/xl` | **20** | Card nổi (elevated/modal), bottom sheet, chart container |
| `radius/2xl` | **28** | Tab bar (capsule shape), large floating panels |
| `radius/full` | **9999** | Circle — Avatar, FAB button, icon button tròn, progress ring, badge |

---

## 6. 🧩 Component Token Summary (Quick Reference cho Figma)

### Primary Button (CTA)

| Property | Value |
|---|---|
| Background | `#2196F3` (accent/primary) |
| Text | `#FFFFFF`, SF Pro Text Semibold 17pt |
| Padding | 14px vertical, 24px horizontal |
| Border Radius | `radius/full` (9999 — pill shape) |
| Shadow | 0 2px 8px `rgba(33,150,243, 0.25)` |
| **Pressed** | Background `#1976D2`, scale 0.97 |

### Card — Standard

| Property | Value |
|---|---|
| Background | `#FFFFFF` @ 93% |
| Backdrop Blur | 10px |
| Border | 0.5px `#E5E5EA` |
| Border Radius | `radius/lg` (16px) |
| Shadow | 0 1px 4px `rgba(0,0,0, 0.04)` |
| Padding | 16px |

### Log Item Card (History)

| Property | Value |
|---|---|
| Background | `#FFFFFF` @ 95% |
| Border | 1.5px solid `color/semantic/success` (`#4CAF50`) khi đạt goal |
| Border Radius | `radius/lg` (16px) |
| Layout | Row: [Icon 40px] — 12px — [Content Column] — [Progress Ring 36px] |

### Progress Bar

| Property | Value |
|---|---|
| Track BG | `#E3F2FD` (accent/primary-surface) |
| Fill | Linear gradient `#2196F3` → `#1E88E5` (left→right) |
| Height | 8px |
| Border Radius | `radius/full` (pill) |

### Tab Bar

| Property | Value |
|---|---|
| Background | `rgba(255,255,255, 0.50)` |
| Backdrop Blur | 40px |
| Border | 0.5px `rgba(255,255,255, 0.30)` |
| Border Radius | `radius/2xl` (28px) |
| Height | 56px |
| Bottom Margin | 8px (floating) |
| Shadow | 0 2px 16px `rgba(0,0,0, 0.06)` |
| Active Icon | `#2196F3` + white circle halo |
| Inactive Icon | `#8A8A8E` @ 60% |

### Segmented Control

| Property | Value |
|---|---|
| Container BG | `#E8EFF6` @ 85% |
| Container Radius | 10px |
| Container Padding | 3px |
| Segment Active BG | `#2196F3` solid |
| Segment Active Radius | 8px |
| Segment Active Text | `#FFFFFF` Semibold |
| Segment Inactive Text | `#8A8A8E` Regular |
| Height | 36px |

---

## 7. 📐 Tổng hợp Figma Variables (Copy-Paste Ready)

Khi tạo **Variables** trong Figma, tổ chức theo **Collections** sau:

### Collection: `Colors`
```
colors/bg/primary          → #EBF2FA
colors/bg/secondary        → #D6E6F5
colors/surface/card        → #FFFFFF (opacity 93%)
colors/surface/glass       → #FFFFFF (opacity 50%)
colors/text/primary        → #1C1C1E
colors/text/secondary      → #3C3C43
colors/text/tertiary       → #8A8A8E
colors/text/muted          → #AEAEB2
colors/text/onAccent       → #FFFFFF
colors/accent/primary      → #2196F3
colors/accent/primaryDark  → #1976D2
colors/accent/primaryLight → #64B5F6
colors/accent/surface      → #E3F2FD
colors/semantic/success    → #4CAF50
colors/semantic/warning    → #FF9800
colors/semantic/danger     → #F44336
```

### Collection: `Spacing`
```
space/2xs   → 2
space/xs    → 4
space/sm    → 8
space/md    → 12
space/base  → 16
space/lg    → 20
space/xl    → 24
space/2xl   → 32
space/3xl   → 40
space/4xl   → 48
space/5xl   → 64
```

### Collection: `Radius`
```
radius/xs   → 4
radius/sm   → 8
radius/md   → 12
radius/lg   → 16
radius/xl   → 20
radius/2xl  → 28
radius/full → 9999
```
