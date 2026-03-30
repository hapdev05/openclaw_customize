# MEMORY.md

## Interlink customer support memory
- On 2026-03-26, Anh Phi asked that I learn 3 Interlink support CSV files in full detail, not just summarize them.
- I should remember them case-by-case: each file, each scenario, what info to request from the user, who the PIC is when listed, and the exact or near-exact support reply logic.
- **Skill created**: `skills/interlink-support/SKILL.md` — full customer support knowledge base with Q&A, bug codes (M01-G04), advanced cases (Burn/HCS/Wallet), and response rules.
- **Detailed case notes**: `memory/2026-03-26-interlink-detailed.md` — case-by-case reference from all 3 CSVs.
- When handling Interlink support, I should read the `interlink-support` skill first, then map user issues to the closest known case before improvising.
- Important support baselines from the training:
  - Ask for Interlink ID + screenshot/video + time + failing step for most bug reports.
  - Often ask for a screen recording when the issue occurs.
  - Do not disclose the HCS formula publicly.
  - Wallet recovery is impossible without prior seed phrase/private key backup.
  - Prefer the more cautious/newer answer if source replies conflict (example: changing email is currently not supported).
  - Product policy baseline: account deletion not supported; Interlink ID change not supported.
  - Reward schedule baseline: weekly game reward Sunday 3AM UTC+0; monthly reward first day of month 3AM UTC+0.

## Conversation logging
- **Skill created**: `skills/conversation-logger/SKILL.md` — tự động ghi log mỗi cuộc hội thoại hỗ trợ.
- Log lưu tại `memory/conversations/YYYY-MM.md` (theo tháng).
- Ghi: vấn đề, phân loại, mã lỗi, ngôn ngữ, trạng thái giải quyết, tóm tắt trao đổi.
- Đánh dấu `⚠️ CÂU HỎI MỚI` khi user hỏi điều chưa có trong skill → admin review.
- KHÔNG ghi thông tin nhạy cảm (ID, mật khẩu, seedphrase).
- Tổng hợp thống kê hàng tuần qua heartbeat (thứ Hai).

## Ambassador program update (2026-03-28)
- Câu trả lời ambassador đã được cập nhật: có link onboarding, trainee process, và contact @ekwinbudi.
- Không còn trả lời "chúng tôi không thuộc chương trình đại sứ" — thay bằng hướng dẫn chi tiết.

## Whitepaper sync (2026-03-28)
- **Skill created**: `skills/whitepaper-sync/SKILL.md` — hướng dẫn sync nội dung whitepaper hàng ngày.
- **Data file**: `memory/whitepaper-data.md` — dữ liệu whitepaper đã tổng hợp (ITL, ITLG, tokenomics, FAQ...).
- **Cron job**: `whitepaper-daily-sync` chạy lúc 3:00 AM UTC+7 (20:00 UTC) hàng ngày.
- Khi user hỏi về token/tokenomics → đọc `memory/whitepaper-data.md` + dẫn link whitepaper.
