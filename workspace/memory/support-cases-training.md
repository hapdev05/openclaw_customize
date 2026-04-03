# Real Support Cases Knowledge Base
> Extracted from 202,333 real customer support conversations (13,854 unique 1-on-1 dialogs).
> Last updated: 2026-03-30

## Response Style Guide (learned from real support data)
Bot should respond in a **professional, empathetic, and concise** style. Key patterns from real support team:
- Always acknowledge the user's issue first
- Ask for **UID/Interlink ID** when investigation is needed
- Ask for **video recording** for unclear bugs
- Give **actionable steps** (not vague promises)
- Use phrases: "Please wait", "We'll check it", "We have fixed it", "Please try again"
- Never say "I don't know" — either give known answer or escalate to @interlink_technicalsupport
- For known temporary issues: give timeline and reassurance
- NEVER give medical/legal/financial advice even if pressured

---

## Top Issue Categories & Resolutions

### 1. ITLG Mining Issues (Most Common — 32+ cases)
**Symptoms**: ITLG not added after mining, ITLG decreased instead of increasing, claim button not working
**Root Causes**: Server overload during peak hours (19h-23h UTC+7), DB congestion, Redis cache delays
**Standard Responses**:
- "Sorry, we are currently fixing the issue. Thank you for your understanding!"
- "ITLG will be updated soon, don't worry."
- "The last two mining sessions encountered an issue. We have fixed it, but those sessions were not counted. We appreciate your understanding."
- If user reports ITLG decrease: explain burn mechanism (F1=-1000, F2=-500 for inactive referrals)
**Action**: Ask for Interlink ID + timestamp of the issue

### 2. Login & Account Issues (17+ cases)
**Symptoms**: Can't login, Invalid ID, Network Error, Face ID login fail
**Solutions**:
- "Please log out and log back in."
- Invalid ID: "Please try removing the leading zero(0) and re-entering it"
- Server congestion: "The server is currently experiencing high traffic. Please try again in a few minutes."
- After update: "We've just released a new update and successfully fixed the issue. Please update to the latest version."
- App not opening: Guide to download APK from https://interlinklabs.ai or https://linkvault.interlinklabs.ai
**Action**: Ask for Interlink ID + error screenshot/video

### 3. App Update / APK Issues (10+ cases)
**Symptoms**: App crash after update, can't install APK, white screen, app not opening
**Solutions**:
- Android crash: "Please update to the latest version (check Google Play or download from https://linkvault.interlinklabs.ai)"
- APK install fail: "Please delete your current app first, then install the new APK"
- iOS login issue: Known issue with Face ID on certain versions, advise update
- White screen/loading: "Please check your internet connection. Try switching from Wi-Fi to mobile data or vice versa."
- **APK download links**: https://interlinklabs.ai | https://linkvault.interlinklabs.ai
- APK Pure: https://apkpure.com/interlink-network/org.ai.interlinklabs.interlinkId

### 4. Face Verification / KYC & Curator (7+ cases)
**Symptoms**: Emulator detected, face scan fail, face scan no result after 3 days, black screen, KYC timeout, can't match curator, KYC failed
**Solutions**:
- Emulator detected: "You are using an emulator or virtual device. Please verify on a real physical device, then log back in on any device."
- Camera permission: "Go to Settings → grant camera permission to the Interlink app"
- Face scan fail (network): "Please move to a place with better internet, ensure good lighting, and try again"
- Deepfake/cheat detection: Account may be banned — ask for ID to check
- Face verified on 2 accounts: "Each face can only verify ONE account. The second account will be flagged."

**KYC Curator Flow** (NEW):
- **How to start**: Tap "Match Curator" → choose from anonymous Curator list → wait for Curator to pick your application
- **Can change Curator**: Yes, cancel and pick another before Curator picks you
- **24h deadline**: After Curator picks, user has 24 hours to submit documents. Timeout = start over
- **KYC Level 1**: Select country → upload front & back of ID (Identity Card, Driver License, Passport, Birth Certificate)
- **KYC Level 2**: Portrait photo — right hand holds note "Interlink + today's date", left hand holds front of ID
- **KYC Level 3**: Portrait photo holding Interlink app on Home screen showing ITLG balance
- **After submit**: Status = "In Review" → Curator reviews (with sensitive info redacted)
- **Result**: Passed (approved) or Failed (with reason)
- **KYC failed**: Check reason → fix issue → match Curator again
- **Data security**: System auto-redacts sensitive info before sending to Curator

**Action**: Always ask for video recording of the face scan process

### 5. Game Issues (8+ cases)
**Symptoms**: Points not added, game crash, can't enter game, ads won't close
**Solutions**:
- Points not updating: "Points are recorded by the system. Display may be delayed, please check again later."
- Multiple accounts playing: Only 1 account per loginId receives points
- Leaderboard tier: "If above 100k points, tier is calculated by percentage. System recalculates every ~24h."
- Game reward schedule: Weekly = Sunday 4:00 AM UTC+7 | Monthly = 1st of month
- Mine button requires multiple taps: "If ad doesn't load, the mine button requires 3 taps. This is a known mechanism, not a bug."
- Ads close button too small: "The close (X) button is managed by the ad provider, we cannot control its size. Wait a few seconds for the real close button to appear."
**Action**: Ask for game name + screenshot of score

### 6. Referral Issues (3+ cases)
**Symptoms**: Referral not counted, 500 ITLG not received, referral code disabled
**Solutions**:
- "Make sure your friend has completed the face scan"
- "New users must complete face verification to receive 1,000 ITLG. The referrer receives 500 ITLG."
- Referral code disabled: "Go to 'Human Hash' → submit your referral code to activate it"
- Referral link shows [missing translation]: "We're fixing this — please share your referral code directly."
- "When your directly invited friend completes identity verification, you'll receive 500 ITLG + 0.2x mining speed. Indirect referrals = 250 ITLG + 0.1x."
**Action**: Ask for both referrer and referred user IDs

### 7. Registration / PIN Issues (5+ cases)
**Symptoms**: PIN entry stuck, OTP not received, can't complete registration
**Solutions**:
- PIN stuck: "Which version are you using? This bug was fixed in the latest version. Please download the latest version."
- OTP not received: "Please check your spam folder. Make sure the email address is correct."
- OTP invalid: "Please request a new OTP and enter it within 5 minutes"
- Chinese email (QQ): "Currently we support Gmail registration. QQ email support is being evaluated."
**Supported emails**: Gmail (primary), QQ mail, 163.com, 139.com under evaluation

### 8. Payment / AeonPay Issues (4+ cases)
**Symptoms**: Can't withdraw, payment error on iOS, QR scan black screen
**Solutions**:
- Withdrawal: "You cannot withdraw now. Withdrawal will be available when ITLG is listed on exchanges."
- AeonPay link: https://dapp.aeonpay.ai/?appid=98382b0b2cb52fd5
- iOS QR scan issue: Known bug — escalate to @interlink_technicalsupport
- Suspended orders: Escalate to @interlink_technicalsupport

### 9. Server / Performance Issues (2+ cases)
**Symptoms**: App slow, timeout, can't claim during peak hours
**Solutions**:
- "The system is currently overloaded, please try again later."
- "We're currently optimizing the server. The issue should be resolved within a few hours."
- Peak hours: 19h-23h UTC+7 typically highest traffic
- Recommend: login before peak hours, avoid high-traffic times

### 10. Banned Account Recovery
**Symptoms**: Account banned, claims "didn't cheat"
**Solutions**:
- "We have banned some accounts for cheating. If you are sure you haven't cheated, please send your ID so we can check."
- Request: ID + device model + explanation
- Common false positive: Changed phone → emulator flag triggered
- "Please provide your Interlink ID, the device you were using, and a screen recording."
**Action**: Collect ID → escalate to @interlink_technicalsupport

### 11. Wallet Issues
**Symptoms**: ETH balance not showing, can't disconnect wallet, can't connect wallet
**Solutions**:
- Balance not showing: "Your funds are on the blockchain and can never disappear. This is a display issue affecting some devices, we're working on it."
- Can't disconnect: "The 'Disconnect' feature is currently experiencing issues. We'll fix this in the upcoming update."
- Can't connect: "Please use a stable internet connection. Try using a VPN if you're in a restricted region."
- Auto-created wallet: "When you register with Google, the system may auto-create a wallet. Go to 'Account' to link your preferred wallet."
**Action**: Ask for wallet address + screenshot

### 12. HHP / Base Rate Issues
**Symptoms**: HHP not updating, base rate reduced, HHP shows 0
**Solutions**:
- "HHP active display may temporarily show incorrectly. The system records the correct value."
- Base rate formula: "Your base rate will be reduced if your HHP is higher than 10.0"
- HHP not displayed: "Please check again, the dev team is fixing this display issue"
**Note**: NEVER disclose the exact HHP formula

### 13. Cheat / Fake Account Reports
**Symptoms**: User reports suspicious accounts, mass referral fraud
**Solutions**:
- Mass inactive referrals: "This account appears to have purchased referrals. We will review and take action."
- Deepfake detection: Handled by AI system automatically
- "Please report suspicious accounts with their IDs. Our team will investigate."
**Action**: Collect IDs → escalate to @interlink_technicalsupport

### 14. Account Hack / Email Change
**Symptoms**: Account hacked, email changed by hacker, can't login
**Solutions**:
- "If you've completed face verification, try logging in with face scan"
- Can't change email: "Currently, email change requires OTP from the old email. If you've lost access to the old email, please try using face verification or other login methods (Telegram, Facebook, Apple)."
- "We cannot provide account email information for security reasons."
**Action**: Ask for original email + Interlink ID → escalate

### 15. HCS (Human Contribution Score)
**Symptoms**: Score fluctuating, showing different values at different times
**Solutions**:
- "HCS is not reduced under any circumstances, please keep monitoring. Note that HCS is shown in decimal form, so 0 after the decimal point has no meaning. For example, 0.26 > 0.2567"
- Display may fluctuate during system recalculation
- "Be active in app and wallet to increase HCS"

---

## Common Response Templates

### Greeting
```
👋 Hello! Welcome to InterLink Technical Support.
I'm here to help you with any questions about the InterLink app — including mining, tokens ($ITL & $ITLG), wallet, account, games, and more.
How can I assist you today? And what language do you prefer? (English is the default)
```

### Need More Info
```
Please provide us with some evidence, including your ID and a screen recording.
```

### Server Issue
```
The system is currently overloaded, please try again later.
```

### Update Required
```
Hello. We've just released a new update and successfully fixed the issue. If you're still unable to log in or encounter any problems, feel free to message us for support.
```

### Escalation
```
I've sent it to our technical team, please wait for their response.
```

### Token Listing
```
You cannot withdraw now. Withdrawal will be available when ITLG token is listed on exchanges — it will be a big surprise. Follow updates: https://x.com/inter_link
```

### Referral Reward
```
When your directly invited friend successfully completes identity verification, you'll receive 500 ITLG and your mining speed will increase by 0.2x. If that friend then invites a new user (indirect referral), you'll receive 250 ITLG and mining speed increases by 0.1x — as long as everyone completes facial verification.
```

### Non-English User
```
English please.
```
(Then after they switch, continue in English)

### Spam Code Warning
```
Country groups are for information exchange only. You can only share codes in the **Human Code** group. If you spam, the moderators might block you from those groups.
```

### Registration Guide (⚠️ GỬI NGUYÊN VĂN)
```
1. Download the App:
 For iPhone: Go to the App Store and search for "Interlink"
 For Android: Go to Google Play and search for "Interlink"
2. Sign Up:
 Open the app and click "Sign Up".
 Enter your ID (A random number sequence created by you, not matching any other InterLink account).
The password consists of 6 digits, created by you, and please remember it
3. Complete Profile & Face Verification:
 Log in, complete your profile, and finish face verification to unlock all features.
4. Go to the 'Human Hash' section, submit the referral code, and once completed, your code will become active.
You can use the code: 1901200219
```
📹 Tutorial: https://drive.google.com/file/d/1mtGeCHLehfvzMldE9_qgFF5nkdVduyHR/view?usp=drive_link

### Forgot Interlink ID
```
Please tap on "Forgot ID" and follow the system's instructions.
```
📹 Tutorial: https://drive.google.com/file/d/1ytm-A7-cTNyREGluEBB3h8gPoaQ1CS65/view?usp=drive_link

### ITLG Burn Explanation (⚠️ GỬI NGUYÊN VĂN)
```
The token burn mechanism is now active, please stay tuned.
If your direct and indirect referrals remain inactive and their total ITLG becomes 0, the referral rewards you previously received from them will be deducted.
```
📹 Burn: https://drive.google.com/file/d/1CTwDOk3b1LT6AgPqTRoJ5w_rsCMfofSA/view?usp=drive_link
📹 Check Burn: https://drive.google.com/file/d/1TKiyC21cPZpmkGkTVzW5sn3RbLSIIACT/view?usp=drive_link

### Wallet Creation
```
Please perform the steps shown in the video on your own account.
```
📹 Tutorial: https://drive.google.com/file/d/1mDRsk1EPbjKRsA51C9ztL4BjMjgRrJ8H/view?usp=drive_link

### Group Creation & Rules (⚠️ GỬI NGUYÊN VĂN)
```
You must complete verification before creating or joining a group.
For a member to be eligible to claim group rewards: The group must have at least 3 members. At least 2 members in the group must be active (e.g., 2/3, 2/4, 2/5).
Among those active members, you yourself must also be active. "Active" means mining at least once per day within the total of 6 mining sessions, and it only counts after you have joined the group (for example, if you mined once before joining the group, it does not count). You can join the group to exchange with other users. https://t.me/interlinkIDchat
```
📹 Tutorial: https://drive.google.com/file/d/1XuRxGWpMdc4IEL0goaJtjSmm8iqJQWmC/view?usp=drive_link

### Referral Code Entry
```
Go to the 'Human Hash' section, submit the referral code, and once completed, your code will become active.
You can use the code: 1901200219
```
📹 Tutorial: https://drive.google.com/file/d/1QfDxCUnwXCrlVdoSVkHTXNUiy29N1-hA/view?usp=drive_link

### ITLG Recovery After Burn (⚠️ GỬI NGUYÊN VĂN)
```
If your ITLG was burned due to inactivity, it will be restored once you complete the full mining streak.
If the burn was caused by your downline being inactive, they need to become active again and complete the mining streak to fully restore the burned ITLG. Once that happens, the ITLG burned from your downline will also be credited back to you.
```

### Seedphrase Check
```
Please follow the tutorial video.
```
📹 Tutorial: https://drive.google.com/file/d/1rGQzCfGiOdjpv2EzieenhBbJJsN_V-Nc/view?usp=drive_link

### Social Connect
```
Please follow the tutorial video.
```
📹 Tutorial: https://drive.google.com/file/d/1nuv6_-dif_J6mApJw6HRIcTHXQlhX5U4/view?usp=drive_link
