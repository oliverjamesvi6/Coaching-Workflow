# Workflow Definition: Client Onboarding & Profile

---

## Scenario Metadata

| Field | Value |
|-------|-------|
| **Workflow Name** | Client Onboarding & Profile |
| **Description** | Qualify a prospective coaching client, capture their profile, and generate a session prep guide before the first coaching call |
| **Outcome** | Coach arrives at the discovery call fully prepared — right questions ready, client profile built, cone-of-possibility framing in place — having done zero manual prep work |
| **Trigger** | Prospective client expresses interest in coaching (in person, text, DM, phone — any channel) |
| **Deliverable** | Client profile document + first-call prep guide |
| **Business Objective** | Maximize the value of the discovery call so the prospect experiences real coaching, has a lightbulb moment, and is motivated to sign up |
| **Current Owner** | Jason (solo) |
| **Lens** | Individual |
| **Pricing Note** | Pricing not yet standardized — flag for separate decision outside this workflow |

---

## Refined Steps

---

**Step 1: Initial Expression of Interest**

- **Action**: Prospective client expresses interest in coaching, usually in a casual in-person or conversational context
- **Sub-steps**:
  1. Prospect pulls Jason aside or brings up coaching in conversation
  2. Jason keeps it conversational — asks "What do you think you want coaching with?"
  3. Light exploration of what they're after — opens their cone of possibility briefly
  4. Jason says: "Let's get on a call next week — it's free, I'll tell you how it works, and we'll go from there"
  5. Discovery call is booked
- **Decision points**: Is this person someone Jason is willing to coach? (gut check — no formal scoring yet)
- **Data in**: Whatever the prospect says in the moment
- **Data out**: Booked discovery call + Jason's immediate impressions held in memory
- **Context needs**: None (fully conversational)
- **Failure modes**: Jason forgets to capture impressions before they fade; call gets booked but no prep happens before it

---

**Step 2: Client Profile Creation (Pre-Discovery Call)**

- **Action**: Jason voice-dictates everything he knows about the prospect into Claude to generate a client profile
- **Sub-steps**:
  1. Jason opens Wispr Flow + Claude before the discovery call
  2. Voice-dictates: who the person is, what they said they want, what he's observed about them over time, what channel they came through
  3. Explicitly notes: only information the prospect has knowingly shared is included (coaching ethics — no snooping)
  4. Claude generates structured client profile from the dictation
- **Decision points**: Is there enough information to generate a useful profile? If not, Claude flags what's missing and Jason fills gaps
- **Data in**: Jason's voice dictation via Wispr Flow
- **Data out**: Structured client profile (see format below)
- **Context needs**:
  - Jason's coaching methodology document (Coactive principles, Kaufman self-actualization framework)
  - Client profile template (Needs Creation)
- **Failure modes**: Jason skips this step and shows up to the call cold; dictation is too vague for Claude to generate a useful profile

---

**Step 3: First-Call Prep Guide Generation**

- **Action**: Claude generates a prep guide for the discovery call based on the client profile
- **Sub-steps**:
  1. Claude takes client profile as input
  2. Generates prep guide (see format below)
  3. Jason reviews — adjusts or accepts
  4. Jason has guide open or memorized before the call
- **Decision points**: Does the prep guide feel right? Jason overrides anything that doesn't fit
- **Data in**: Client profile from Step 2; Jason's coaching methodology
- **Data out**: First-call prep guide
- **Context needs**:
  - Coactive coaching question library (Needs Creation — or pulled from Adam Quiney course notes already uploaded)
  - Kaufman self-actualization spectrum reference
- **Failure modes**: Guide is too generic; Jason ignores it and wings it anyway

---

**Step 4: Discovery Call**

- **Action**: Jason conducts the free discovery call — part explanation of coaching, part actual coaching experience
- **Sub-steps**:
  1. Open with confidentiality disclaimer
  2. Ask what brought them to this conversation (let them lead)
  3. Deliver a taste of coaching — use prep guide questions to open their cone of possibility
  4. Prospect has at least one lightbulb moment ("I never thought of it that way")
  5. Explain the program: AI-generated behavioral change program + weekly coaching calls
  6. Discuss pricing (currently flexible — flag for standardization)
  7. Prospect says yes or no
- **Decision points**:
  - Is this person a good fit? (Jason's judgment)
  - Do they want to proceed?
  - 30-day or 90-day engagement?
- **Data in**: Prep guide from Step 3; whatever the prospect shares live on the call
- **Data out**: Call summary + handoff package for Workflow #2 (Program Generation)
- **Context needs**:
  - Zoom AI summary / meeting notes (if call is on Zoom) — or Jason voice-dictates recap immediately after
- **Failure modes**: No recording or summary captured; handoff to Program Generation is verbal/mental only and data is lost

---

**Step 5: Post-Call Capture & Handoff**

- **Action**: Immediately after the discovery call, Jason captures what AI needs to generate the 30-day program
- **Sub-steps**:
  1. If Zoom: pull AI meeting summary
  2. Jason voice-dictates via Wispr Flow: what behavior needs to change, what accountability structure fits this person, what questions/prompts will elicit the right weekly conversations
  3. Claude appends to client profile
  4. Client profile + call summary become the input package for Workflow #2
- **Decision points**: Did they say yes? If no — workflow ends. If yes — hand off to Program Generation.
- **Data in**: Zoom summary (if available) + Jason's voice dictation
- **Data out**: Complete client onboarding package ready for Program Generation
- **Context needs**: Updated client profile doc; Zoom meeting summary
- **Failure modes**: Jason skips the post-call capture; Program Generation has to start from scratch

---

## Step Sequence and Dependencies

- **Sequential**: Steps 1 → 2 → 3 → 4 → 5 (each depends on the prior)
- **Parallel**: None — this is a linear pipeline
- **Critical path**: 1 → 2 → 3 → 4 → 5
- **Note**: Step 2 and 3 can be collapsed into a single Claude session (dictate → profile → prep guide in one sitting)

---

## Context Shopping List

| Artifact | Description | Used By | Status | Key Contents | AI Accessible? | Readiness Notes |
|----------|-------------|---------|--------|--------------|----------------|-----------------|
| Jason's Coaching Methodology | Coactive principles, Kaufman self-actualization framework, NLP — when to use what | Steps 2, 3 | Exists (partial) | Modality descriptions, when each applies, core coaching questions | Partial | Needs to be written up and stored in a Claude Project |
| Adam Quiney Course Notes | Notes from Quiney's coaching course — question library and frameworks | Step 3 | Exists (uploaded previously) | Coaching questions, cone of possibility framing | Yes — already uploaded | Pull into Claude Project for this workflow |
| Client Profile Template | Structured format for capturing what Jason knows about a prospect | Step 2 | Needs Creation | Name, background, presenting issue, probable deeper issue, self-actualization read, fit signals, red flags | Yes — Claude generates it | Build once, reuse per client |
| First-Call Prep Guide Template | Format for the pre-call guide Claude generates | Step 3 | Needs Creation | What I know about them, presenting vs. deeper issue, self-actualization read, 3–5 opening questions, what to listen for | Yes — Claude generates it | Build once, reuse per client |
| Zoom AI Summary | Auto-generated meeting summary from Zoom | Steps 4, 5 | Exists (conditional) | Call transcript summary, key moments | Partial — requires Zoom account with AI Companion enabled | Confirm Zoom plan supports this; fallback is Wispr Flow dictation |

---

## Prep Guide Format (What Claude Should Generate in Step 3)

1. **What I know about them** — short paragraph from dictation
2. **Presenting issue vs. probable deeper issue** — what they said vs. what's likely underneath
3. **Where they sit on the self-actualization spectrum** — Kaufman read: safety/security vs. growth-oriented
4. **Modality notes** — primarily Coactive; flag where Kaufman framework adds value during the engagement
5. **3–5 opening questions** — designed to open their cone of possibility and give them a taste of coaching
6. **What to listen for** — 2–3 fit signals, 1–2 red flags

---

## Handoff Package to Workflow #2 (Program Generation)

When the prospect says yes, the following must be captured before handing off:

- What behavior needs to change to expand their cone of possibility
- Non-prescriptive but reliable methods to create that change for this person
- What kind of accountability structure fits them
- What questions or prompts will elicit the right weekly conversations

---

*Workflow Definition complete. Copy this output — it's the input for Step 3: Build, where you'll design the AI-powered version of this workflow.*
