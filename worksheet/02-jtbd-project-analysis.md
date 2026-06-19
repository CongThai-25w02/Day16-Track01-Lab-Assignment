---
artifact: 02 — JTBD Project Analysis
bai-tap: Lab 2 — Dùng JTBD để soi lại dự án nhóm
format: Theo nhóm dự án → share trong bàn → chốt hypothesis cuối
time: 25 phút trên lớp
nop-cuoi: Có — đây là file nộp cuối của Lab 2
companion-reference: Strategyn_JTBD_Playbook.pdf (giảng viên gửi kèm)
---

# Lab 2 — JTBD Project Analysis / Dùng JTBD để soi lại dự án nhóm

**Tên dự án / sản phẩm:** RoboPlanner (AI20K‑162) — lớp thực thi agent CÓ KIỂM CHỨNG cho robot kho mô phỏng, ra lệnh bằng tiếng Việt

> Đây là **file duy nhất** của Lab 2.  
> File này đồng thời đóng vai trò:
>
> - guide từng bước,
> - worksheet để điền trực tiếp,
> - và file nộp cuối cho người chấm.

Mục tiêu của bài này không phải brainstorm thêm thật nhiều tính năng AI.
Mục tiêu là:

1. **xác định người dùng thực sự đang cố hoàn thành job gì**
2. **hiểu họ đang dùng giải pháp nào để hoàn thành job đó hôm nay**
3. **chỉ ra AI nên chen vào đúng bước nào trong workflow**
4. **viết ra product hypothesis và assumption còn phải validate**

Quy tắc xuyên suốt: **không rõ job thì đừng bàn feature.**

---

## Cần mở song song 2 thứ

1. **File này** — để điền trực tiếp
2. **`Strategyn_JTBD_Playbook.pdf`** — giảng viên gửi kèm

### Cách dùng playbook cho đúng

Bạn **không cần đọc hết 48 trang**.  
Trong bài này, playbook chủ yếu dùng để tra 4 thứ:

1. **Cách nhìn thị trường qua JTBD lens**
2. **`Job executor` là ai**
3. **Cách viết `job statement`: `verb + object + contextual clarifier`**
4. **8 bước của `job map`**:
   `define -> locate -> prepare -> confirm -> execute -> monitor -> modify -> conclude`

### 2 chương nên mở nhiều nhất

- **Chapter 2 — Define Your Market**
- **Chapter 3 — Build Your Job Map**

> Dùng playbook để **tra framework và ví dụ**.  
> Dùng file này để **làm bài và chốt output**.

---

## Đầu ra bắt buộc

Người chấm cần thấy đủ 6 phần trong chính file này:

1. **`Project slice` + market context**
2. **`Job executor` + `core JTBD`**
3. **3 `job stories`**
4. **`JTBD lite map` + pain points**
5. **`AI leverage point` + `product hypothesis`**
6. **`Assumptions to validate` + verdict cuối sau thảo luận**

Nếu thiếu một trong sáu phần trên, bài sẽ bị xem là chưa hoàn chỉnh.

---

## Cách làm trong lớp (25 phút)

```text
3'  Chốt 1 lát cắt cụ thể của dự án
7'  Viết market context + job executor + core JTBD
6'  Viết 3 job stories + current alternatives
6'  Điền JTBD lite map + AI leverage point + hypothesis
3'  Share trong bàn và sửa version cuối
```

> Nếu dự án làm theo nhóm, cả nhóm có thể thảo luận chung.  
> Nhưng file này vẫn nên có **version chốt rõ ràng** của người nộp.

---

## Bước 0 — Khoanh đúng 1 lát cắt của dự án

Phần lớn dự án nhóm viết quá rộng ở bước này, rồi sau đó mọi thứ mơ hồ theo.

### Khoanh đúng 1 lát cắt theo 4 điểm

- [x] **1 nhóm người dùng chính** → vận hành viên kho (không phải kỹ sư) ra lệnh cho robot; cùng đội QA/an toàn phải duyệt cho robot hành động
- [x] **1 hoàn cảnh / tình huống rõ** → giữa ca, bố trí kho thay đổi (vật cản tĩnh chắn lối), cần đổi nhiệm vụ robot mà không gọi kỹ sư
- [x] **1 job cốt lõi** → đưa đúng 1 vật tới đúng vị trí khi môi trường thay đổi, mà vẫn đủ tin để đưa vào quy trình thật
- [x] **1 workflow đủ cụ thể để vẽ ra được** → ra lệnh tiếng Việt → agent lập kế hoạch nhiều bước → di chuyển/né vật cản → drop đúng ô → oracle độc lập xác nhận

### Điền nhanh trước khi làm

- **Dự án của nhóm tôi là:** RoboPlanner (AI20K‑162) — một agent (LLM + LangGraph, 7 node parse→perceive→plan→act→observe→replan→summarize) lập kế hoạch tác vụ cho robot kho **mô phỏng 2D**; điểm khác biệt là **lớp thực thi CÓ KIỂM CHỨNG**: đọc trạng thái thật, trace audit được, biết "nói không" khi bất khả thi.
- **Lát cắt tôi chọn để phân tích hôm nay là:** Phạm vi đo của v2 (đã "thu nhỏ" theo mentor) — *di chuyển đúng 1 vật qua kho có chướng ngại tĩnh, drop đúng ô, oracle độc lập chấm*, kèm 2 thuộc tính bắt buộc: trace audit được và biết "nói không".
- **Vì sao tôi chọn lát cắt này:**  
  > Vì tôi phụ trách Agent core + Product nên cần nhìn rõ *job thật* nằm ở đâu chứ không chỉ ở tính năng. Lát cắt này là phần nhóm cam kết đo được bằng oracle độc lập, đủ hẹp để kiểm chứng nghiêm túc trong ~2 tuần, và là nơi lộ ra khác biệt thật của dự án (kiểm chứng được), thay vì khoe nhiều tính năng không đo được.

### Viết quá rộng vs viết sắc hơn

| Viết quá rộng | Viết sắc hơn |
|---|---|
| Giúp SME dùng AI để marketing | Giúp chủ shop online phản hồi câu hỏi trước mua hàng nhanh và nhất quán trong giờ cao điểm |
| Dùng AI để làm slide | Tạo bản nháp deck nội bộ mạch lạc cho buổi họp gấp trong thời gian rất ngắn |
| AI cho tuyển dụng | Giúp recruiter sàng lọc CV đầu vào nhanh hơn trước vòng gọi sơ bộ |

> Nếu bạn không mô tả được **một hoàn cảnh cụ thể**, khả năng cao bạn đang viết quá rộng.

---

## Bước 1 — Viết `Project Snapshot`

### Tóm tắt dự án trong 3 dòng

1. **Nhóm tôi đang nghĩ mình đang giải quyết vấn đề gì?**  
   > Điều khiển robot kho hôm nay phải lập trình từng bước, vỡ khi môi trường đổi, và là hộp đen nên đội an toàn/QA không dám đưa vào quy trình thật. Rào cản số 1 không phải "model đủ thông minh chưa" mà là "có audit được, có dám tin không".

2. **Người dùng chính hiện nhóm đang nhắm tới là ai?**  
   > Vận hành viên kho/nhà máy muốn điều khiển robot bằng ngôn ngữ thay vì lập trình. Phụ: kỹ sư tích hợp (prototype logic nhiệm vụ) và đội an toàn/QA cần kế hoạch kiểm chứng được.

3. **Hiện tại người dùng đó đang giải quyết vấn đề này bằng cách nào?**  
   > Lập trình cứng từng bước / teach‑pendant + luật WMS cố định; mỗi lần bố trí đổi thì gọi kỹ sư lập lại; muốn "thông minh" thì thử gọi LLM trần — nhưng LLM trần bịa kết quả nên QA không duyệt.

---

## Bước 2 — Viết `Market Context`

Ở đây chưa cần solution. Chỉ cần bối cảnh thị trường đủ để hiểu:
**ai đang gặp chuyện gì, trong hoàn cảnh nào, và vì sao bây giờ đáng giải.**

### Trả lời 4 câu ngắn

1. **Ai đang gặp vấn đề này?**  
   > Kho/nhà máy dùng robot di chuyển hàng: vận hành viên (không phải kỹ sư) phải chạy nhiệm vụ hằng ngày, và đội an toàn/QA phải chịu trách nhiệm khi cho robot hành động.

2. **Vấn đề xuất hiện trong hoàn cảnh nào?**  
   > Khi bố trí kho thay đổi (vật cản, pallet, lối đi đổi) làm kịch bản lập sẵn vỡ; khi cần đổi nhiệm vụ gấp; và khi phải chứng minh cho QA rằng robot làm đúng & an toàn trước khi đưa vào quy trình thật.

3. **Hiện tại họ đang dùng giải pháp thay thế nào?**  
   > Lập trình cứng từng bước + luật cố định; gọi kỹ sư mỗi khi đổi; hoặc thử một lời gọi LLM không grounding (không đọc trạng thái thật, không audit được).

4. **Vì sao đây là thời điểm đáng giải?**  
   > "Bộ não" (LLM) giờ là commodity, đủ rẻ để lập & sửa kế hoạch theo ngôn ngữ tự nhiên. Thứ còn thiếu để deploy không phải model giỏi hơn, mà là **lớp thực thi đáng tin** quanh nó (grounded + trace + oracle). Đây là khoảng trống mà dự án nhắm vào.

### Tóm tắt market context trong 3-4 dòng

> Robot kho hiện cứng nhắc và là hộp đen, nên mỗi thay đổi đều tốn kỹ sư còn đội rủi ro thì không dám ký duyệt.  
> Mặt khác, agent LLM tuy hiểu ngôn ngữ và biết lập kế hoạch nhưng hay "bịa", nên không qua được cửa compliance. Điểm đáng giải bây giờ là biến agent thành thứ **audit được + không hallucinate**, vì đó mới là điều kiện để doanh nghiệp dám đưa vào sản xuất.

---

## Bước 3 — Xác định `Job Executor`

`Job executor` là người **trực tiếp dùng một giải pháp để hoàn thành job**.

### Đừng nhầm với:

- người mua tiền nhưng không trực tiếp làm job
- người ảnh hưởng quyết định
- cả một công ty hay một phòng ban quá rộng

### Gợi ý viết cho đúng

- Sai hoặc quá rộng: `SME`, `doanh nghiệp`, `thị trường`
- Tốt hơn: `chủ shop online`, `nhân viên CSKH`, `recruiter`, `sales ops manager`

### Điền

- **Job executor của dự án này là:** Vận hành viên kho ra lệnh cho robot (người trực tiếp gõ "đưa pallet A tới chuyền 3" và cần việc được làm). **Lưu ý quan trọng nổi lên khi soi JTBD:** người trực tiếp làm *job kiểm chứng* — tức "đọc trace, xác nhận và dám ký duyệt cho agent hành động" — lại là **đội QA/an toàn (người duyệt deploy)**. Đây mới là executor của phần giá trị lõi (lớp kiểm chứng) của dự án.
- **Vì sao tôi tin đây là người trực tiếp "thuê" giải pháp để làm job:**  
  > Vận hành viên là người trực tiếp ra lệnh và chịu việc kẹt khi robot vỡ kịch bản, nên họ "thuê" agent để hoàn thành cú di chuyển. Nhưng lớp differentiator (grounded + trace + abstain) lại được **QA/đội rủi ro** "thuê" để làm job của họ: tin và ký duyệt mà vẫn truy được trách nhiệm. Dự án thực ra phục vụ 2 executor, và phần khó nhất là làm hài lòng người duyệt.

---

## Bước 4 — Viết `Core JTBD`

`Core JTBD` là công việc cốt lõi người dùng đang cố hoàn thành.

### Công thức gợi ý

```text
[verb] + [object] + [contextual clarifier]
```

### Ví dụ

- Chưa tốt: `trả lời inbox bằng AI`
- Tốt hơn: `giải quyết câu hỏi trước mua hàng nhanh và chính xác trong giờ cao điểm`

- Chưa tốt: `dùng AI để viết nội dung`
- Tốt hơn: `tạo bản nháp nội dung chiến dịch phù hợp với brand trong thời gian rất ngắn`

### 3 tiêu chí tự kiểm

- [x] Nếu bỏ tool hiện tại đi, job này vẫn còn tồn tại
- [x] Trong câu không có tên sản phẩm, AI, chatbot, app, màn hình
- [x] Câu đang mô tả **điều user muốn hoàn thành**, không phải thứ product đang làm

### Bản nháp 1

**Core JTBD bản nháp:**  
> Dùng agent LLM để điều khiển robot kho bằng tiếng Việt.

### Gạch bỏ từ solution nếu có

- Các từ solution tôi đang lỡ nhét vào câu: "agent LLM", "robot", "bằng tiếng Việt" (đây là solution và giao diện đầu vào, không phải job). Ngôn ngữ tự nhiên là *cách ra lệnh*, không phải điều user muốn hoàn thành.

### Bản chốt

**Core JTBD cuối cùng:**  
> Đưa đúng hàng tới đúng vị trí trong kho khi bố trí liên tục thay đổi, mà không phải lập trình lại từng bước và vẫn kiểm soát được rủi ro để dám đưa vào quy trình thật.

---

## Bước 5 — Viết 3 `Job Stories`

Nếu `core JTBD` là job ở mức cốt lõi, thì `job story` giúp bạn thấy
**job này xuất hiện trong hoàn cảnh nào**.

### Format

```text
When [trigger], I want to [motivation], so I can [outcome].
```

### Ví dụ

`When inbox đổ dồn vào buổi tối, tôi muốn có câu trả lời nhất quán ngay lập tức, so I can không mất đơn vì phản hồi chậm.`

### Bảng 3 job stories

| # | Trigger / When | Motivation / I want to | Outcome / so I can | Điều story này cho thấy |
|---|---|---|---|---|
| JS1 | Giữa ca có vật cản/pallet lạ chắn lối robot vẫn quen chạy | Ra lệnh lại bằng tiếng Việt và để robot tự tìm đường vòng | Không phải gọi kỹ sư và không dừng cả dây chuyền | Pain ở môi trường động — chỗ kịch bản cứng vỡ |
| JS2 | Cần đổi nhiệm vụ robot ("đưa pallet A tới chuyền 3") mà tôi không biết lập trình | Gõ/nói bằng tiếng Việt là robot hiểu và làm | Tự điều việc mà không phụ thuộc kỹ sư | Pain ở rào cản ngôn ngữ / không lập trình được |
| JS3 | Robot báo "đã xong" một nhiệm vụ sắp đưa vào quy trình thật | (QA) xem lại từng bước nó đọc gì–làm gì kèm bằng chứng độc lập | Dám ký duyệt và vẫn truy được trách nhiệm khi có sự cố | Pain ở niềm tin/audit — chính là moat của dự án |

### Tự kiểm nhanh

- [x] Mỗi story là một **tình huống thật**, không phải slogan chung chung
- [x] 3 story không trùng hệt nhau (môi trường động / rào cản ngôn ngữ / niềm tin–audit)
- [x] Sau khi đọc 3 story, tôi hình dung được lúc nào product của mình đáng xuất hiện

---

## Bước 6 — Liệt kê `Current Alternatives`

Qua JTBD lens, đối thủ không chỉ là app cùng ngành.
Đối thủ là **bất kỳ thứ gì user đang "thuê" để làm job**:

- thao tác tay
- file Excel / Google Sheets
- intern / nhân viên
- agency
- ChatGPT / Claude / Gemini
- công cụ chuyên dụng khác
- hoặc thậm chí là **không làm gì cả**

### Bảng alternatives

| Alternative hiện tại | User đang thuê nó để làm gì? | Nó làm tốt gì? | Nó fail ở đâu? | Switching cost hiện tại cao hay thấp? |
|---|---|---|---|---|
| Lập trình cứng từng bước / teach‑pendant + luật WMS cố định | Cho robot chạy đúng tuyến đã định | Ổn định, tất định, dễ chứng nhận an toàn trong môi trường tĩnh | Vỡ khi bố trí đổi; mỗi thay đổi phải gọi kỹ sư; vận hành viên không tự đổi được | Cao (đã tích hợp, đội an toàn đã duyệt) |
| Gọi kỹ sư tích hợp mỗi khi cần đổi nhiệm vụ/đường đi | Xử lý ca mới ngoài kịch bản | Linh hoạt theo người, đúng bối cảnh cụ thể | Chậm, tốn tiền, gây downtime; không scale | Trung bình |
| Một lời gọi LLM trần (không grounding) | Thử cho agent "thông minh" tự sinh kế hoạch | Hiểu ngôn ngữ, ra kế hoạch nhanh | Bịa kết quả, không đọc trạng thái thật, không audit được → QA không bao giờ duyệt | Thấp về tiền, nhưng **không deploy nổi** |

### Kết luận nhanh

**Nếu project của tôi biến mất hôm nay, user nhiều khả năng sẽ quay về:**  
> Lập trình cứng + gọi kỹ sư khi cần đổi (Alt 1 + Alt 2) — chấp nhận cứng nhắc và tốn người để đổi lấy thứ đội an toàn đã duyệt. Baseline mà RoboPlanner phải vượt là: vừa linh hoạt (đổi bằng lời, tự replan) **vừa đủ tin để duyệt** — không alternative nào hiện có cả hai.

---

## Bước 7 — Điền `JTBD Lite Map`

Đây là bản rút gọn của `job map` trong playbook.

### Mục tiêu

Không phải để làm consultant workshop hoàn chỉnh.  
Mục tiêu là nhìn ra:

1. workflow hiện tại của user đi qua những bước nào
2. bước nào đang đau nhất
3. AI có nên chen vào đó không

### 8 bước tham chiếu từ playbook

1. `Define`
2. `Locate`
3. `Prepare`
4. `Confirm`
5. `Execute`
6. `Monitor`
7. `Modify`
8. `Conclude`

> Không nhất thiết bước nào cũng quan trọng như nhau trong dự án của bạn.  
> Nếu ít liên quan, ghi `N/A`, đừng để trống.

### Bảng JTBD Lite Map

| Step | Trong workflow này user đang cố làm gì? | Hôm nay họ đang dùng gì? | Friction / pain hiện tại | Mức đau |
|---|---|---|---|---|
| Define | Diễn đạt nhiệm vụ ("đưa pallet A tới chuyền 3") cho robot hiểu | Vận hành viên mô tả → kỹ sư dịch sang mã | Rào cản ngôn ngữ: không tự ra lệnh được, phải qua kỹ sư | High |
| Locate | Xác định vật đích và ô/khu đích trong không gian | Kỹ sư mã hóa tọa độ; vận hành viên ước lượng bằng mắt | Mapping thủ công, dễ sai tên/vị trí | Med |
| Prepare | Lập đường đi né chướng ngại trước khi chạy | Tuyến cố định lập sẵn | Tuyến cứng, không tự né khi có vật cản mới | High |
| Confirm | Kiểm kế hoạch có hợp lệ/khả thi/an toàn trước khi chạy | Tin chương trình hoặc nhờ kỹ sư review | Hộp đen — không tự kiểm được; không biết khi nào bất khả thi | High |
| Execute | Di chuyển / pick / drop tới đích | Robot chạy script (`move_to·pick·drop`) | Cứng nhắc; lệch một chút là fail, không tự xoay | Med |
| Monitor | Theo dõi robot có đang làm đúng & đọc đúng trạng thái thật | Camera, người đứng nhìn, status robot tự khai | Không tin status tự khai; thiếu trace từng bước để soi | High |
| Modify | Lập lại kế hoạch khi vật cản xuất hiện / bố trí đổi | Dừng, gọi kỹ sư, lập trình lại | Chậm, tốn tiền, downtime; thường phải dừng việc | High |
| Conclude | Xác nhận đã xong đúng + có bằng chứng để audit | Tin robot báo "done"; ít log audit | Không có xác nhận độc lập; QA thiếu hồ sơ để ký duyệt | High |

### Chốt 2 bước đau nhất

**Bước đau nhất #1:** Confirm + Monitor + Conclude — tin & kiểm chứng được robot đang/đã làm đúng (hộp đen, không audit được)  
**Bước đau nhất #2:** Modify — lập lại kế hoạch khi môi trường đổi mà không phải gọi kỹ sư lập trình lại

**Vì sao đây là nơi đáng chú ý nhất:**  
> Theo chính luận điểm của nhóm, rào cản số 1 để deploy không phải model giỏi hơn mà là **audit được + dám tin** — pain này nằm ở cụm Confirm/Monitor/Conclude.  
> Modify là pain vận hành tốn kém nhất (downtime + kỹ sư). Giải được 2 cụm này thì agent mới vừa linh hoạt vừa qua được cửa compliance — đúng chỗ không alternative nào làm được.

---

## Bước 8 — Chỉ ra `AI Leverage Point`

Sau khi map workflow, mới hỏi:
**AI nên vào đâu, với vai trò gì, và vì sao là ở đó?**

### Nhắc nhanh

- Đừng nhét AI vào chỉ vì "có AI thì nghe hay"
- Nếu pain lớn nhất không nằm ở chỗ AI giải tốt, hãy thành thật ghi ra
- Nếu current alternative đã đủ tốt, project cần xem lại

### Bảng leverage point

| Step | AI nên giúp bằng cách nào? | Vì sao AI hợp ở đây? | Rủi ro chính nếu dùng AI |
|---|---|---|---|
| Confirm / Monitor / Conclude (lớp kiểm chứng) | Mọi tool‑call đọc trạng thái thật từ sim (grounded); hiển thị trace *suy nghĩ → tool → tham số → kết quả*; oracle độc lập chấm; biết "nói không" khi bất khả thi | Agent LLM vừa hành động vừa giải thích được từng bước bằng ngôn ngữ; cặp grounding + oracle biến hộp đen thành thứ audit được — đúng điều QA cần để ký duyệt | Nếu grounding/trace sai hoặc agent bịa "done" thì niềm tin sụp — đúng là bug đang làm Bảng A = 0% hiện nay |
| Modify (replan) | Khi gặp vật cản, agent lập lại đường đi từ trạng thái thật hiện tại, không cần lập trình lại | Lập kế hoạch từ mục tiêu + quan sát chính là vòng lặp agent (parse→plan→act→observe→replan) | Replan có thể vi phạm ràng buộc ngầm/an toàn; latency cao (~6s/bước) chưa đạt mục tiêu <3s |

### Kết luận nhanh

**AI leverage point quan trọng nhất của dự án tôi là:**  
> Lớp thực thi **CÓ KIỂM CHỨNG** ở cụm Confirm/Monitor/Conclude — grounded + trace audit được + biết "nói không". Đây là chỗ biến agent từ "thông minh nhưng không ai dám dùng" thành "dám đưa vào quy trình thật".

**Vì sao không phải ở bước khác:**  
> Vì "bộ não" (khả năng lập kế hoạch của LLM) là **commodity** — ai cũng gọi được model. Giao diện ra lệnh tiếng Việt chỉ là input, dễ sao chép. Tốc độ thực thi cũng không phải điểm khác biệt. Thứ tạo giá trị deploy được và khó sao chép chính là làm cho hành động của agent **đáng tin và audit được** — nên leverage phải đặt ở đó.

---

## Bước 9 — Viết `Product Hypothesis`

Bây giờ mới đến lúc viết hypothesis.

### Công thức gợi ý

```text
Nếu chúng ta giúp [job executor] làm [job / sub-job] tốt hơn ở bước [x],
bằng cách [AI leverage],
thì họ sẽ chuyển từ [current alternative] sang [hướng giải pháp của nhóm],
vì [giá trị rõ nhất].
```

### Bản hypothesis của tôi

> Nếu chúng ta giúp **vận hành viên kho và đội QA/an toàn** tin và kiểm chứng được hành động của robot ở **bước Confirm/Monitor/Conclude**, bằng cách **mọi hành động đọc trạng thái thật + trace audit từng bước + oracle độc lập chấm + biết "nói không" khi bất khả thi**,  
> thì họ sẽ chuyển từ **lập trình cứng + gọi kỹ sư (hộp đen)** sang **để agent tự lập kế hoạch nhưng có kiểm chứng**, vì **lần đầu họ dám đưa agent vào quy trình thật mà vẫn audit được khi có sự cố**.

### Tín hiệu sớm nếu hypothesis này đúng

1. QA/đội rủi ro chấm "trace đủ để hiểu & tin" đạt ngưỡng (audit pass ≥ 90% theo rubric cố định) trên mẫu ca thật.
2. Tỷ lệ hành động grounded ≥ 95% và hallucinated‑done = 0% giữ ổn định qua nhiều seed → người duyệt bắt đầu ký duyệt đề xuất của agent mà không cần sửa.

---

## Bước 10 — Liệt kê `Assumptions to Validate`

Job story chưa có research vẫn chỉ là **giả thuyết tốt hơn**, chưa phải sự thật.

### 5 assumption thường đáng kiểm

- Tôi đã chọn đúng `job executor`
- Pain này thật sự đủ đau và xảy ra đủ thường xuyên
- User sẽ đổi khỏi alternative hiện tại nếu có giải pháp tốt hơn
- AI thực sự tạo giá trị ở step tôi chọn
- User đủ tin kết quả AI để đưa vào workflow thật

### Bảng assumptions

| Assumption | Vì sao assumption này rủi ro? | Tôi đang có bằng chứng gì? | Cần validate bằng cách nào tiếp theo? |
|---|---|---|---|
| A1 — Người thật sự "thuê" lớp kiểm chứng là ai (vận hành viên hay QA/người duyệt) | Đang dồn UX cho vận hành viên, trong khi người quyết deploy lại là đội rủi ro → xây cho nhầm người | Pilot proposal đã nghiêng về người duyệt; chưa có phỏng vấn thật | Phỏng vấn cả 2 vai; xác định ai là người ký duyệt đưa agent vào quy trình |
| A2 — Pain "hộp đen, không dám tin" đủ lớn để đổi | Có thể doanh nghiệp tắc vì thiếu người chứ không phải vì compliance | Luận điểm nhóm + tiêu chí chọn pilot (quy trình đang tắc vì compliance) | Chọn quy trình có ground truth, sai đo được bằng tiền/thời gian; hỏi xem có thật đang tắc vì compliance |
| A3 — "Audit được + không bịa" là điều kiện để mua, không phải nice‑to‑have | Nếu chỉ là "thích thì tốt", giá trị không đủ để trả tiền | Chưa có người mua doanh nghiệp trả tiền | Pilot 90 ngày, đo % đề xuất được ký duyệt lên production (mục tiêu ≥70%) |
| A4 — Agent lõi thật sự chạy được end‑to‑end (sinh tool‑call hợp lệ, tới đích) | Bảng A (agent thật) hiện success = 0% do bug function‑calling; chưa có gì để "kiểm chứng" nếu agent không hành động được | Đã xác định root cause + vá P0‑1; abstain đúng 2/2; hallucinated‑done = 0% | Chạy lại eval đa seed (`run_eval_v2.py --seeds 3`) tới khi success > 0 ổn định |
| A5 — Phương pháp (grounded+trace+oracle) chuyển được từ robot sim sang nghiệp vụ thật | Domain chứng minh là robot kho, nhưng giá trị bán lại ở quy trình nghiệp vụ (đối soát/duyệt) | Chưa de‑risk; mới là proof‑of‑method | Pilot shadow mode trên dữ liệu lịch sử 1 quy trình; dựng oracle từ ground truth khách |

### Assumption nguy hiểm nhất nếu tôi đang sai

> Trước mắt (chặn cứng): **A4** — agent lõi đang 0% (Bảng A). Nếu agent không tự sinh được hành động hợp lệ thì cả lớp kiểm chứng không có gì để kiểm; đây cũng là Ưu tiên #1 của nhóm.  
> Ở tầng JTBD/sản phẩm: **A1** — nếu chọn nhầm job executor (xây cho vận hành viên trong khi người thật sự "thuê" lớp kiểm chứng là đội duyệt/rủi ro) thì sản phẩm tối ưu sai người và cả hypothesis lệch theo.

---

## Bước 11 — Share trong bàn (3')

### Mỗi người / mỗi nhóm chỉ nói 4 thứ

1. **Job executor của bạn là ai**
2. **Core JTBD của bạn là gì**
3. **Step đau nhất đang nằm ở đâu**
4. **AI leverage point + assumption rủi ro nhất là gì**

### Nếu chưa biết hỏi ngược gì, dùng 4 câu này

1. **"Câu JTBD này có đang lỡ nhét solution vào không?"**
2. **"Alternative hiện tại của user là gì, và tại sao họ chưa bỏ nó?"**
3. **"Pain mạnh nhất nằm ở bước nào trong workflow, có chắc AI giải tốt được không?"**
4. **"Assumption nào nếu sai thì cả hypothesis sẽ sập?"**

### Ghi nhanh sau khi nghe bàn phản biện

| Ý phản biện tôi nghe được | Nó chạm vào phần nào? | Tôi sẽ giữ / sửa gì? |
|---|---|---|
| "Job executor là vận hành viên hay đội QA? Người ký duyệt deploy mới là người thật sự mua lớp kiểm chứng." | A1 + job executor | Sửa: nâng QA/người duyệt thành executor của job kiểm chứng; vận hành viên là người dùng giao diện ra lệnh |
| "Agent đang 0% (Bảng A) — nói 'auditable' lúc này có sớm không?" | A4 + AI leverage point | Giữ leverage point nhưng đặt cổng: phải có success > 0 ổn định rồi mới được tuyên bố moat |
| "Robot kho sim có thuyết phục người mua nghiệp vụ không? Có nên chuyển hẳn sang đối soát/duyệt?" | A5 + market context | Giữ sim làm proof‑of‑method; định vị pilot ở quy trình back‑office (đã có trong PILOT_PROPOSAL) |

---

## Bước 12 — Chốt version cuối sau thảo luận

### Sau khi nghe phản biện, tôi thay đổi gì?

- [ ] Giữ nguyên `job executor`
- [x] Sửa `job executor`
- [x] Giữ nguyên `core JTBD`
- [ ] Sửa `core JTBD`
- [ ] Giữ nguyên `AI leverage point`
- [x] Sửa `AI leverage point`
- [x] Giữ nguyên `product hypothesis`
- [ ] Sửa `product hypothesis`

### Vì sao tôi giữ / sửa?

> Sửa **job executor**: tách rõ hai vai — vận hành viên (người ra lệnh) và QA/người duyệt (người thật sự "thuê" lớp kiểm chứng và quyết định deploy). Phần giá trị lõi phục vụ vai thứ hai.  
> Giữ **core JTBD** vì qua phản biện vẫn đứng vững (đưa hàng đúng chỗ khi môi trường đổi, kiểm soát được rủi ro).  
> Sửa **AI leverage point**: nhấn rõ lớp kiểm chứng là moat, nhưng thêm cổng "agent phải có success > 0 trước khi tuyên bố".  
> Giữ **product hypothesis** về bản chất (chỉ bổ sung vai QA cho rõ).

### Version cuối cùng tôi nộp

**Job executor:**  
> Vận hành viên kho (người ra lệnh tiếng Việt) — và quan trọng hơn cho phần lõi: đội QA/an toàn (người duyệt cho agent hành động) là executor của job kiểm chứng.

**Core JTBD:**  
> Đưa đúng hàng tới đúng vị trí trong kho khi bố trí liên tục thay đổi, mà không phải lập trình lại từng bước và vẫn kiểm soát được rủi ro để dám đưa vào quy trình thật.

**2 bước đau nhất trong workflow:**  
> Confirm/Monitor/Conclude (tin & kiểm chứng được robot làm đúng) và Modify (replan khi môi trường đổi).

**AI leverage point chính:**  
> Lớp thực thi CÓ KIỂM CHỨNG: mọi hành động đọc trạng thái thật (grounded) + trace audit từng bước + oracle độc lập chấm + biết "nói không" khi bất khả thi.

**Product hypothesis:**  
> Nếu giúp vận hành viên + QA tin và kiểm chứng được hành động robot ở bước Confirm/Monitor/Conclude — grounded + trace + oracle + abstain — thì họ chuyển từ lập trình cứng/hộp đen sang agent có kiểm chứng, vì lần đầu dám đưa agent vào quy trình thật mà vẫn audit được.

**Assumption cần validate đầu tiên:**  
> A4 — vá xong bug function‑calling, chạy lại eval đa seed để Bảng A có success > 0 ổn định (vì nếu agent lõi chưa chạy thì không có gì để kiểm chứng).

---

## Checklist trước khi nộp

- [x] Tôi đã khoanh đúng 1 lát cắt cụ thể của dự án.
- [x] Tôi đã phân biệt được `job executor` với buyer / influencer.
- [x] `Core JTBD` của tôi không nhét solution vào câu.
- [x] Tôi đã viết đủ 3 `job stories`.
- [x] Tôi đã điền `JTBD lite map` và khoanh ra 2 bước đau nhất.
- [x] Tôi đã chỉ ra `AI leverage point` thay vì nhảy thẳng vào feature list.
- [x] Tôi đã ghi rõ `assumptions to validate`.
- [x] Tôi đã sửa version cuối sau khi share trong bàn.

---

## Nếu còn thời gian / làm về nhà

- Phỏng vấn nhanh 1 người dùng thật để kiểm xem `job story` nào là sát nhất.
- So sánh `current alternatives` với project của nhóm theo 3 tiêu chí: nhanh hơn, rẻ hơn, tin hơn.
- Tự hỏi lại một câu khó: **nếu không dùng AI, project này còn tạo giá trị không?**
- Nếu câu trả lời là "không", hãy xem lại liệu nhóm đang giải **job thật** hay chỉ đang tìm chỗ để nhét AI.

> **Trả lời câu hỏi khó cho dự án này:** Job "đưa hàng đúng chỗ trong kho đang thay đổi, đủ tin để đưa vào quy trình thật" tồn tại độc lập với AI — hôm nay vẫn đang được giải bằng lập trình cứng + kỹ sư. AI (agent có kiểm chứng) là cách giải mới cho phép đổi bằng lời + tự replan + vẫn audit được.  
> **Cảnh báo trung thực:** nếu bỏ phần "có kiểm chứng" (grounded/trace/abstain) thì chỉ còn "một lời gọi LLM" — không tạo được giá trị deploy. Vậy giá trị thật của dự án nằm ở **lớp kiểm chứng**, không phải ở việc "có AI". Đây đúng là lý do nhóm đặt North Star là "lớp thực thi CÓ KIỂM CHỨNG" thay vì "AI điều khiển robot" — tín hiệu cho thấy nhóm đang giải job thật, AI chỉ là phương tiện. (So sánh nhanh theo 3 tiêu chí: **nhanh hơn** lập trình lại bằng tay khi đổi việc; chưa chắc **rẻ hơn** lúc đầu; ăn điểm ở **tin hơn** nhờ audit — nhưng chỉ đúng khi A4 được giải.)
