---
artifact: 01 — Case Analysis
bai-tap: Lab 1 — Phân tích "tử huyệt" chiến lược
format: Cá nhân trước → share trong bàn → chốt verdict cuối
time: 20 phút trên lớp
nop-cuoi: Có — đây là file nộp cuối của Lab 1
---

# Lab 1 — Case Analysis / Phân tích "tử huyệt" chiến lược

**Case đã chọn:** Stack Overflow
**Người làm:** Công Thái 
**Bàn / nhóm bàn:** Không tên
**Ngày:** 06/18/2026

> Đây là **file duy nhất** của Lab 1.  
> File này đồng thời đóng vai trò:
>
> - guide từng bước,
> - worksheet để điền trực tiếp,
> - và file nộp cuối cho người chấm.

Mục tiêu của bài này không phải kể lại "AI đã giết một công ty". Mục tiêu là chỉ ra, bằng bằng chứng thật:

1. **vì sao case đó bị tổn thương trước AI**
   Thao tác rườm rà và Tiện lợi tức thì: Trước AI, để có câu trả lời trên Stack Overflow, lập trình viên phải rời môi trường viết code (IDE), lên trình duyệt, gõ tìm kiếm, hoặc phải tự viết câu hỏi (định dạng code chuẩn, giải thích mạch lạc) rồi ngồi đợi. Với AI Assistants, họ có thể chat trực tiếp ngay trong IDE (như Cursor, Copilot), copy đoạn code lỗi thô ráp vào và nhận kết quả sửa sau 3 giây.
2. **điều gì đã thay đổi vĩnh viễn**
- Lập trình viên hiện tại sử dụng AI trực tiếp ngay trong môi trường gõ code (nhúng trong IDE như Cursor, VS Code). Họ không đi tìm kiến thức nữa, mà kiến thức tự động "phục vụ" tận nơi. Thói quen click vào các liên kết website truyền thống để đọc tài liệu đã bị cắt đứt vĩnh viễn.
- 
4. **và nếu rút một cảnh báo cho dự án của nhóm mình thì đó là gì**

Quy tắc xuyên suốt: **không có bằng chứng = không có nhận định.**

---

## Đầu ra bắt buộc

Người chấm cần thấy đủ 4 phần trong chính file này:

1. **3-5 bằng chứng chốt**
2. **4 nhận định bắt buộc**
3. **ghi chú sau khi share trong bàn**
4. **verdict cuối của cá nhân**

Nếu thiếu một trong bốn phần trên, bài sẽ bị xem là chưa hoàn chỉnh.

---

## Cách làm trong lớp (20 phút)

```text
2'  Chọn case
8'  Làm cá nhân: gom bằng chứng + viết 4 nhận định
7'  Share trong bàn: 90 giây / người + hỏi vặn lại
3'  Tự sửa verdict cá nhân sau thảo luận
```

---

## Bước 0 — Chọn case thật nhanh

Mặc định: **bạn tự chọn case của mình**.

### Một case phù hợp cần có 4 điều

- [ ] Có một **AI shock** hoặc mốc đổi cục diện đủ rõ
- [ ] Có thể tìm được ít nhất **3-5 bằng chứng công khai**
- [ ] Có tác động đủ nhìn thấy được ở user / doanh thu / pricing / traffic / cổ phiếu / usage / vị thế cạnh tranh
- [ ] Có thể trả lời câu hỏi: **"Điều gì đã thay đổi vĩnh viễn?"**

### Điền nhanh trước khi làm

- **Case / sản phẩm / công ty:** Stack Overflow
- **AI / platform / sản phẩm mới tạo áp lực:** ChatGPT (OpenAI) & Claude (Anthropic)
- **Vì sao tôi chọn case này?**  
  > Sự sụt giảm lượng câu hỏi từ hàng trăm nghìn xuống mức thấp kỷ lục là một minh chứng định lượng (quantitative chứng cứ) hoàn hảo, trực quan nhất cho khái niệm "AI Disruption" mà không ai có thể tranh cãi.

### Nếu bí case, chọn 1 trong 6 case gợi ý này

| Case | Vì sao đáng phân tích | Một tín hiệu đáng chú ý |
|---|---|---|
| Chegg | entry point học tập đổi rất nhanh | 7,8M → 3,2M thuê bao |
| Stack Overflow | hiệu ứng mạng bị đảo chiều | câu hỏi mới giảm mạnh sau ChatGPT |
| Jasper | lớp vỏ dễ bị generic AI ép | định giá và tăng trưởng chậm lại sau ChatGPT |
| Tome | AI phổ thông "đủ tốt" làm phân khúc cũ yếu đi | nhiều đợt cắt giảm và pivot |
| Inflection / Pi | chatbot tiêu dùng bị ông lớn lấn át | đội ngũ chuyển sang Microsoft |
| Figma / Claude Design | rủi ro "đất thuê" khi platform bước xuống app layer | cổ phiếu Figma phản ứng tiêu cực khi Claude Design ra mắt |

> Nếu có case riêng rõ hơn, dùng case riêng.

---

## Bước 1 — Gom 3-5 bằng chứng chốt

Không cần chép lại mọi số. Chỉ giữ những bằng chứng đủ mạnh để đỡ toàn bộ lập luận của bạn.

### Tìm bằng chứng theo 4 cụm

1. **Case trước AI**
   Sản phẩm là gì, user là ai, họ trả tiền cho cái gì, case từng thắng nhờ gì.

2. **AI shock**
   Mốc Big Tech AI / platform AI / sản phẩm mới xuất hiện và đổi luật chơi.

3. **Tác động quan sát được**
   User, doanh thu, ARR, pricing, traffic, usage, cổ phiếu, sa thải, pivot.

4. **Cục diện mới của thị trường**
   Ai phản ứng tốt hơn, ai thay thế tốt hơn, entry point mới nằm ở đâu, phân khúc còn sống không.

### Ưu tiên nguồn thế nào?

| Mức ưu tiên | Loại nguồn | Ví dụ |
|---|---|---|
| 1 | Nguồn gốc | báo cáo tài chính, investor relations, pricing page, blog chính thức |
| 2 | Báo uy tín | Reuters, CNBC, Bloomberg, FT, TechCrunch |
| 3 | Dữ liệu công khai / tổng hợp | MacroTrends, Similarweb, Stack Overflow Survey, Sacra |

### Bảng bằng chứng chốt

| # | Bằng chứng / số liệu chốt | Vì sao số này quan trọng? | Nguồn |
|---|---|---|---|
| E1 | Kho dữ liệu của Stack Overflow đạt hơn 24 triệu câu hỏi và 35 triệu câu trả lời tích lũy trong 15 năm, với hệ thống điểm uy tín (Reputation System) khắt khe đẩy câu trả lời tối ưu lên top 1 Google SEO. | Chứng minh "Moat" (lợi thế cạnh tranh) cực mạnh của mô hình cũ dựa trên tri thức cộng đồng do con người tự tạo (UGC) và sự phụ thuộc hoàn toàn vào luồng kéo traffic từ Google. | Stack Overflow Official Data / Similarweb |
| E2 | Lượng câu hỏi mới hàng tháng sụt giảm nghiêm trọng từ đỉnh hơn 200.000 câu hỏi xuống chỉ còn vài ngàn. Song song đó, 84% lập trình viên chuyên nghiệp thừa nhận đã đưa các công cụ GenAI vào workflow hàng ngày. | Đây là bằng chứng định lượng trực diện nhất cho thấy hành vi tra cứu của dev đã dịch chuyển vĩnh viễn: từ chủ động "đi tìm link" sang "đón nhận câu trả lời" ngay trong IDE.| Stack Overflow Developer Survey / Sacra |
| E3 | Mức độ tin tưởng của lập trình viên vào tính chính xác của code do AI sinh ra sụt giảm từ 40% xuống còn 29% do hiện trạng AI ảo tưởng (hallucination) và sinh code lỗi hệ thống. | Khẳng định phân khúc tri thức gốc của con người chưa chết. AI chỉ giải quyết phần ngọn (code thô), còn Stack Overflow đóng vai trò là "lưới lọc xác minh" (verification layer) cuối cùng khi hệ thống gặp sự cố lớn.| Stack Overflow Developer Survey |
| E4 | Stack Overflow ký các thỏa thuận thương mại API trị giá hàng chục triệu USD với OpenAI và Google, đồng thời tích hợp Stack Overflow MCP Server trực tiếp vào hệ sinh thái AI Agent. | Minh chứng cho cú Pivot (chuyển mình) sống còn về mô hình doanh thu: Từ một nền tảng bán quảng cáo ăn theo traffic (B2C) thành một "trạm cấp dữ liệu thô độc quyền" (B2B) cho chính các Big Tech. | Reuters / TechCrunch / Blog chính thức của Stack Overflow |
| E5 | | | |

### 3 phát hiện ban đầu

Trước khi viết nhận định, ghi nhanh 3 dòng:

1. **Case này từng thắng nhờ...**  
   > Lợi thế mạng lưới khổng lồ (Network Effects) từ kho tri thức đóng góp miễn phí của con người
2. **AI shock làm thay đổi...**  
   > Điểm chạm tra cứu (Entry point) của người dùng: Kiến thức được AI chủ động "đẩy" (Push) trực tiếp vào môi trường gõ code (IDE) thời gian thực, triệt tiêu hoàn toàn nhu cầu "kéo" (Pull) traffic thủ công bằng cách click vào website truyền thống.
3. **Dấu hiệu mạnh nhất cho thấy luật chơi mới là...**  
   > Sự dịch chuyển giá trị lõi của sản phẩm: Bản thân trang web Stack Overflow không còn là đích đến của người dùng cuối, mà trở thành hạ tầng ngầm (Back-end data infrastructure) cung cấp nguyên liệu sạch để huấn luyện và định hướng cho các AI Agent.

---

## Bước 2 — Viết 4 nhận định bắt buộc

### Nhận định 1 — Trước AI, case này thắng nhờ giả định gì?

Gợi ý:

- Người dùng thuê sản phẩm này để làm gì?
- Giá trị lõi trước AI là gì?
- Họ thắng nhờ workflow, switching cost, brand, distribution, data hay một giả định hành vi nào?
- Job-to-be-done (công việc người dùng "thuê" sản phẩm làm hộ) là gì?

**Trả lời của tôi:**  
> Trước AI, Stack Overflow thắng nhờ giả định hành vi: Khi gặp bế tắc về kỹ thuật, lập trình viên bắt buộc phải chủ động rời khỏi môi trường code để đi tìm kiếm tài liệu (Mô hình Pull).
Job-to-be-done cốt lõi mà người dùng "thuê" Stack Overflow là giải quyết các lỗi cú pháp/logic phát sinh nhanh nhất có thể. Nền tảng thiết lập vị thế thống trị tuyệt đối nhờ cấu trúc Data Advantage (kho tri thức UGC tích lũy khổng lồ) kết hợp với Distribution dựa trên công cụ tìm kiếm truyền thống (SEO thống trị trang đầu Google). Người dùng chấp nhận workflow thủ công này vì tại thời điểm đó, không có bất kỳ điểm chạm (Entry point) nào tối ưu hơn.

**Bằng chứng đỡ nhận định này:** E1
---

### Nhận định 2 — Kỳ vọng người dùng và luật chơi cạnh tranh đã đổi ở đâu?

#### Nhắc nhanh 7 Dịch chuyển Kỳ vọng

1. Làm xong giúp tôi
2. May đo cho tôi
3. Tự lo việc lặt vặt
4. Trả theo kết quả
5. Phản hồi ngay
6. Giao diện tự thay đổi
7. Thấu hiểu ngữ cảnh

#### Nhắc nhanh 5 Competitive Dynamics

- switching costs giảm
- data advantages tăng
- platform risk
- build-copy cycles tăng tốc
- GTM + distribution quan trọng hơn

**Shift kỳ vọng quan trọng nhất:** Phản hồi ngay + Thấu hiểu ngữ cảnh (User chuyển từ việc chấp nhận đọc các câu trả lời chung chung sang kỳ vọng nhận đoạn code sửa chính xác cho riêng dự án của họ ngay lập tức). 
**Competitive dynamic quan trọng nhất:** Build-copy cycles tăng tốc + Platform risk (Các công cụ AI xây dựng tính năng sinh code với tốc độ chóng mặt, biến chính kho data của Stack Overflow thành năng lượng để bóp nghẹt traffic của họ).

**Trả lời của tôi:**  
> Điểm chạm tra cứu (Entry point) của người dùng đã bị chiếm đóng hoàn toàn. Lập trình viên không còn kiên nhẫn với workflow: Gặp lỗi -> Lên Google -> Lọc link -> Đọc và tự sửa.
Luật chơi cạnh tranh đã đổi từ "Quản trị kho tri thức tĩnh" sang "Tạo sinh giải pháp động trực tiếp trong IDE". Trải nghiệm không phán xét, phản hồi trong mili-giây của ChatGPT và việc nhúng sâu vào nơi làm việc của GitHub Copilot/Cursor đã nâng tiêu chuẩn kỳ vọng của người dùng lên mức: "Hãy sửa lỗi ngay tại chỗ tôi đang gõ", biến việc mở trình duyệt tìm link trở thành một thao tác thừa thãi và lạc hậu.

**Bằng chứng đỡ nhận định này:** E2

---

### Nhận định 3 — Giả định nào không còn đúng nữa? Điều gì đã thay đổi vĩnh viễn?

Gợi ý:

- Switching cost cũ có từng giữ user ở lại không? Vì sao giờ không còn đủ?
- Entry point cũ của sản phẩm có còn tồn tại không, hay người dùng đã chuyển sang một điểm bắt đầu mới?
- Workflow cũ có còn được chấp nhận không, hay chuẩn mới là "làm xong giúp tôi / ngay trong nơi tôi đang làm việc"?
- "Thay đổi vĩnh viễn" không phải là giá cổ phiếu giảm; nó là **chuẩn mới trong đầu người dùng** hoặc **luật chơi mới của thị trường**.
- Phân khúc này còn tồn tại không? Nếu còn, nó đang được phục vụ theo cách khác ra sao?

**Điều đã thay đổi vĩnh viễn theo tôi là:**  
> Thói quen click vào liên kết website để giải quyết các bài toán lập trình sơ cấp đã biến mất vĩnh viễn.
Giả định cũ cho rằng "Cộng đồng khổng lồ và hệ thống tính điểm (Reputation) là rào cản phòng thủ (Moat) không thể phá vỡ" đã không còn đúng. Khi AI bóc tách toàn bộ kho dữ liệu đó thành câu trả lời tức thì, Moat cộng đồng bỗng chốc biến thành "viện bảo tàng lưu trữ". Chuẩn mới trong đầu người dùng hiện tại là Code-generation (Tạo sinh) chứ không còn là Code-searching (Tìm kiếm). Phân khúc tra cứu cộng đồng nay bị đẩy lùi về phía sau, chỉ còn tồn tại dưới dạng một Lưới lọc xác minh (Verification layer) để người dùng tìm đến khi AI gặp hiện tượng ảo tưởng (hallucination) hoặc sinh code lỗi hệ thống.

**Bằng chứng đỡ nhận định này:** E2, E3

---

### Nhận định 4 — Case này còn cứu được không? Nếu có, phải đổi bằng cách nào?

Gợi ý:

- Nếu cứu được: họ phải đổi ở moat nào, workflow nào, distribution nào?
- Nếu không cứu được: vì sao đã quá muộn?
- So với một đối thủ phản ứng tốt hơn, họ chậm ở đâu?

**Verdict ban đầu của tôi:** Có nhưng phải đổi rất mạnh

**Trả lời của tôi:**  
> Stack Overflow không thể cứu vãn được traffic người dùng cuối (B2C) theo cách cũ, nhưng họ hoàn toàn sống sót và bứt phá bằng cách đổi hẳn Moat và mô hình doanh thu sang B2B.
Họ buộc phải từ bỏ tư thế của một "Nền tảng hiển thị quảng cáo ăn theo traffic" để trở thành "Hạ tầng ngầm cung cấp dữ liệu sạch độc quyền" (Data Infrastructure) cho các Big Tech. Bằng cách chặn thu phí API dữ liệu đối với OpenAI, Google và phát triển công cụ nhúng như Stack Overflow MCP Server cho AI Agent, họ chuyển dịch dòng tiền thành công: Thay vì thu tiền từ lượt click của dev, họ thu tiền trên mỗi token dữ liệu mà các mô hình AI buộc phải cắn vào để học công nghệ mới.

**Bằng chứng đỡ nhận định này:** E4

---

## Tóm tắt cá nhân trước khi share trong bàn

Viết đúng 3 câu:

1. `Case này yếu đi vì...`
2. `Điều thay đổi vĩnh viễn là...`
3. `Verdict của tôi là...`

**Bản tóm tắt 3 câu của tôi:**  
1.Case này yếu đi vì: Điểm chạm tra cứu (Entry point) bị các AI Assistant đánh chiếm ngay tại môi trường viết code (IDE), triệt tiêu hoàn toàn workflow rời màn hình để đi tìm link truyền thống.

2. Điều thay đổi vĩnh viễn là: Chuẩn tư duy của người dùng đã dịch chuyển từ "Tìm kiếm code mẫu có sẵn" sang "Tạo sinh đoạn code cá nhân hóa tức thì", biến website Stack Overflow từ một trường học công cộng thành một hạ tầng dữ liệu ngầm.

3. Verdict của tôi là: Stack Overflow sẽ sống sót mạnh mẽ nhưng dưới một hình hài hoàn toàn khác: Không còn là một mạng xã hội của lập trình viên (B2C Ads) mà là một trạm cấp nguyên liệu thô độc quyền không thể thay thế cho các Big Tech AI (B2B Licensing).
---

## Bước 3 — Share trong bàn (7')

### Mỗi người chỉ nói 4 thứ trong 90 giây

1. **Case bạn chọn là gì**
2. **Bằng chứng mạnh nhất bạn có là gì**
3. **Điều gì đã thay đổi vĩnh viễn**
4. **Verdict của bạn**

### Nếu chưa biết hỏi ngược gì, dùng 4 câu này

1. **"Bằng chứng mạnh nhất cho nhận định đó là gì?"**
2. **"Điều gì ở đây là triệu chứng, còn điều gì là thay đổi vĩnh viễn?"**
3. **"Nếu switching cost từng cao, vì sao người dùng vẫn rời đi?"**
4. **"Platform mới hoặc đối thủ mới đã chiếm entry point ở đâu?"**

### Ghi nhanh khi nghe các bạn cùng bàn

| Người | Case | Bằng chứng mạnh nhất họ nêu | Điều họ cho là "thay đổi vĩnh viễn" | Verdict của họ |
|---|---|---|---|---|
| Bạn 1 | | | | |
| Bạn 2 | | | | |
| Bạn 3 | | | | |
| Bạn 4 | | | | |

### Sau khi cả bàn share xong, chốt 3 ý chung

**1. Bàn tôi thấy case nào có bằng chứng mạnh nhất? Vì sao?**  
> _______________________________________________

**2. Có pattern nào lặp lại giữa nhiều case không?**  
Ví dụ: switching costs giảm, platform bước xuống app layer, user chuyển sang "làm xong giúp tôi", moat cũ quá mỏng…  
> _______________________________________________

**3. Một cảnh báo cho chính dự án của nhóm tôi là gì?**  
> _______________________________________________

---

## Bước 4 — Chốt lại verdict cá nhân sau thảo luận (3')

### Sau khi nghe bàn phản biện, verdict của tôi:

- [ ] Giữ nguyên
- [ ] Đổi nhẹ
- [ ] Đổi mạnh

### Vì sao tôi giữ / đổi verdict?

> _______________________________________________  
> _______________________________________________

### Verdict cuối cùng của tôi (phiên bản nộp)

**Case này tổn thương trước AI vì:**  
> _______________________________________________

**Điều thay đổi vĩnh viễn là:**  
> _______________________________________________

**Nếu phải rút 1 bài học cho dự án của nhóm mình, tôi rút ra:**  
> _______________________________________________

---

## Checklist trước khi nộp

- [ ] Tôi đã chọn ít nhất 3 bằng chứng chốt có nguồn.
- [ ] Mỗi nhận định đều chỉ vào ít nhất 1 bằng chứng.
- [ ] Tôi đã ghi lại phần share trong bàn.
- [ ] Tôi đã viết verdict cuối sau thảo luận.

---

## Nếu còn thời gian / làm về nhà

- Bổ sung thêm một case "đối thủ phản ứng tốt hơn" để so.
- Thêm một đoạn ngắn: **nếu tôi là PM của case này trong 6 tháng đầu sau AI shock, tôi sẽ làm gì đầu tiên?**
- Kiểm lại xem case này yếu vì expectation shift, competitive dynamics, hay cả hai cùng lúc.
