# 2026-03-26 — Interlink Support Training (Detailed)

Loaded from 3 CSV files. This is the full case-by-case reference.

## Source Files
1. `Interlink_technicalsupport - Các câu trả lời thường dùng.csv` — Quick FAQ (~30 cases)
2. `Interlink_technicalsupport - Cách xử lý và reply user.csv` — Bug codes M01-O03 (~14 cases)
3. `Interlink_technicalsupport - Cách xử lý và reply user 2.csv` — Advanced: Burn, Email, HCS, Wallet (~11 cases)

## Key Policy Baselines
- Account deletion: NOT supported
- ID change: NOT supported
- Email change: NOT supported (use face/Telegram/Facebook/Apple login instead)
- HCS formula: NEVER disclose publicly
- Wallet recovery: IMPOSSIBLE without seedphrase/private key
- Reward schedule: Weekly = Sunday 3AM UTC+0, Monthly = 1st of month 3AM UTC+0

## Burn Mechanics
- Active burn mechanism: inactive referrals cause ITLG deduction
- F1 referral burned to 0 → -1000 ITLG from you
- F2 referral burned to 0 → -500 ITLG from you
- Second burn by same referral → no additional deduction
- Recovery: complete full mining streak (self) or wait for downline to complete theirs

## Bug Handling Protocol
- Always ask for: Interlink ID + screenshot/video + timestamps
- For unclear bugs: request screen recording
- PIC assignments: Mining → Quang, Rewards → Minh, Login → Quang/Anh Đạt, Wallet → Quang
- Escalation: if issue persists after basic troubleshooting (exit app, wait 10-15 min), push to Dev

## HCS Rules (Internal - DO NOT share formula)
- Tell users: be active in app (Mining, Group Mining, Games) and wallet (Trade, Swap)
- AI calculates based on individual activity, fair for new and old users
- Multiple wallets linked to one ID → all count for HCS
- Wallet must be active (Trade/Swap) to count

## Skill File Created
- `workspace/skills/interlink-support/SKILL.md` — full customer support knowledge base
- Covers all cases from all 3 CSVs
- RBAC: regular users can read this skill via `read` tool only
