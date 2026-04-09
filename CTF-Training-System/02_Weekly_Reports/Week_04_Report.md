# 📅 Training Report 04

**Period:** March 21 – March 27, 2026  
**Duration:** 7 Days  
**Focus Area:** AI Security / Prompt Injection – Gandalf Adventures

---

## Weekly Metrics

| Metric                  | Target  | Actual | Status |
|-------------------------|---------|--------|--------|
| Training Hours          | 5–10    | 7      | ✓      |
| Challenges Solved       | 5–10    | 11     | ✓      |
| Live CTF Participated   | 1–2     | 0      | ✗      |
| CTF Challenges Solved   | 2–5     | 11     | ✓      |
| Writeups Created        | 3–5     | 11     | ✓      |
| New Techniques Learned  | 3–5     | 7+     | ✓      |

---

## Weekly Points Breakdown

| Source                | Points |
|-----------------------|--------|
| Training Hours        | 7      |
| Challenges Completed  | 55     |
| Quality Bonuses       | 110    |
| Live CTF Performance  | 0      |
| Writeups & Learning   | 110    |

**Weekly Total Points:** 282  
**XP Earned This Period:** 1500 XP  
**Cumulative Total XP:** 6320 XP

---

## Category Distribution (Hours This Period)

```
Web Exploitation:     0 hours  [          ] 0%
Binary Exploitation:  0 hours  [          ] 0%
Cryptography:         0 hours  [          ] 0%
Reverse Engineering:  0 hours  [          ] 0%
Forensics:            0 hours  [          ] 0%
OSINT:                0 hours  [          ] 0%
AI Security:          7 hours  [==========] 100%
```

---

## Skill Level Assessment (Self-Rated 1–10)

| Specialty            | Last Period | This Period | Change |
|----------------------|-------------|-------------|--------|
| Linux Fundamentals   | 5           | 5           | 0      |
| Binary Exploitation  | 2           | 2           | 0      |
| Reverse Engineering  | 3           | 3           | 0      |
| AI Security          | 5           | 7           | +2     |
| Prompt Injection     | 5           | 7           | +2     |

---

## Weekly Achievements

- ✓ Completed all 7 Gandalf Adventures challenges
- ✓ Bypassed document-based AI via embedded instruction injection
- ✓ Used emoji encoding to bypass text output filters
- ✓ Exploited logical contradiction in a truth-telling AI
- ✓ Extracted password through constraint-based hint deduction
- ✓ Used thematic roleplay to lower model defenses
- ✓ Successfully injected a competing system prompt
- ✓ Completed all 5 Tongue Tied Gandalf levels
- ✓ 🎉 Reached Level 6 — Intermediate

---

## Adventures Summary

| Adventure        | Strategy                          | Flag       |
|------------------|-----------------------------------|------------|
| Summarizer       | Embedded instruction injection    | PLANETARY  |
| Emoji Gandalf    | Emoji character substitution      | FORTITUDE  |
| Truthteller      | Multilingual logic trap           | ATHENS     |
| Sandolf          | Constraint-based extraction       | SPECIMEN   |
| Halloween        | Thematic story-telling            | CAULDRON   |
| Reverse Gandalf  | System prompt injection           | CITADEL    |
| Tongue Tied L1–5 | Story-telling + ### injection     | Various    |

---

## Weekly Challenges & Lessons

### Biggest challenge this week
Tongue Tied Gandalf Level 5 — required a very specific hard rule injection prompt. Small changes to the prompt caused it to fail. The `###` markers appear to signal training commands, making the injection more reliable.

### How you overcame it
Tested multiple prompt variations. Found that the exact format of the injection mattered significantly. Kept the structure strict and precise.

### Most valuable lesson learned
AI models have multiple layers of vulnerability. Even when direct extraction is blocked, indirect techniques — embedding instructions, encoding output, creating logical contradictions, or injecting new system rules — can consistently bypass defenses.

### Adjustment for next week
Return to binary exploitation:

- Continue picoCTF binary exploitation challenges (Buffer Overflow 1, 2, 3)
- Study GDB debugging
- Practice stack memory layout
