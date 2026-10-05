# Prototype Links & Tester Protocol

## 1. Prototype Access Links (Liên kết thử nghiệm)

### Interactive Prototype Suite

| Phương án | Liên kết trong bản tải về | Đường dẫn hash |
| :--- | :--- | :--- |
| Trang chọn phương án | [Mở prototype](prototypes/index.html) | `#/` |
| Option A — Diagnostic Refresher | [Mở Option A](prototypes/index.html#/option-a) | `#/option-a` |
| Option B — Knowledge Checklist | [Mở Option B](prototypes/index.html#/option-b) | `#/option-b` |
| Option C — A/B Contrast & Escalation | [Mở Option C](prototypes/index.html#/option-c) | `#/option-c` |

**Hướng dẫn cho Giảng viên / Trợ giảng:**

1. Mở [repository trên GitHub](https://github.com/minttamdayne/Track1_Day19_2A202602433_DinhThiMinhTam), chọn **Code → Download ZIP**, rồi giải nén.
2. Mở `prototypes/index.html` bằng Chrome hoặc Edge. Giữ nguyên thư mục `static/` và `videos/` bên cạnh file HTML; không cần cài Node.js hay build ứng dụng.
3. Chọn phương án từ trang đầu. Dùng nút **Quay lại** ở góc trên để trở về trang chọn và mở phương án tiếp theo. Có thể mở trực tiếp bằng các đường dẫn hash ở bảng trên.
4. Prototype sử dụng Tailwind CDN và Google Fonts; cần kết nối Internet để tải đầy đủ kiểu giao diện.

**Nếu trình duyệt hạn chế mở file trực tiếp:** Tại thư mục repository, chạy `python3 -m http.server 8000`, rồi mở [trang prototype local](http://localhost:8000/prototypes/index.html). Đây là địa chỉ trên máy người chấm, không phải link công khai.

**Trạng thái link chạy công khai:** GitHub Pages tại `https://minttamdayne.github.io/Track1_Day19_2A202602433_DinhThiMinhTam/prototypes/` trả HTTP 404 khi kiểm tra ngày 05/10/2026. Chưa dùng URL này làm link chấm trực tiếp; cần triển khai bản static và kiểm tra lại trước khi nộp nếu yêu cầu chấm bằng link web công khai.

**Giới hạn bản prototype hiện tại:** Nội dung AI, mở giáo trình và gửi Trợ giảng sử dụng dữ liệu / phản hồi mô phỏng; không chứng minh tích hợp AI hoặc Mentor thật. Option A hiện có câu hỏi đếm ngược 10 giây; Option C hiện đối chiếu Euclid–Cosine. Đây là các sai lệch so với bản thiết kế 2 câu / 60 giây và Token Count–Dimension cần được đối chiếu khi chấm.

- **Stitch Design Project:** `projects/10443824955033242934` (VLearn UI UX Redesign & Workspace Studio); mã project không thay thế link chia sẻ công khai.

---

## 2. Kịch bản thử nghiệm chuẩn dành cho Tester ngoài nhóm (Gate 4)

### Bối cảnh giao cho Tester (Unbiased Framing)
> *"Chào bạn! Bạn đang vào vai một học viên non-tech / chuyển ngành tham gia khóa học AI trên nền tảng VLearn. Bạn đang thực hành Bài 4: Xây dựng RAG Agent cơ bản với LangChain. Tại bước VectorStore Indexing, bạn gặp lỗi hoặc cảm thấy bối rối trước hai thuật ngữ then chốt: **'Embedding Dimension'** (tại sao văn bản dài ngắn khác nhau đều thành 1536 chiều?) và **'Cosine Similarity'** (thuật toán này đo độ tương đồng ngữ nghĩa ra sao?). Bạn muốn nhanh chóng hiểu bản chất kiến thức nền để tiếp tục hoàn thành bài tập trong ít hơn 3 phút."*

### Nhiệm vụ của Tester (Task Instructions)
1. Quan sát màn hình bài tập LangChain và thông báo rào cản khái niệm bên trái.
2. Bấm nút kích hoạt hỗ trợ trên thanh công cụ.
3. Lần lượt trải nghiệm 3 phương án hỗ trợ (dùng trang chọn phương án hoặc các link A/B/C ở trên):
   - **Option A: Diagnostic Refresher (AI-Led):** Bấm “Tôi vẫn chưa hiểu”, trả lời câu hỏi kiểm tra nhanh và quan sát phản hồi / chuyển tiếp sang AI Tutor trong bản hiện tại.
   - **Option B: Knowledge Checklist (User-Led):** Khám phá drawer cây phân rã kiến thức nền, tự tick chọn mắt xích mình thấy mơ hồ (vd: *Cosine Similarity tính thế nào?*) và đọc micro-lesson trực quan bung ra.
   - **Option C: A/B Contrast & Escalation (Co-create & Human):** Trải nghiệm đối chiếu 2 kịch bản hiểu tương phản (Cách hiểu A vs Cách hiểu B), đọc giải thích ngộ nhận và thử nghiệm nút gửi ticket hỗ trợ 1-1 cho Trợ giảng.
4. Thử tính năng kiểm soát và phục hồi (**"✕ Đóng / Quay lại bài"**) ở mỗi phương án.
5. Vừa dùng vừa nói to suy nghĩ (Think-Aloud Protocol) mà không cần người hướng dẫn phải can thiệp hay gợi ý.
