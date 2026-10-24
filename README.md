# Real-Time-API-Abuse-Detection-Adaptive-Security
🔍 Overview

APIs are a common target for abuse such as brute-force logins, credential stuffing, scraping and request flooding. A fixed rate limit treats every client the same, which blocks genuine users or misses clever attackers.

SENTINEL takes a different approach. It looks at several behaviour signals together, combines them into a single risk score, and then chooses a response that matches the level of risk instead of a simple allow-or-deny decision.

✨ Key Features
📊 Multi-factor risk scoring from request rate, failed logins, endpoint access pattern and suspicious requests
🔄 Adaptive response with four levels: Allow, Monitor, Throttle, Block
🧾 Explainable decisions: every result lists the exact risk factors that raised the score
🎯 Capped score that never exceeds 100
⚙️ Easy-to-tune thresholds defined as constants at the top of the code
💻 Interactive console interface with a clean security report
🪶 No external dependencies, only the Java standard library

Client details + traffic metrics (input)
              │
              ▼
   Risk Score Calculation  (0 – 100)
              │
              ▼
   Threshold Comparison
              │
              ▼
 ALLOW / MONITOR / THROTTLE / BLOCK
              │
              ▼
  Risk factors + recommended response (report)

  You enter the client IP, API endpoint, HTTP method and four traffic metrics.
calculateRiskScore() adds points for each risk signal found.
getSecurityAction() maps the final score to a security action.
showRiskReasons() explains which signals contributed to the score.
showRecommendation() prints the response to apply.
