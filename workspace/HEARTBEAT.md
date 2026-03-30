# HEARTBEAT.md

## Periodic Tasks

### 📋 Weekly Conversation Stats (Monday)
- If today is Monday: read `memory/conversations/YYYY-MM.md` for the current month
- Summarize in daily memory `memory/YYYY-MM-DD.md`:
  - Total conversations last week
  - Top 3 most common issues
  - Count of ⚠️ new questions not in skill
  - Count of ❌/⏳ unresolved cases
- If there are many ⚠️ new questions → notify admin Anh Phi to update `interlink-support` skill

### 📄 Whitepaper Sync Health Check (Daily)
- Check `memory/whitepaper-data.md` → verify "Last synced" date is today or yesterday
- If last sync is older than 2 days → cron job may have failed → log warning in daily memory
- If whitepaper content has major changes → notify admin

