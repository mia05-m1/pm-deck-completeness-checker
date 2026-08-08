# PM Deck Completeness Skill

## Purpose

Evaluate a product release feature deck against essential criteria for documentation. A complete deck contains enough information for a technical writer to generate release notes without contacting the PM for clarification.

## Checklist Criteria

Each criterion is either **PRESENT** or **MISSING**.

If **MISSING**: Flag for PM clarification.

### 1. FEATURE NAME & DESCRIPTION ✓

**Required:** Clear name and concise description of what the feature does.

**Check:** Can you answer "What is this feature?" in one sentence?

**Example Present:**
> "Verify Prepare: Reconciliation preparation powered by AI, with >90% reduction in preparation time while maintaining 100% human control."

**Example Missing:**
> No description; only slide title "New Feature Q3"

---

### 2. PRIMARY USE CASE ✓

**Required:** Specific problem the feature solves or workflow it enables.

**Check:** Can you explain *why* this feature matters to users?

**Example Present:**
> "Move accountants from preparing every reconciliation to reviewing only exceptions that matter."

**Example Missing:**
> "Helps with finance" (too vague)

---

### 3. TARGET AUDIENCE/ROLES ✓

**Required:** Which user roles can use this feature?

**Check:** Are specific roles named (e.g., "Finance Accountant", "Manager")?

**Example Present:**
> "Audience: Finance Accountant (daily user), Close Approver/Controller (approval), Finance Manager (oversight)"

**Example Missing:**
> "For finance users" (which ones?)

---

### 4. WORKFLOW STAGES ✓

**Required:** Step-by-step process or workflow the feature enables.

**Check:** Can you follow the steps a user takes?

**Example Present:**
> "1. Ingest (bank statements, invoices) → 2. Analyze (risk scoring) → 3. Prepare (draft) → 4. Review (accountant) → 5. Approve (controller)"

**Example Missing:**
> "User reviews data" (how? in what order?)

---

### 5. KEY CAPABILITIES ✓

**Required:** Core behaviors or actions the feature supports.

**Check:** Are the specific things users can do clearly listed?

**Example Present:**
> "Confidence scoring, evidence linking, exception flagging, bulk approvals, audit trail"

**Example Missing:**
> "Helps with reconciliation" (how specifically?)

---

### 6. PERMISSIONS/ACCESS CONTROL ✓

**Required:** Who can do what? (Read-only vs. edit vs. approve)

**Check:** Is there a permissions matrix or clear access rules?

**Example Present:**
> "Finance Accountant: read/edit | Controller: read-only | Manager: dashboard view only"

**Example Missing:**
> "Everyone can use it" (undefined access levels)

---

### 7. CONFIGURATION OPTIONS ✓

**Required:** What settings does a tenant admin need to configure?

**Check:** Are there defaults? Required vs. optional settings?

**Example Present:**
> "Confidence threshold (default 85%), materiality amount (default $25K), approval chain, evidence required (yes/no)"

**Example Missing:**
> "Configurable settings" (which ones?)

---

### 8. ROLLOUT PLAN / AVAILABILITY ✓

**Required:** When is this available? To whom? In what phases?

**Check:** Is the timeline and customer eligibility clear?

**Example Present:**
> "Phase 1 (Late July-Aug): default OFF for existing tenants, opt-in. Phase 2 (Sept-Oct): default ON for new customers. Phase 3 (Nov+): default ON for all."

**Example Missing:**
> "Coming soon" (when? for whom?)

---

### 9. INTEGRATIONS/DEPENDENCIES ✓

**Required:** What systems does this connect to? What's required?

**Check:** Are integrations listed (GA, preview, planned)?

**Example Present:**
> "GA: Snowflake, bank feeds, cloud storage. Planned: Workday, NetSuite, Dynamics"

**Example Missing:**
> No mention of integrations (does it need any?)

---

### 10. PERFORMANCE METRICS / IMPACT ✓

**Required:** Measurable improvement or scale (if applicable).

**Check:** Are numbers provided (time savings, accuracy, volume)?

**Example Present:**
> ">90% reduction in preparation time, 93% accuracy rate, 15-20 min review time (vs 45-60 min)"

**Example Missing:**
> "Saves time" (how much?)

---

### 11. KNOWN LIMITATIONS OR CONSTRAINTS ✓

**Required:** What doesn't this feature do? What are the constraints?

**Check:** Are limitations explicitly stated?

**Example Present:**
> "Locked reconciliation cannot be modified without exception handling. Evidence export scheduled for next release."

**Example Missing:**
> No mention of limitations (are there none, or just not documented?)

---

### 12. SYSTEM REQUIREMENTS / PREREQUISITES ✓

**Required:** What does a user/tenant need to use this?

**Check:** Browser? Data preparation? Plan tier? Permissions?

**Example Present:**
> "Requires: Standard tier and above, Tenant Admin setup, active integrations to source systems"

**Example Missing:**
> No prerequisites mentioned (are there none?)

---

### 13. TRAINING / ENABLEMENT PLAN ✓

**Required:** How will users learn to use this?

**Check:** Are training materials, guides, or Q&A sessions planned?

**Example Present:**
> "30-45 min recorded module for Accountants, 20-30 min for Controllers, 60 min for Admins, live Q&A sessions"

**Example Missing:**
> "Training will happen" (when? what format?)

---

### 14. SUPPORT / SLA / ESCALATION PATH ✓

**Required:** Who do users contact if something breaks? What's the response time?

**Check:** Is there a support model documented?

**Example Present:**
> "Contact: CSM for top-tier accounts, help.center for self-serve, escalation path defined"

**Example Missing:**
> No support information (unclear who to contact)

---

### 15. SECURITY / COMPLIANCE / DATA HANDLING ✓

**Required:** Any security or compliance notes? GDPR? Encryption? Audit trails?

**Check:** Are sensitive data considerations documented?

**Example Present:**
> "Audit trail on all actions, 100% human control retained, encrypted data in transit"

**Example Missing:**
> No mention of security/compliance (assumed handled elsewhere?)

---

## Scoring

**PRESENT** = +1 per item
**MISSING** = flag for clarification

### Interpretation

- **15/15 PRESENT** → COMPLETE (proceed with release notes)
- **12-14 PRESENT** → MOSTLY COMPLETE (minor gaps, consider contacting PM)
- **9-11 PRESENT** → INCOMPLETE (3+ gaps, recommend PM clarification before starting)
- **<9 PRESENT** → BLOCKED (too many gaps, cannot proceed without PM input)

## Important Rules

### 1. Don't Guess

If a criterion is unclear or missing, mark it **MISSING**.

Do not infer from related slides.

Example:
- Deck mentions "Accountant reviews output" but doesn't list permissions.
- Mark PERMISSIONS as MISSING.
- Do not assume "Accountant can edit."

### 2. "Not Specified" is Valid

If the deck genuinely doesn't mention limitations or system requirements:

Mark as MISSING, but note:

> "Not specified in deck (may not apply, or may be documented elsewhere)"

### 3. Examples Aren't Proof

If the deck shows an example configuration but doesn't explain which settings are configurable:

Mark CONFIGURATION as MISSING.

Do not assume other settings exist.

### 4. Separate Complete from Correct

This skill checks **completeness**, not accuracy.

Example:
- Deck says "Available August 15"
- Checklist marks "AVAILABILITY: PRESENT" ✓
- Fact-checking (is August 15 accurate?) is a separate task

## Usage in Documentation Workflow

1. Writer receives PM deck
2. Runs completeness check
3. Gets report:
   - Items present
   - Items missing
   - Flagged for PM clarification
4. Writer decides:
   - **CRITICAL** (e.g., "What are the permissions?"): Contact PM now
   - **NICE-TO-HAVE** (e.g., "FAQ not mentioned"): Proceed without it

5. Writer starts release notes using present items
6. Writer adds specific clarification requests to PM

---

## Example Completeness Report

```
FEATURE: Verify Prepare (Reconciliation AI)

PRESENT (13/15):
✅ Feature name & description
✅ Primary use case
✅ Target audience/roles
✅ Workflow stages
✅ Key capabilities
✅ Permissions/access
✅ Configuration options
✅ Rollout plan
✅ Integrations
✅ Performance metrics
✅ Training plan
❌ Known limitations
✅ System requirements
✅ Support/SLA

MISSING (2/15):
❌ Known limitations — Slide mentions "once approved, locked" but no comprehensive limitation list
❌ Support/SLA — No mention of support response time or escalation path

SUMMARY:
Deck is 87% complete. Recommend brief clarification on:
1. Full list of known limitations (Accountant-facing)
2. Support tier/SLA for this feature

Status: MOSTLY COMPLETE — Proceed with clarification
```
