# Detection Engineering Writeups

## Detection 1: Impossible Travel with Token Reuse

### Problem
Token theft allows attackers to bypass MFA and reuse valid sessions.

### Approach
- Correlate login events by user
- Compare geolocation distance
- Enforce time-based constraints
- Validate consistent device/app context

### Outcome
High-confidence detection of session hijacking with minimal false positives.

---

## Detection 2: Anomalous Role Assignment

### Problem
Attackers escalate privileges using legitimate admin APIs.

### Approach
- Identify privileged role assignments
- Compare against historical baseline
- Flag low-frequency actors

### Outcome
Detects insider threats and compromised admin accounts.

---

## Detection 3: Storage Exfiltration

### Problem
Data exfiltration often blends into normal cloud usage.

### Approach
- Monitor blob read operations
- Track access volume and spread
- Compare against baseline behavior

### Outcome
Surfaces stealthy exfiltration attempts without alert fatigue.
