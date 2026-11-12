# Phân công LAB5 — L3A · T3 Du lịch · Nhóm TamThaiTu

> **Hạn nộp:** 23:59 ngày 12/11/2026 (lớp L3A) · **Thời lượng:** 240 phút · **Nộp:** link repo công khai `K5-L3A-Day05-T3-TamThaiTu` gồm `spec.md` + `prototype/`
>
> **Lát cắt T3:** đổi lịch / hoàn vé khi chuyến bay bị huỷ (Traveloka + chính sách hãng bay). Cái giá khi sai: mất vé, mất lượt đổi miễn phí, gửi yêu cầu hoàn không rút lại được.
> Chép nguyên văn lát cắt, bảng tool, 3 tin mồi, hard tests và dữ liệu đặt chỗ từ `tracks/t3-travel.md` trong repo đề.

---

## 1. Ai giữ phần nào

Theo rubric, R3 + R4 + R5 chiếm 75/100 điểm, nên mỗi người giữ **một khối chính** và **một khối phụ**. Ai giữ phần nào thì phải giải thích được phần đó khi demo (vibe-coding rule: không giải thích được thì phần đó 0 điểm).

| Thành viên | Vai | Giữ chính (viết, chịu trách nhiệm) | Phụ | Điểm rubric phụ trách |
|---|---|---|---|---|
| **VŨ** — ______ | Kịch bản & mức tự chủ | §2 Kịch bản rủi ro · **§4 Mức tự chủ** | §1 Lát cắt | R1 (5) + R2 (10) + **R4 (25)** = 40 |
| **TRƯỜNG** — ______ | Câu chữ AI & UX khi sai | **§3 Khi AI sai** | §6 Tốt là gì · câu chữ trong prototype | **R3 (25)** + R6 (5) = 30 |
| **THÀNH** — ______ | Prototype & nộp bài | **§5 Prototype** + thư mục `prototype/` | §7 Demo · repo, checklist nộp | **R5 (25)** + R7 (5) = 30 |

**Theo hướng dẫn, chặng 1–4 cả nhóm làm chung.** "Giữ chính" nghĩa là người đó **ghi vào `spec.md`** và **chốt lập luận**, không có nghĩa là làm một mình. Từ chặng 5, mỗi người làm phần mình.

---

## 2. Lịch làm việc theo chặng (240 phút)

| Phút | Chặng | A | B | C | Mốc TA |
|---|---|---|---|---|---|
| 0–10 | 1 · Đọc đề | Viết §1: lát cắt + 3 việc KHÔNG làm | Đọc bảng tool: tool nào đọc, tool nào thay đổi, tool nào **không đảo được** | Tạo repo trống, công khai, đúng tên · copy template thành `spec.md` · điền bảng thành viên | |
| 10–45 | 2 · Kịch bản | **Ghi bảng ≥8 kịch bản** vào §2 · chốt 2 kịch bản đắt nhất | Viết kịch bản lớp ① nguồn sự thật, ② mơ hồ (cách người thật nhắn: viết tắt, đang giận, gộp hai việc) | Viết kịch bản lớp ③ ngoài thẩm quyền, ④ đặc thù domain · bắt đầu phác layout màn hình | **M1** (phút 45) |
| 45–90 | 3 · Khi AI sai | Hỗ trợ: đối chiếu với kịch bản §2, phản biện | **Ghi §3** cho 2 kịch bản đắt nhất | Vẽ phác 1–2 màn hình theo §3 (chưa code) | |
| 90–125 | 4 · Mức tự chủ | **Ghi §4** · điều phối vòng "mỗi người tự xếp 5 phút" | Tự xếp mức · thử mức trên kịch bản thường | Tự xếp mức · nghĩ cách hiện mỗi mức trên màn hình | **M2** (phút 125) |
| 125–140 | Nghỉ | | | | |
| 140–200 | 5 · Prototype | Kiểm prototype có đúng mức ở §4 không · viết sẵn ca lạ để thử | Viết câu chữ AI nguyên văn trong prototype · map nguyên tắc HAX/PAIR vào màn hình | **Dựng prototype** · chụp 1–2 ảnh đánh số · ghi §5 | **M3** (phút 200) |
| 200–210 | 6 · Tốt là gì | Chấm thử trên 2 kịch bản đắt nhất | **Ghi §6**: 3 tiêu chí Pass/Fail | Sửa lỗi prototype | |
| 210–240 | Demo | Trình bày: kịch bản + mức tự chủ | Trình bày: AI nói gì khi sai | Trình bày: lát cắt + bấm prototype · ghi §7 sau demo | |

**Thiếu giờ:** bỏ §6 và giảm số kịch bản ở §2. **Không cắt §3, §4, §5.**

---

## 3. Việc cụ thể của từng người

Mỗi quyết định ghi đủ **bốn ý**: *đã cân nhắc phương án nào · chọn phương án nào · vì sao · loại các phương án kia vì sao*. Bằng chứng phải trỏ về **tool cụ thể, dòng dữ liệu của track, mục "Sản phẩm thật hôm nay", hoặc số trên ảnh prototype**. "AI có thể trả lời sai" không được tính.

### VŨ — Kịch bản & mức tự chủ

**§1 Lát cắt & phạm vi** (R1 · 5 điểm)
- [ ] Chép lát cắt từ track: *một người dùng · một công việc · một quyết định AI · một kết quả*
- [ ] 3 việc tính năng KHÔNG làm, mỗi việc một câu lý do (kiểm lại: prototype của C không được làm những việc này)

**§2 Kịch bản rủi ro** (R2 · 10 điểm)
- [ ] ≥8 kịch bản, mỗi lớp ①②③④ ít nhất một, viết giống tin người thật
- [ ] Mỗi dòng: `tin người dùng | lớp | AI có thể sai thế nào (trỏ về tool/dữ liệu) | sản phẩm tốt nên làm gì | nhãn (nhẹ / sửa được / không chấp nhận được)`
- [ ] Có ít nhất 1 kịch bản AI **trông đúng nhưng vẫn rủi ro** (ví dụ: đúng chuyến khách cần nhưng đổi vé khi khách chưa xác nhận)
- [ ] Khoanh 2 kịch bản đắt nhất: vì sao đắt hơn các kịch bản còn lại · kịch bản nào **suýt được chọn** và vì sao không (4 điểm, dễ bỏ sót)

**§4 Mức tự chủ** (R4 · 25 điểm)
- [ ] Mọi tool có mức: tự làm / cần người duyệt / cấm
- [ ] Mỗi tool lập luận theo cost-of-error: **sai thì ai chịu gì · đảo được không · chờ người thì mất gì** (10 điểm; không viết "vì tiện", "vì AI giỏi")
- [ ] Tool cần duyệt: **ai** duyệt · người duyệt **thấy gì** · **quá hạn** thì sao (với T3: chuyến thay thế có thể hết chỗ trong lúc chờ)
- [ ] Tool khó xếp nhất: A, B, C mỗi người từng chọn gì · cái giá mỗi phía (trỏ về kịch bản §2) · nhóm chốt thế nào
- [ ] Thử mức trên **2 kịch bản đắt nhất + 1 kịch bản bình thường**, trả lời 3 câu: cái sai có bị chặn? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích?
- [ ] Luật thêm hoặc tool tách bước (ví dụ: tách "soạn yêu cầu hoàn" khỏi "gửi yêu cầu hoàn") và kịch bản nào nhờ đó bị chặn
- [ ] Một mức tự chủ đã đổi **lời hứa nào** với người dùng ("AI đổi vé giúp bạn" khác "AI soạn sẵn, bạn bấm xác nhận")

### TRƯỜNG — Câu chữ AI & UX khi sai

**§3 Khi AI sai** (R3 · 25 điểm), làm cho **từng** kịch bản trong 2 kịch bản đắt nhất:
- [ ] **AI nói gì (nguyên văn)** · người dùng **thấy gì** ngoài câu chữ (độ chắc, căn cứ, nút, nhãn) · người dùng **làm gì tiếp** · **ai được báo, sau bao lâu**, người đó thấy gì
- [ ] Quyết định **hỏi lại / trả lời kèm giới hạn / dừng và chuyển người**: chọn cách nào, **loại hai cách kia vì sao** (8 điểm, phần nặng nhất của R3)
- [ ] Loại lỗi: hệ thống / người dùng / ngữ cảnh, và vì sao cách nói xin lỗi và cách sửa đi theo loại đó
- [ ] 2–3 nguyên tắc HAX/PAIR (gợi ý: G2, G10, G9, G11, PAIR Explainability + Trust), mỗi nguyên tắc trỏ vào **một câu chữ cụ thể** → chuyển cho C để gắn vào một chỗ trên màn hình
- [ ] Một lỗi mà **sửa câu chữ không cứu được** (ví dụ: AI báo "đã hoàn vé" khi không có quyền gửi) → thiết kế cứu nó thế nào
- [ ] Nghĩ đủ 4 đường: happy path · low-confidence · không căn cứ · người dùng sửa AI

**§6 Tốt là gì** (R6 · 5 điểm)
- [ ] 3 tiêu chí Pass/Fail mà người ngoài nhóm chấm ra cùng kết quả
- [ ] Chấm thử thiết kế trên 2 kịch bản đắt nhất, ghi lỗi còn lại

**Hỗ trợ prototype:** viết toàn bộ câu chữ AI trong prototype, khớp nguyên văn với §3.

### THÀNH — Prototype & nộp bài

**Repo & nộp bài**
- [ ] Repo **mới, trống, công khai**, tên `K5-L3A-Day05-T3-TamThaiTu` (không fork repo đề) · mở thử bằng cửa sổ ẩn danh
- [ ] `spec.md` (từ `03-spec-template.md`) · bảng thành viên ở đầu · **mã học viên đúng**
- [ ] Không commit API key (nếu có, để trong biến môi trường) · chỉ dùng dữ liệu dựng

**§5 Prototype** (R5 · 25 điểm)
- [ ] 1–2 màn hình cho **ca khó nhất**. Ca này phải **khác** ca "đổi sang sáng mai" trong prototype mẫu của giảng viên
- [ ] Bấm qua được từ đầu tới cuối, không phải can thiệp tay (5 điểm)
- [ ] Thấy được **độ chắc hoặc căn cứ** AI dựa vào, ví dụ dòng chính sách hãng bay, dữ liệu đặt chỗ (4 điểm)
- [ ] Mức tự chủ hiện **đúng như §4**: tự làm có **hoàn tác** · cần duyệt có **xác nhận** · có **đường chuyển người** · việc cấm **không có nút** (6 điểm)
- [ ] 1–2 ảnh **đánh số** trong `prototype/`, mỗi số ghi: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào (6 điểm)
- [ ] Ghi §5: link/file · công cụ · phần nào mock · có gọi AI thật không · **cách hiện đã chọn, cách khác đã nghĩ tới và vì sao loại** (4 điểm)
- [ ] (Bonus +3) ≥1 lời gọi AI thật ở quyết định chính, có log hoặc ảnh, không lộ key
- [ ] Kẹt kỹ thuật quá 20 phút thì **gọi TA**

**§7 Demo**
- [ ] Viết kịch bản demo 4 phút: lát cắt (30") → bấm ca khó → một mức tự chủ và cái giá khi sai → ca lạ
- [ ] Sau demo, ghi vào §7 ca lạ đã nhận, prototype đã làm gì, nhóm có đổi ý gì không

---

## 4. Bàn giao giữa các thành viên

| Từ → Đến | Bàn giao gì | Hạn |
|---|---|---|
| A → B, C | 2 kịch bản đắt nhất (đã chốt) | Phút 45 |
| B → C | Câu AI nói nguyên văn + 2–3 nguyên tắc HAX/PAIR và chỗ trên màn hình | Phút 90 |
| A → C | Bảng mức tự chủ đã chốt (để biết nút nào có, nút nào không) | Phút 125 |
| C → A, B | Link prototype + ảnh đánh số để kiểm khớp với §3, §4 | Phút 195 |
| Cả nhóm | Đọc lại toàn bộ `spec.md`, push lên repo | Trước 23:59 |

---

## 5. Kiểm tra trước khi nộp (cả nhóm)

- [ ] Mỗi người trả lời được: *"Hành động này sai thì ai mất gì?"* · *"Lỗi nguy hiểm nhất là gì?"* · *"Phần bạn làm là gì?"*
- [ ] Mỗi người chỉ được trên màn hình: *"Chỗ nào là G__?"*
- [ ] Prototype không vi phạm 3 việc "KHÔNG làm" ở §1
- [ ] Câu chữ trong prototype khớp nguyên văn với §3; nút trên prototype khớp mức ở §4
- [ ] Bảng "Việc đã làm" trong `spec.md` ghi đúng việc thực tế của từng người
- [ ] (Bonus +5) Quyết định có xung phong demo trước lớp không: người nói chính là ______
