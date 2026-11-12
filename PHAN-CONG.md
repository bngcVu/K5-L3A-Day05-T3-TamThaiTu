# Phân công LAB5 — L3A · T3 Du lịch · Nhóm TamThaiTu

> **Hạn nộp:** 23:59 ngày 12/11/2026 · **Nộp:** link repo công khai `K5-L3A-Day05-T3-TamThaiTu` gồm `spec.md` + `prototype/` · Repo nộp **không** chứa file này.
>
> **Lát cắt T3:** trong Đặt chỗ của tôi, hành khách vừa nhận tin chuyến bị huỷ và nhắn hỏi → AI giữ chỗ / hỏi lại / đổi vé / chuyển nhân viên. Dữ liệu và tool: `Tai-lieu-tham-khao/t3-travel.md`.

---

## 1. Trạng thái hiện tại

| Mục | Người | Trạng thái |
|---|---|---|
| Bảng thành viên (họ tên đầy đủ, mã HV, bàn/zone) | cả nhóm | **Chưa** — placeholder trong `spec.md` |
| §1 Lát cắt, §2 Kịch bản (K1–K12), §4 Mức tự chủ | VŨ | **Đã viết** — chờ cả nhóm đọc và chốt |
| §4 bảng bỏ phiếu "tool khó xếp nhất" | TRƯỜNG, THÀNH | **Chưa** — điền cột của mình sau khi tự xếp mức |
| §3 Khi AI sai | TRƯỜNG | Chưa |
| §6 Tốt là gì | TRƯỜNG | Chưa |
| §5 Prototype + thư mục `prototype/` | THÀNH | Chưa |
| §7 Demo | THÀNH | Sau demo |

---

## 2. Ai giữ phần nào

| Thành viên | Giữ chính | Phụ | Điểm |
|---|---|---|---|
| **VŨ** | §1, §2, §4 | Đọc lại §3 và §5 (kiểm khớp); chấm thử §6 | R1+R2+R4 = 40 |
| **TRƯỜNG** | §3 | §6; câu chữ AI trong prototype; đọc lại §4 | R3+R6 = 30 |
| **THÀNH** | §5, `prototype/` | §7; repo và nộp bài; đọc lại §2 | R5+R7 = 30 |

Mỗi phần có **một người viết, một người đọc lại**. Ai cũng đã đọc phần của người khác nên khi demo bị hỏi vẫn trả lời được.

---

## 3. Việc còn lại, theo thứ tự

### Bước 1 — Cả nhóm (15 phút)
- [x] TRƯỜNG, THÀNH đọc `spec.md` §2 và §4. Chỗ nào không đồng ý thì sửa ngay.
- [x] Xác nhận 2 kịch bản đắt nhất (**K3, K9**) và mức tự chủ cho 5 tool.
- [x] Mỗi người tự xếp mức cho `gui_yeu_cau_hoan_ve` (5 phút, không bàn), rồi **điền cột của mình** vào bảng bỏ phiếu §4. Nếu kết quả khác P2 thì VŨ sửa phần "nhóm chốt". *(Trường đã chọn P2; Vũ P2; cột Thành còn trống — cho tới giờ chưa có phiếu nào khác P2, nên chưa cần sửa "nhóm chốt".)*
- [x] Điền họ tên đầy đủ của 3 thành viên vào đầu `spec.md`
- [x] Kiểm lại **mã học viên** của Trường (`2A2026034` chỉ có 9 ký tự, hai bạn kia có 11) — **phải đúng**
- [ ] Điền bàn/zone (hiện còn `____`)

### Bước 2 — TRƯỜNG: §3 (khoảng 45 phút)
Làm cho **K3** và **K9**. Mỗi kịch bản ghi:
- [x] Câu AI nói **nguyên văn** · người dùng thấy gì ngoài câu chữ · làm gì tiếp · ai được báo, sau bao lâu
- [x] Quyết định hỏi lại / trả lời kèm giới hạn / chuyển người: chọn gì, **loại hai cách kia vì sao**
- [x] Loại lỗi: hệ thống / người dùng / ngữ cảnh; vì sao cách nói và cách sửa đi theo loại đó
- [x] 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào **một câu chữ cụ thể**
- [x] Một lỗi **sửa câu chữ không cứu được**: dùng K11 hoặc K12 ("đã huỷ", "đã đổi lại" khi không có tool). Thiết kế cứu: L5 chuyển nhân viên + nút chỉ hiện khi tool có thật
- [x] Nghĩ đủ 4 đường: happy path · low-confidence · không căn cứ · người dùng sửa AI

**Bàn giao cho THÀNH:** câu chữ nguyên văn + nguyên tắc HAX/PAIR nào ở chỗ nào.

### Bước 3 — THÀNH: prototype (khoảng 60 phút)

**Công cụ (đã chốt): một file `prototype/index.html` do coding agent (Claude Code) viết, mở thẳng bằng trình duyệt.** Không Lovable, v0, Figma, không cần đăng ký tài khoản hay cài thêm. Lý do: README cho phép "chỉ cần trình duyệt nếu làm HTML", và đây là cách ít tốn token nhất.

**Quy tắc làm gọn (để đỡ tốn token):**
- Một file duy nhất, **HTML + CSS + JS thuần**, không thư viện, không CDN, không ảnh, không animation (trừ đồng hồ đếm ngược của giữ chỗ).
- CSS tối đa khoảng 20 dòng: font hệ thống, viền xám, nút mặc định, mỗi mức tự chủ khác nhau bằng một nhãn chữ (không cần màu mè).
- Dữ liệu giả cứng trong một object JS (đặt chỗ TRV-7Q2K và 3 chuyến thay thế). Hội thoại là kịch bản có sẵn, bấm nút để đi tiếp. Không backend, không đăng nhập.
- Không gọi AI thật ở bản đầu. Chỉ làm bonus +3 nếu còn giờ **và** không lộ API key.
- Yêu cầu agent sửa theo từng lần nhỏ, không viết lại cả file mỗi lần.
- Ảnh đánh số: số ①②③ viết thẳng vào HTML (thẻ `<sup>` hoặc `<b>`), rồi chụp màn hình trình duyệt. Không cần công cụ chỉnh ảnh.

**Nội dung (1 file, 2 màn hình, chuyển bằng 2 tab chữ):**
- [x] **Màn 1 — K3:** tin "đổi giúp mình sang sáng mai" → AI giữ chỗ BM 201 (đếm ngược 20 phút, nút *Nhả chỗ* = tự làm có hoàn tác) → **thẻ xác nhận đổi** có tên từng hành khách, dòng "dùng lần đổi miễn phí duy nhất", nút *Xác nhận đổi · Xem chuyến khác · Gặp nhân viên* (cần duyệt). Có một dòng căn cứ: "Nguồn: dữ liệu đặt chỗ lúc 15:00".
- [x] **Màn 2 — K12:** khách nói đổi nhầm, AI nhận lỗi thật, **không có nút "đổi lại"**, chỉ có *Gặp nhân viên* kèm bản tóm tắt cho nhân viên.
- [x] Thể hiện ≥2 mức tự chủ khác nhau; việc cấm (đổi tên, huỷ yêu cầu hoàn đã gửi) **không có nút**
- [x] Bấm qua từ đầu tới cuối không cần can thiệp tay
- [x] Ca lạ: ô nhập tin tự do chuyển nhân viên khi tin không khớp kịch bản có sẵn
- [x] 2 ảnh đánh số trong `prototype/`; mỗi số ghi: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào
- [x] Ghi §5: công cụ · phần nào mock · không gọi AI thật · **cách hiện đã chọn, cách khác đã nghĩ tới và vì sao loại**
- [x] Prototype **không vi phạm 3 việc "KHÔNG làm"** ở §1 (không bồi thường, không đổi tên, không thanh toán)
- [ ] Kẹt kỹ thuật quá 20 phút thì **gọi TA**; không dựng được thì vẽ tay 2 màn hình rồi chụp

**Trong lúc THÀNH dựng:** VŨ đọc lại prototype so với §4 (nút nào có, nút nào không) và viết sẵn 3 ca lạ để thử.

### Bước 4 — Hoàn thiện (khoảng 20 phút)
- [x] TRƯỜNG viết §6: 3 tiêu chí Pass/Fail mà người ngoài nhóm chấm ra cùng kết quả
- [ ] VŨ chấm thử §6 trên K3 và K9, ghi lỗi còn lại
- [x] THÀNH chụp ảnh đánh số, ghi §5

### Bước 5 — Demo (30 phút) và nộp
- [ ] Mỗi người nói một phần: THÀNH (lát cắt và bấm prototype) · VŨ (kịch bản và mức tự chủ, cái giá khi sai) · TRƯỜNG (AI nói gì khi sai)
- [ ] THÀNH ghi §7: ca lạ nhận được, prototype xử lý thế nào, nhóm có đổi ý gì
- [ ] Quyết định có xung phong demo trước lớp (+5) không: người nói chính là ______
- [ ] THÀNH tạo repo mới, trống, công khai `K5-L3A-Day05-T3-TamThaiTu`, chỉ chứa `spec.md` và `prototype/`; mở thử bằng cửa sổ ẩn danh
- [ ] Không commit API key; chỉ dùng dữ liệu dựng

---

## 4. Bàn giao

| Từ → Đến | Gì | Khi nào |
|---|---|---|
| VŨ → cả nhóm | `spec.md` §1, §2, §4 | Xong rồi |
| TRƯỜNG → THÀNH | Câu chữ AI nguyên văn, nguyên tắc HAX/PAIR và chỗ trên màn hình | Trước khi THÀNH dựng màn 2 |
| VŨ → THÀNH | Bảng mức (nút nào có, nút nào không): đã nằm trong §4 | Xong rồi |
| THÀNH → VŨ, TRƯỜNG | Prototype và ảnh đánh số, để kiểm khớp §3, §4 | Trước demo |

---

## 5. Kiểm tra trước khi nộp

- [ ] Mỗi người trả lời được: *"Hành động này sai thì ai mất gì?"* · *"Lỗi nguy hiểm nhất là gì?"* · *"Phần bạn làm là gì?"*
- [ ] Mỗi người chỉ được trên màn hình: *"Chỗ nào là G__?"*
- [ ] Câu chữ trong prototype khớp nguyên văn với §3; nút khớp mức ở §4
- [ ] Bảng "Việc đã làm" trong `spec.md` ghi đúng việc thực tế của từng người
