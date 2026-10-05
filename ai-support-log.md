# AI Support Log — Nhật Ký Hỗ Trợ Của AI & Phản Biện Con Người

- **Học viên:** Đinh Thị Minh Tâm (MHV: 2A202602433)
- **Dự án:** VLearn — AI Tutor: Diagnostic Refresher, Three Prototypes, One Next Change
- **Hồ sơ:** Track1_Day19_2A202602433_DinhThiMinhTam
- **Công cụ AI trong phiên chỉnh sửa tài liệu:** Codex
- **Phạm vi ghi nhận:** Rà soát và chỉnh sửa tài liệu cá nhân, README và phiếu phản hồi cho phiên Minh Tâm phỏng vấn Nguyễn Thu Thảo. Nhật ký này ghi nhận công việc trong cuộc trao đổi hiện tại; không quy toàn bộ công việc kỹ thuật của nhóm thành đóng góp cá nhân của Minh Tâm.

---

## 1. AI Đã Giúp Được Những Gì? (AI Contributions)

- Đọc và đối chiếu tài liệu Markdown của dự án để xác định bối cảnh LangChain RAG Indexing, cơ chế của Option A/B/C và phản hồi được ghi trong tài liệu tổng hợp nhóm.
- Chỉnh [prototype-feedback-note.md](prototype-feedback-note.md) theo thông tin Minh Tâm xác nhận: tester là Nguyễn Thu Thảo, 22 tuổi, sinh viên năm cuối ngành Hệ thống thông tin.
- Soạn lại phần Observation trong [README.md](README.md), thống nhất xếp hạng của Thu Thảo là **Option C > Option B > Option A** theo tài liệu tổng hợp nhóm.
- Chuyển phiếu phản hồi sang mẫu **hai cột, bảy tiêu điểm** do Minh Tâm cung cấp: First Action, Hesitation, Evidence Checking, Control & Recovery, Selected Option, Trade-offs và Counter-evidence.
- Phân biệt phản hồi đã có với dữ liệu còn thiếu, tránh biến mô tả tính năng prototype thành hành vi thực tế của tester.

## 2. AI Đã Sai Hoặc Còn Hạn Chế Ở Đâu? (AI Flaws & Limitations)

- **Tài liệu kế thừa chưa đúng chủ thể:** Bản AI Support Log trước ghi tên Phạm Thành Đạt, mã học viên 2A202602721 và các công việc như xây dựng testbed, cài skills, cấu hình hook. Các nội dung này chưa có căn cứ để ghi là đóng góp của Minh Tâm.
- **Thông tin tester thay đổi giữa các bản:** Bản phiếu trước mô tả phiên Minh Trí và chứa trích dẫn, thao tác chi tiết của phiên đó. Khi chuyển sang Thu Thảo, các chi tiết này không thể được giữ rồi gán cho người mới.
- **Thiếu bằng chứng hành vi riêng:** Tài liệu tổng hợp nhóm có xếp hạng và nhận xét của Thu Thảo, nhưng chưa có ghi chép riêng về nút bấm đầu tiên, thời gian do dự, việc đọc nguồn hoặc thao tác gửi/hủy ticket. AI có thể hỗ trợ diễn giải tài liệu, chưa thể xác nhận những hành vi này.
- **Nguy cơ suy rộng quá mức:** Thích Option C không đồng nghĩa với hiểu bài nhanh hơn, tự hoàn thành bài tập hoặc giảm bỏ học. Cảm giác an tâm vì có Trợ giảng cũng chưa chứng minh ticket được gửi hay Trợ giảng phản hồi đúng thời gian.

## 3. Minh Tâm Đã Định Hướng & Kiểm Soát Việc Chỉnh Sửa Như Thế Nào? (Human-in-the-Loop)

- Yêu cầu AI đọc lại tài liệu và sửa biên bản theo đúng sinh viên điều phối là **Đinh Thị Minh Tâm**.
- Xác nhận tester chính xác là **Nguyễn Thu Thảo**, 22 tuổi, sinh viên năm cuối ngành Hệ thống thông tin, thay cho Minh Trí ở bản trước.
- Yêu cầu soạn lại mục Observation của README cho phiên Thu Thảo để thống nhất với hồ sơ cá nhân.
- Cung cấp mẫu phiếu phản hồi bắt buộc gồm bảy tiêu điểm, đặt trọng tâm vào ghi chép hành vi thực tế (**Fact-First**).
- Yêu cầu sửa AI Support Log thành nhật ký cá nhân của Minh Tâm. Những dữ liệu thực địa còn thiếu cần được Minh Tâm bổ sung từ ghi chép phiên, không để AI tự tạo lời nói hay hành vi của tester.

## 4. Kết Quả Kiểm Tra & Những Điểm Còn Chưa Chứng Minh

- **Đã kiểm tra:** Phiếu phản hồi có đúng hai cột và đủ bảy tiêu điểm; tên tester và xếp hạng thống nhất với bản README đã chỉnh. Kiểm tra `git diff --check` riêng cho phiếu phản hồi đạt.
- **Cần bổ sung:** Thời gian và hình thức phiên, First Action, thao tác kiểm tra minh chứng, cách phục hồi thực tế, sự đánh đổi Thu Thảo chấp nhận và phát biểu nguyên văn nếu có.
- **Still Unproven:** Khả năng hoàn thành luồng độc lập (Gate 4), thời gian hiểu bài dưới ba phút, khả năng vận dụng sau khi quay lại bài tập, độ bền ghi nhớ và hiệu quả hỗ trợ từ Trợ giảng thật.
- **Giới hạn của đợt chỉnh sửa:** Công việc được ghi ở đây là chỉnh tài liệu; chưa thực hiện kiểm thử giao diện hoặc xác minh các tích hợp AI/Mentor đang chạy.

**Tài liệu đối chiếu:** [README.md](README.md), [prototype-feedback-note.md](prototype-feedback-note.md), [group-feedback-synthesis.md](group-feedback-synthesis.md) và [three-option-design-sheet.md](three-option-design-sheet.md).
