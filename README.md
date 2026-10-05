# Track 1 — Day 18 Lab: Three Prototypes, One Next Change
**Chương trình:** VinUni AIA — AI Product & Technical Management
**Học viên:** Đinh Thị Minh Tâm
**Mã học viên (MHV):** `2A202602433`
**Repository:** `Track1_Day19_2A202602433_DinhThiMinhTam`

---

## 1. Thông tin Cá nhân và Nhóm
- **Họ và tên:** Đinh Thị Minh Tâm
- **Mã học viên:** `2A202602433`
- **Tên nhóm:** Nhóm 2A — Case A: Diagnostic Refresher
- **Thành viên nhóm:**
  1. **Phạm Thành Đạt** — Phụ trách kiến trúc kỹ thuật testbed, thiết kế Option B (Knowledge Checklist User-Led), điều phối phiên thử nghiệm cá nhân #1.
  2. **Bùi Thị Ngọc Trân** — Phụ trách thiết kế Option A (Diagnostic Refresher AI-Led), điều phối phiên thử nghiệm cá nhân #3.
  3. **Đinh Thị Minh Tâm** — Phụ trách thiết kế Option C (A/B Contrast & Escalation Co-create & Human), điều phối phiên thử nghiệm cá nhân #2.
- **Case được chọn:** **Case A — AI Tutor: Diagnostic Refresher**
  - *Trigger:* Học viên bấm nút “Tôi vẫn chưa hiểu”
  - *Input:* Bài hiện tại, câu trả lời/mã nguồn gần đây và lịch sử học tập
  - *AI Action:* Chẩn đoán và lựa chọn khái niệm nền tương ứng
  - *Output:* Một phần ôn lại ngắn (< 3 phút) trước khi đưa học viên quay lại bài hiện tại
  - *User Control:* Học viên chủ động yêu cầu trợ giúp và nắm quyền kiểm soát tiến trình

---

## 2. Hypothesis Problem (Giả thuyết Vấn đề Day 18)

### Bản Giả thuyết Vấn đề của Nhóm:
> **"Học viên non-tech và chuyển ngành thường xuyên bị nghẽn và bỏ dở bài học khi tiếp cận các bài tập kỹ thuật AI tổng hợp (như LangChain RAG Indexing), do họ thiếu khả năng tự chẩn đoán chính xác lỗ hổng kiến thức nền (prerequisites) đang gặp phải và thiếu giải pháp ôn tập bổ trợ ngắn gọn, tức thì (< 3 phút) ngay tại giao diện học tập."**

### Nối kết với Bằng chứng Thực nghiệm Day 17 (Gate 1 — Evidence Continuity):
- **Phỏng vấn Anh Khánh (25 tuổi - BA):** Vừa làm vừa học dự án mới, giai đoạn đầu bị ngợp bởi lượng kiến thức kỹ thuật quá lớn; workaround là tự dùng AI tham khảo nhưng tài liệu bị rối và tốn thời gian xác nhận thủ công.
- **Phỏng vấn Bạn Khuê (21 tuổi - Sinh viên CS):** Gặp khó ở các môn lý thuyết nền tảng phức tạp (Cryptography/Cloud); phải tìm tài liệu rời rạc bên ngoài làm gián đoạn luồng làm bài thực hành.
- **Phỏng vấn Bạn Thương (23 tuổi - BA) & Bạn Linh (22 tuổi - Marketing):** Cả hai đều đối mặt với rào cản thuật toán và code. Workaround điển hình của bạn Linh là **chủ động nhờ AI Agent tạo checklist kiến thức để chẻ nhỏ vấn đề**. Khi AI đưa ra kết quả thiếu nhất quán ngữ cảnh (như Thương phản ánh), người học mất rất nhiều công sức điều chỉnh thủ công.

### Điều Nhóm Chưa Biết (The Unknown):
- Chưa biết cơ chế nào giữa **AI tự chẩn đoán (AI-Led)**, **Người học tự soi chiếu checklist (User-Led)**, hay **Đối chiếu phản biện tư duy kết hợp Trợ giảng (Human-in-the-loop)** sẽ giúp người học non-tech thông suốt nhanh nhất mà không gây quá tải nhận thức.
- Chưa biết việc ôn tập vi mô tức thì (< 3 phút) có thực sự chuyển hóa thành năng lực giải quyết bài tập độc lập lâu dài hay chỉ là giải pháp tình thế.

---

## 3. Three Solution Options & Prototype Links (Gate 2 & Gate 3)

### Constants (Giữ cố định cho cả 3 Options):
- **Target User:** Học viên non-tech / chuyển ngành (Marketing, BA mới vào nghề).
- **Situation:** Đang trong luồng học bài tập kỹ thuật tổng hợp thì bị nghẽn ở một khái niệm nền tảng.
- **Task:** Xác định và lấp nhanh lỗ hổng kiến thức nền để tiếp tục hoàn thành bài học.
- **Desired Outcome:** Hiểu bản chất khái niệm bị hổng trong < 3 phút, khôi phục sự tự tin và tiếp tục làm bài mà không rời khỏi giao diện.
- **Content/Data Fixture:** **Bài 4: Xây dựng RAG Agent cơ bản với LangChain** — Tại bước cấu hình VectorStore Indexing, học viên gặp lỗi/không hiểu thuật ngữ: *"Embedding Dimension & Cosine Similarity"*.

**Cách mở để chấm:** Tải repository về và mở [trang chọn prototype](prototypes/index.html), sau đó chọn A/B/C. Xem [liên kết và hướng dẫn thử nghiệm](prototype-link.md) để mở từng phương án. GitHub chỉ hiển thị mã nguồn HTML; link chạy công khai chưa được xác minh hoạt động.

### Variables Across Options (Khác biệt về Cơ chế & Phân chia vai trò):

| Phương án | Cơ chế cốt lõi (Mechanism) | Phân chia vai trò User — AI | Human Control & Đường Phục Hồi (Recovery) | Prototype Link |
| :--- | :--- | :--- | :--- | :--- |
| **Option A: Diagnostic Refresher (AI-Led)** | **Chẩn đoán trắc nghiệm tự động:** AI đưa ra 2 câu mini-quiz để xác định điểm hổng, sau đó push Refresher Card 60s về khái niệm nền tương ứng. | - **AI:** Hỏi qua quiz, chấm điểm, suy luận concept bị hổng, sinh thẻ tóm tắt (*Ask*).<br>- **User:** Trả lời 2 câu quiz, đọc Refresher Card, bấm quay lại bài. | - **Kỳ vọng:** Báo rõ quiz 60s.<br>- **Bằng chứng:** "Dựa trên bài học VectorStore & câu trả lời quiz".<br>- **Phục hồi:** Nút *"Bỏ qua chẩn đoán"* & *"Đây không phải phần tôi cần"*. | [Mở Option A](prototypes/index.html#/option-a) |
| **Option B: Knowledge Checklist (User-Led)** | **Cây phân rã kiến thức tự chọn:** Giao diện hiển thị drawer checklist các mắt xích nền tảng; user tự click vào mắt xích mơ hồ để xem giải thích trực quan. | - **AI:** Phân rã cấu trúc prerequisite; thụ động chờ user click (*Don't Act*).<br>- **User:** Tự duyệt checklist, tự tick chọn điểm chưa rõ (*Self-Assessment*). | - **Kỳ vọng:** Nhãn tab ghi rõ danh mục kiến thức có sẵn.<br>- **Bằng chứng:** Dẫn link nguồn Bài 2 trong giáo trình.<br>- **Phục hồi:** Nút đóng drawer [X], bỏ tick chọn, nút mở bài giảng gốc. | [Mở Option B](prototypes/index.html#/option-b) |
| **Option C: A/B Contrast & Escalation (Co-create & Human)** | **Đối chiếu phản biện tư duy & Kết nối Mentor:** AI đưa ra 2 kịch bản hiểu tương phản (A vs B); giải thích ngộ nhận; nếu vẫn tắc thì tự tạo ticket gửi Trợ giảng. | - **AI:** Sinh 2 kịch bản tương phản; giải thích ngộ nhận; tự gom context gửi Mentor khi user yêu cầu (*Ask*).<br>- **User:** Chọn phương án A/B; quyết định có cần escalate cho Mentor không. | - **Kỳ vọng:** Ghi rõ cơ chế đối chiếu & thời gian phản hồi Trợ giảng.<br>- **Bằng chứng:** "68% học viên nhầm Dimension & Token Count".<br>- **Phục hồi:** Preview ticket trước khi gửi, nút hủy gửi, thoát an toàn 100%. | [Mở Option C](prototypes/index.html#/option-c) |

---

## 4. Đóng Góp Của Tôi Trong Nhóm (Individual Contribution)

1. **Thiết kế & Hoàn thiện Phương án C (A/B Contrast & Escalation — Co-create & Human):**
   - Đóng góp phương án đối chiếu hai cách hiểu để nhận diện ngộ nhận, kết hợp đường hỗ trợ từ Trợ giảng khi người học vẫn bị nghẽn; lấy cảm hứng từ nhu cầu hỗ trợ và kiểm tra ngữ cảnh trong phỏng vấn Thương ở Day 17.
   - Phân vai: người học chọn cách hiểu và quyết định có cần hỗ trợ; hệ thống trình bày đối chiếu và chuẩn bị nội dung yêu cầu hỗ trợ để người học xem trước, xác nhận hoặc hủy.
2. **Thực hiện Phiên Thử Nghiệm Cá Nhân (Facilitation & Observation):**
   - Điều phối phiên với Nguyễn Thu Thảo (22 tuổi, sinh viên năm cuối ngành Hệ thống thông tin) và lập [phiếu phản hồi cá nhân](prototype-feedback-note.md) theo mẫu Fact-First.
3. **Biên soạn Tài liệu & Tổng hợp Phản hồi:**
   - Hoàn thiện nội dung Chặng 4 và Chặng 5, đối chiếu [tổng hợp phản hồi nhóm](group-feedback-synthesis.md), đề xuất một Next Change kết hợp checklist tự chọn với đối chiếu ngộ nhận và nêu các điểm Still Unproven.

**Phần kế thừa của nhóm:** Kiến trúc testbed và thiết kế Option B do Phạm Thành Đạt phụ trách; Option A do Bùi Thị Ngọc Trân phụ trách. Các phần này tạo nền tảng chung cho phiên thử nghiệm của tôi.

---

## 5. Prototype Feedback & Group Synthesis (Gate 4 & Gate 5)

### Observation từ Phiên Tôi Điều Phối (Tester: Nguyễn Thu Thảo — 22 tuổi):

- **Người điều phối:** Đinh Thị Minh Tâm (MHV: 2A202602433).
- **Tester ngoài nhóm:** Nguyễn Thu Thảo, sinh viên năm cuối ngành Hệ thống thông tin.
- **Phản ứng với Option A:** Quiz trong lúc đang bị nghẽn bài thực hành tạo cảm giác bị kiểm tra bài cũ và tăng áp lực tâm lý.
- **Phản ứng với Option B:** Xếp thứ hai sau Option C; chưa có ghi chép riêng về lý do đánh giá và các mắt xích Thảo đã chọn.
- **Phản ứng với Option C:** Yêu thích nhất vì ví dụ đối chiếu A/B làm rõ điểm nhầm lẫn giữa Token Count và Embedding Dimension; nút kết nối Trợ giảng tạo cảm giác an tâm khi gặp khó khăn.
- **Xếp hạng mức độ ưa thích:** Option C > Option B > Option A.
- **Bài học từ phản hồi:** Thử kết hợp checklist tự chọn với thẻ đối chiếu ngộ nhận và giữ đường kết nối Trợ giảng dự phòng.
- **Giới hạn ghi nhận:** Phản hồi trên được đối chiếu từ tài liệu tổng hợp nhóm; cần bổ sung ghi chép thao tác và kết quả tiếp tục bài tập để đánh giá khả năng hoàn thành độc lập, thời gian hiểu bài và mức độ vận dụng.
- Chi tiết xem tại: [prototype-feedback-note.md](prototype-feedback-note.md).

### Tổng hợp Từ Ba Phiên Thử Nghiệm (Group Synthesis):
- **Cross-Tester Patterns:** Cả 3 tester đều yêu cầu can thiệp phải dưới 3 phút; bằng chứng minh bạch (số liệu 68% nhầm lẫn, trích xuất Bài 2) gia tăng độ tin cậy; các nút thoát hiểm là bắt buộc.
- **Divergences:** Kỹ sư công nghệ ưu tiên Option B (tự chủ, nhanh); trong khi học viên chuyển ngành/non-tech đánh giá cao Option C (đối chiếu tư duy, có Trợ giảng bảo chứng).
- Chi tiết xem tại: [group-feedback-synthesis.md](group-feedback-synthesis.md).

### One Group Next Change (Thay đổi then chốt tiếp theo dựa trên bằng chứng):
> **Tích hợp Cơ chế Lai (Hybrid Flow): Khởi đầu bằng Cây Mắt Xích Kiến Thức (Option B - User-Led), nhưng khi người học bấm vào một mắt xích, giao diện cung cấp tùy chọn "Xem đối chiếu cách hiểu A vs B" (từ Option C) kèm nút gửi Trợ giảng dự phòng nếu vẫn chưa thông.**

### Still Unproven (Những điểm vẫn chưa được kiểm chứng):
1. Chưa kiểm chứng được khả năng duy trì trí nhớ dài hạn (retention) của học viên sau các thẻ micro-lesson 60s.
2. Chưa kiểm chứng được chi phí vận hành và thời gian phản hồi thực tế của Trợ giảng khi số lượng ticket tăng đột biến trong giờ cao điểm.

---

## 6. AI Support Log (Tóm tắt Phản ánh Cá nhân)

- **AI đã giúp gì:** Codex hỗ trợ tôi đọc và đối chiếu tài liệu Markdown, chỉnh phiếu phản hồi cho phiên tôi điều phối với Nguyễn Thu Thảo, cập nhật mục Observation trong README và trình bày phiếu theo mẫu hai cột, bảy tiêu điểm Fact-First. Phản hồi được thống nhất theo tài liệu nhóm: Option C > Option B > Option A.
- **AI sai và còn hạn chế ở đâu:**  Mức độ ưa thích Option C chưa chứng minh khả năng hiểu bài nhanh hơn hay hoàn thành bài tập độc lập.
- **Tôi đã định hướng và kiểm soát gì:** Tôi xác nhận người điều phối là Đinh Thị Minh Tâm (MHV: 2A202602433), tester là Nguyễn Thu Thảo (22 tuổi, sinh viên năm cuối ngành Hệ thống thông tin); yêu cầu chỉnh README và cung cấp mẫu phiếu phản hồi Fact-First. Các dữ liệu còn thiếu được đánh dấu để tôi bổ sung từ ghi chép phiên, không dùng lời nói hoặc thao tác của tester khác.
- Chi tiết xem tại: [ai-support-log.md](ai-support-log.md).
- **Những điểm còn cần kiểm chứng:** Hành động đầu tiên, cách kiểm tra minh chứng, thao tác phục hồi, sự đánh đổi Thu Thảo chấp nhận và kết quả tiếp tục bài tập. Đợt hỗ trợ này tập trung vào chỉnh tài liệu, chưa xác minh luồng giao diện, tích hợp AI/Mentor hoặc khả năng hoàn thành độc lập theo Gate 4.

---

## 7. Cấu Trúc Hồ Sơ Nộp Bài
```
Track1_Day19_2A202602433_DinhThiMinhTam/
├── README.md                          # Thuyết minh tổng thể 6 phần theo chuẩn Day 18
├── three-option-design-sheet.md       # Phân tích Chặng 2 (Three Options) & Chặng 3 (Human-AI Design Pass)
├── prototype-link.md                  # Liên kết prototype & kịch bản thử nghiệm chuẩn
├── prototype-feedback-note.md         # Ghi chép phiên thử nghiệm cá nhân facilitate
├── group-feedback-synthesis.md        # Tổng hợp 3 phiên thử nghiệm, Next Change & Still Unproven
├── ai-support-log.md                  # Nhật ký hỗ trợ AI của Minh Tâm
├── DESIGN.md                          # Hệ thống thiết kế VLearn, bảng màu, typography và nguyên tắc UX
├── AGENTS.md                          # Chỉ dẫn workflow Stitch MCP và quy tắc 5 Evaluation Gates
├── index.html                         # Bộ testbed prototype tương tác chạy trực tiếp trên trình duyệt
├── prototypes/
│   └── index.html                     # Bản testbed chuyên biệt của nhóm
└── .agents/
    ├── hooks.json                     # Cấu hình AI Log Hook
    ├── scripts/
    │   ├── ai_log_hook.sh
    │   └── ai_log_hook.py             # Script tự động ghi log AI
    └── skills/                        # Các kỹ năng đã cài đặt (Matt Pocock, UI/UX, BA)
```
