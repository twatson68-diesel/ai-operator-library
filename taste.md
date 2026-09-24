# Taste profile — AI Operator Library

This is the rubric the weekly refresh scores against. It is meant to be edited. Tell me a change in plain language and I rewrite this file, republish it, and the next run uses the new rules.

**Owner:** Tim Watson · CEO, SMART Asset Management (pallet/rack pooling, logistics) and SMART Pest Prevention
**Last updated:** 2026-09-24 (Voice UI track added)
**Core feed (follow this):** https://ai-operator-library.pplx.app/feed.xml — top 3 per layer
**Full feed:** https://ai-operator-library.pplx.app/full.xml — everything

---

## What he is building

A personal AI system on two frameworks:
- **Nufar Gaspar's Agent OS** — seven layers: Identity, Context, Skills, Memory, Connections, Verification, Automations
- **Karpathy's LLM Wiki** — `raw/` immutable sources → `wiki/` pages the model writes → `CLAUDE.md` schema, `/ingest` `/lint` `/query` `/digest`

Stack in play: Claude (Chat, Cowork, Code), Perplexity, Notion as control plane, Salesforce, Tableau, Zapier, Dropbox, Granola, Obsidian-adjacent markdown.

---

## Level gate — added 2026-08-23

Tim has outgrown introductory material. **Reject anything that announces its own level**: "101", "explained", "clearly explained", "getting started", "for non-technical people", "full beginner tutorial", "in N minutes", "complete guide to X" where X is a single feature. He can already build skills, context files, and harnesses — an episode has to tell him something he could not have written himself.

**Second Brain is closed.** No note-taking, Obsidian vaults, LLM-wiki builds, or personal knowledge base construction. The L0 feed was retired on 2026-08-23.

## Active interests

Focus topics as of 2026-09-24:

1. **Token optimization** (T6) — what agents cost to run. Context-window efficiency, context rot, compaction thresholds, prompt caching and cache economics, model routing to cheaper models for cheap subtasks, token budgets and per-agent cost accounting, and where spend actually leaks: long tool outputs, verbose system prompts, retry storms, runaway crons, subagent fan-out. Measured results earn a slot — "cut boot tokens by N%", "$X/month to $Y". Long-context vs RAG counts when framed as a cost decision, not a quality one.

2. **Claude Code best practices** (T7) — how experienced people actually run it. CLAUDE.md design, subagents and delegation, parallel agents and worktrees, hooks, slash commands, custom skills, output styles, MCP wiring, permissions and allowlists, plan mode, context management, session handoff, and honest accounts of what broke. Tool comparisons only when the lesson is about running Claude Code better.

3. **Conversational voice as a UI** (T8, added 2026-09-24): talking to his agents instead of typing. Turn-taking and endpointing, meaning when the agent decides he has finished speaking. Also barge-in and interruption handling, the latency budget from speech to first audio, speech-to-speech models vs STT→LLM→TTS pipelines, voice agent frameworks (Pipecat, LiveKit Agents, OpenAI Realtime, ElevenLabs Agents, Vapi), and designing the conversation itself: pacing, confirmations, how an agent reads back a list. Why it matters: he runs voice front ends on his own agents (Lex mobile, a voice iOS build) and has a standing rule that a voice agent waits until he finishes and answers at a deliberate pace. **Reject:** voice AI as a business (call-center ROI, selling voice agents), TTS model launches, voice cloning, and podcasts about podcasting.

Secondary, still live: **collaborating agents** (T2) and **graphs** (T3).

Retired — do not re-add, do not treat as dormant: Second Brain (08-23), Memory (09-05), OpenClaw (09-07), Semantic Layer (09-07), Context (09-07), Verification (09-07), **Hermes (09-10)**.

**Pattern worth respecting: seven topics retired in 18 days, and Hermes was the declared focus for three of them before being cut.** Interests here turn over fast. Prefer a tight, high-signal set per topic over exhaustive coverage, and don't spend heavy verification effort deepening a topic that is only days old.


## Feed size rule

The library grew to 82 episodes and became unusable — Tim reported not paging down far enough to reach things. Two feeds now:

- **Core feed** (`core.xml`) — the one he follows. Rebuilt 2026-09-03. Three rules now: anything added in the last **30 days** surfaces ahead of the standing picks (capped at 3 per layer so a big topic add can't flood it), then the strongest **3 per layer** standing (HIGH tier first, builds first), and anything he has **already finished is withheld entirely**. Currently 40 episodes. The old flat 3-per-layer rule meant new additions were invisible — 5 Hermes episodes were added on 2026-09-02 and only 1 reached this feed.
- **Full feed** (`full.xml`) — everything, for when he wants depth on one layer.

Global episode numbers are shared across both feeds, so `#43` always means the same episode. When a new episode enters a layer that already has 3 core slots, it goes in the full feed and only enters core if it beats an incumbent — say which one it displaces and why.

Artwork is composed locally, not hotlinked: the source episode image with an opaque bottom band carrying the original show name and the `NN · Lx` chip. Files live in `site/art/`, mapped in `artmap.json`. Apple binds a custom feed's episodes to that feed's show identity, so burning the show name into the image is the only way it shows in a list view.

## Relevance gate — applied first, before anything else

**An episode must help Tim build or run HIS system.** If it teaches someone how to start or grow an AI business, sell AI services, or run a company that is not his, it is rejected — no matter how many Auto-include criteria it hits.

The test: after listening, could he change a file, a workflow, or a decision inside SMART Logistics, SMART Pest, or his personal Agent OS? If the answer is "he could start a different business," that is a reject.

This gate exists because on 2026-08-16 three Build With AI episodes about making money with Codex passed Auto-include cleanly on "live build + non-engineer + favored show."

## Auto-include

Applied only after the relevance gate passes. An episode gets added without asking if it hits **two or more**:

1. **Live build** — someone builds a working thing on air, start to finish
2. **Names a specific artifact** — a file, folder structure, slash command, rubric, schema, or prompt you could recreate
3. **Non-engineer operator** as the builder or subject
4. **Fills a thin layer** — currently Verification and Memory, in that order
5. **From a favored show** — The Cognitive Revolution, How I AI, Build With AI, The AI Daily Brief (Operators/Build cuts only), The Startup Ideas Podcast, Master Claude Chat/Cowork/Code, AI & I
6. **Read-across to his businesses** — logistics, supply chain, CRM/Salesforce, data warehouses, back-office finance, field service, roll-up and valuation economics

## Auto-reject

Dropped regardless of how good it is:

- MCP or any protocol/standard **as the subject** (fine as plumbing inside a personal build)
- Model releases, benchmarks, scaling debates, capability speculation
- Funding rounds, company strategy, AI policy, regulation, safety/alignment as the main topic
- Enterprise rollout at large headcount, org change management, "future of work"
- Guest interviews that are mostly about the guest's company
- Pure research: interpretability, architectures, training methods
- Anything requiring real engineering to reproduce

## Known exception

**The Cognitive Revolution gets a wider lane.** He likes the show on its own merits. Operator-judgment episodes that fail the build test still qualify if they carry hard numbers, a named framework, or a thesis touching his businesses — these land in **Layer 8 · Judgment**. Cap Layer 8 at 6 episodes so it doesn't crowd the build layers.

---

## Style rules for the entries

- One line per episode, content-derived. Name the actual technique, file, or number.
- No filler: never "great overview," "deep dive into," "must listen."
- Tag **BUILD** vs **Method** honestly. Method-only episodes sort last inside a layer.
- Every episode title carries the show name and air date: `NN · Lx · Show Name · YYYY-MM-DD · Title`. The show name has to live in the title because Apple binds every episode in a custom feed to that feed's show identity — it will always label the show as "AI Operator Library," so the title is the only field where the original show can appear. The feed's own pubDate stays synthetic to preserve rank order, so the title is the only place the true air date shows in Apple.
- Assign exactly one layer. When it straddles, pick the layer he'd be in when the episode helps most.

---

## BANNED SHOWS — never include, no exceptions

- **OpenClaw Cast** — banned 2026-09-05. Tim: "Don't ever include OpenClaw Cast podcasts. They are terrible." Do not add episodes from this show to any feed, do not surface it as a near-miss, and do not propose mining its back catalogue. Its 2 episodes were removed on the day of the ban.
- **AI-narrated shows with no human practitioner** — Neural intel Pod, Impact Vector, Agentic AI at Work, AI Odyssey, Rapid Synthesis, Colaberry AI Podcast, Intellectually Curious, AI Fire Daily, Awesome Agents, Models & Agents, My Weird Prompts. These rank well on agent keywords and are worthless.

## Feedback log

- `2026-09-24`: **Added T8 Voice UI, 15 episodes (#109-123)**, from 35 researched and 20 rejected. Scope is running a voice front end on his own agents. That means turn-taking and endpointing, barge-in, the latency budget, speech-to-speech vs chained pipelines, frameworks (Pipecat, LiveKit, ElevenLabs, Vapi) and conversation design. GATES: the **relevance gate did the most work**. Voice AI is dominated by call-center and sales-dialer content, so Perk's "10,000 calls a week", Convo AI's "Hidden Complexities of Enterprise Voice" and VUX World's chatbot-to-voice all fell as somebody else's business. Also dropped as thin or vendor-led: Hamming testing, Vodex, the Google Live API, and the Boson avatars episode. The AI-narrated rule killed 5, including two HackerNoon read-aloud articles; one of them, an AssemblyAI latency playbook, had genuinely good content. Two non-English episodes were dropped (Hebrew, French). CORE: FOCUS for VOICE was set to 3, not 5, after the first build put 10 voice episodes in core and pushed it to 57. Core now carries 6: the three live builds (Killian Lucas, LiveKit, Todoist Ramble) and the three turn-taking episodes. RULE STRAIN: Headcount Zero's Twilio + Realtime barge-in build was rejected on *suspicion* of AI narration, not confirmation. The ElevenLabs and OpenAI Realtime teams are thin: one ElevenLabs guest, zero from OpenAI Realtime.

- `2026-09-20` — Weekly run #7. 37 new items in the window, 4 added, **prune skipped a second week**. Added: Agentic Conversations' "Why Cost Per Million Tokens Is A Useless KPI?" → Token Ops (Palo Alto Networks' AI-finance lead at FinOps X on why their AI-spend dashboards went useless); Superlinear's "Fall 2026 Workflow for Starting Projects with Coding Agents" → Claude Code (less harness engineering, more steering on decisions that compound); SED's "Scaling Agent Workloads at Vercel" → Agent Teams (what breaks past one-user-one-session); Master Claude ep. 8 "Scheduled and Delegated Work" → Automations. GATES: the news/roundup rule did the heavy lifting again — six AI Daily Brief episodes, ThursdAI and Cognitive Revolution's AI:AM all rejected. Level gate killed Startup Ideas' "Instinct AI: The AI Assistant for normal people". **RULE STRAIN: Master Claude shipped six Beyond Prompting episodes in seven days and only one earned a slot.** A single show flooding the window is a new pattern; if it repeats, cap per-show additions per run. NEW FEED: Agentic Conversations (the renamed MLOps feed) is producing genuine cost-accounting material — first addition from it. **MAC SCHEMA CHANGE: `ZDURATION` no longer exists on `ZMTEPISODE` in Apple Podcasts. `ZPLAYCOUNT` survives and remains the completion signal; the prune query must drop the duration column.**

- `2026-09-13` — Weekly run #6. 30 new items in the window, 3 added, **prune skipped — his Mac timed out twice and I stopped rather than retrying**. Added: Superlinear's "New Model Dropped? 4 Ways to De-slop Your Project" → Token Ops, which treats a model release as the trigger to delete accumulated cruft rather than just swapping models; Master Claude's "Claude Surface Map" → Claude Code, on picking Chat vs Cowork vs Code by reach; ADB's "Multiplayer AI Sprint" → Agent Teams. GATES: the model-release rule did most of the work this week — GPT-6 Astra coverage alone accounted for four rejections across ADB, Super Data Science, Startup Ideas and ThursdAI. Level gate killed Startup Ideas' "Local AI Clearly Explained". Roundup rule killed TCR's AI:AM Highlights, SED News and two ADB news episodes. NEW SOURCE WORTH WATCHING: **Superlinear** is a strong fit for both current tracks — its back catalogue includes "Context Hygiene for Coding Agents", "Beyond Root-Level Harness Engineering" and "Give Coding Agents Eyes Beyond the Chat". Not backfilled, per the two-week rule on young topics. FEED QUIRKS: Superlinear's feed has no per-item `<link>` (resolve via itunes id 6794345650); Forward Deployed's substack id 179088941 returns 0 items and needs re-resolving.

- `2026-09-10` — "Remove Hermes and open claw as topics... New topics: token optimization; Claude code best practices." Retired **Hermes (16 episodes)**, archived and reversible; OpenClaw was already gone from the 09-07 cut, so nothing to do there. Registered **T6 Token Optimization** and **T7 Claude Code**. Hermes had been the declared focus for exactly three days, and 7 of its 16 episodes were added on 09-07 specifically to deepen it — which is now sunk effort. Adjusted the approach accordingly: `FOCUS` in emit_v2.py now gives each new topic 6 core slots rather than 10, and the rubric records that interests here turn over in days, so new topics get a tight high-signal set rather than an exhaustive sweep.

- `2026-09-07` (later) — Backfilled Hermes from 9 to 16 after the retirement left it thin: Eric Siu's operator numbers and his "kneecapped" config episode, two Wes Roth install walkthroughs, How I AI with Alex Finn on 24/7 local hardware, Intelligent Machines 874 with Jeffrey Quesnelle, and Fix My Business on framework churn. Also weighted core toward the focus topic — `FOCUS = {"HERMES": 10}` in emit_v2.py gives Hermes 10 slots instead of 3, so it is now 15 of 35 core episodes instead of competing evenly with dormant layers. CORPUS REALITY, third confirmation: mainstream dev and homelab shows have ZERO Hermes-agent episodes — Latent Space, MLOps, TWIML, Changelog, SE Daily, Syntax, Self-Hosted, LINUX Unplugged, Talk Python all checked. The deepest build material is non-English (Spanish Atareao ATA 807 on config decisions, French Big Data Hebdo 231 on the five-layer harness and ~10ms memory retrieval). If he wants more depth, translation is the only remaining lever. Dropped Julian Goldie's VPS episode despite good content — its episode page 404s.
- `2026-09-07` — "remove open claw, semantic layer, open claw, contest, verification. im particularly focused on hermes use and build right now." Retired **OpenClaw (12), Semantic Layer (19), Context (8), Verification (9) = 48 episodes**, all archived and reversible. Read "contest" as Context, the only plausible match. Library 132 → 85, core 42 → 26. Checked first that no Hermes material was buried inside the doomed layers — none was. FOUND A REAL GAP: 4 of the 48 lived in `tcr_adds.json`, a second episode source `emit_v2.py` merges that I had never checked during a retirement; the build threw `KeyError: 'VERIFICATION'` and caught it. Any future layer retirement must purge BOTH `v2.json` and `tcr_adds.json`. Also worth noting the trajectory: five topics retired in 16 days, and OpenClaw was killed one day after I added two OpenClaw episodes to it. Additions to a young interest may not be worth the verification cost until it has held for a few weeks.

- `2026-09-06` — Weekly run #5. Pruned 13 newly finished episodes (all of Identity's remaining picks, three Context, three Skills, three Connections, one Verification, one Agent Teams) — 28 now archived as listened. 104 new items in the window but only 38 were real: **Tina Huang's feed dumped 66 back-catalogue YouTube re-uploads** with fresh pubDates, all career and beginner content ("stop being lazy", "Why You Can't Find A Job", "Vibe Coding 101"). Added 5: How I AI's Grok-Bot-vs-OpenClaw stack migration and ADB on OpenClaw 2.0's multiplayer workspace → OpenClaw; ADB with **Nufar Gaspar** on agentic loops → Automations; Joe Reis on "death of data teams" → Semantic Layer, filling the thin critique angle; How I AI's self-improving PM assistant → Skills. GATES: relevance gate killed four Build With AI money-making episodes and two Startup Ideas; model-release rule killed both ThursdAI GPT-6 episodes, ADB on Fable 5.1, and How I AI on GPT-6 Astra; roundup rule killed TCR's AI:AM Highlights and Super Data Science's ICYMI. RULE STRAIN: The Cognitive Revolution's MongoDB episode on retrieval and agent memory was rejected only because Memory was retired yesterday — the topic is dead but adjacent material will keep arriving, so this will recur. Dropped The Data Exchange's agent-cost episode despite good content: its site 404s and the Apple lookup returned nothing, so no verifiable episode page.

Append every signal here, newest first. Format: `date — signal → rule change`.

- `2026-08-20` — Show name not visible in Apple → moved it into the episode title (`NN · Lx · Show · date · Title`), since Apple always renders titles but binds the show label to the feed itself. Artwork was checked against Apple's spec (square, 1400-3000px, JPEG/PNG) and 0 of 10 sampled failed, so episode art is valid — Apple simply shows it on the episode detail and Now Playing screens rather than the list, and caches aggressively.
- `2026-08-20` — Between-window gap found: a windowed run can miss episodes published before the window opens. Two back-catalogue finds added — Master Claude "Managing Context Rot" → Memory (takes it off 4), and Practical AI "Models, Harnesses, and Multi-Agent Systems" → Automations, which covers the harness idea the Latent Space episode would have. FIX FOR FUTURE RUNS: check each show's newest item against the last run date rather than trusting a fixed 8-day window.
- `2026-08-20` — Off-cycle run #2 (Tim asked to run now). 25 in window, 13 not previously judged, 4 added: Claude Code as an AI employee → Identity; skillsmaxxing / skills as SOPs → Skills; AI Engineering Skills Map → Context; solo founder + Codex for a physical product → Skills. RELEVANCE GATE WORKED: both Build With AI client-signing episodes were rejected automatically instead of needing a manual override. Judgment call worth flagging: the Yana Bana episode is a founder story, which brushes the gate, but kept for the physical-product-without-engineers parallel — say the word if that's too loose. MEMORY got nothing again and is now the only single-digit layer at 4.
- `2026-08-20` — "Add the picture from the episode" → every item now carries `<itunes:image>`. 66 of 76 use the show's real per-episode artwork joined on the audio URL; Build With AI and AI & I publish no per-episode art at all, so those 10 fall back to channel artwork. Site cards show thumbnails too. Any future addition must carry an image or fall back to its show's channel art.
- `2026-09-05` (later) — "Don't ever include OpenClaw Cast podcasts. They are terrible." BANNED. Removed both episodes that were in the library. This retroactively kills the back-catalogue mining I had proposed three times — that recommendation was wrong and should not have been repeated after the first non-answer. Note the lesson: I judged that show by its titles and description rather than by whether Tim actually valued it, and I pushed it hard on that basis. The T1 OpenClaw TRACK stays — the ban is on the show, not the software.
- `2026-09-05` — "Remove all the stuff about memory, it's not helping me get where I want to go. I'm really interested in Hermes." MEMORY (L4) RETIRED — 3 episodes archived to retired.json (How I AI's Claude Code life operator, the Lindy Teammate episode that anchored the Memory brief, Master Claude on context rot). CAUGHT BEFORE DELETING: two of the five Hermes episodes were living inside the Memory layer and would have been destroyed by a literal reading of the request. Pulled them out first. HERMES promoted from a scattered topic tag to **Track 5**, purple, 10 episodes — the 5 existing ones consolidated from four different layers plus 5 new. Honest note for future runs: the English-language Hermes Agent podcast corpus is genuinely thin. The framework is ~7 months old and roughly half of everything indexed on the keyword is AI-narrated slop. 10 is close to the real ceiling right now; the richer vein for the same practical itch is the OpenClaw Cast back catalogue, 20 unmined audio episodes on running an agent harness in production.
- `2026-09-04` (later) — "Refresh the Apple Podcasts artwork now." Apple caches channel art by URL and never refetches the same path, so republishing cover.jpg had no effect. Fixed by versioning the filename (cover-20260904.jpg plus all 12 layer covers) and pointing every feed at the new path. Also rewrote the core feed description, which still described "a Second Brain layer" and "the strongest three per layer" — both untrue since the L0 retirement and the 2026-09-03 core rebuild.
- `2026-09-04` — Screenshot check on which feed to unfollow. Confirmed he was looking at the LIVE feed (top episode 27 · L4 · Practical AI · Hermes), not the dead pplx.app one (top episode 01 · L0 · Build With AI). Note the dead feed still returns 200 on GET - only HEAD fails - so it has been quietly serving retired Second Brain episodes. Also caught stale cover art reading "82 EPISODES · 39 BUILDS · 8 LAYERS" against an actual 127 / 45 / 8 layers + 4 tracks; make_cover.py hardcodes these, so regenerate whenever totals move.
- `2026-09-03` — "Are these in my feed now? How do I automate this?" Found that only 1 of 5 Hermes episodes had reached core, because the flat 3-per-layer rule had no notion of recency. Rebuilt core_pick with a 30-day fresh window capped per layer. Read his Apple Podcasts DB and retired the **15 of 36** core episodes he has finished — all of Identity, most of Context and Connections, and the Lindy Teammate episode that anchored the Memory brief. Play state note: ZPLAYCOUNT is the only reliable completion signal on his Mac; ZPLAYHEAD and ZHASBEENPLAYED are both 0 even for finished episodes. Also discovered he still has the dead pplx.app feed subscribed alongside the GitHub one. Topic add/retire/prune is now a saved skill rather than an improvised pipeline.
- `2026-09-02` — "Find episodes about Hermes ai." Two different subjects share the name: the Nous Research open-weight model family (Hermes 3/4/4.3) and Hermes Agent, the self-improving open-source agent framework released Feb 2026 and routinely compared to OpenClaw. Only the AGENT subject is in scope — the model releases are auto-rejected as model news. 5 added: Practical AI with Nous CTO Jeffrey Quesnelle and Behind the Craft with co-founder Karan Malhotra → Memory (the skill-writing learning loop is exactly the Memory-layer mechanism, and Memory was thinnest at 3); OpenClaw Cast's Hermes-vs-OpenClaw comparison → OpenClaw; The Growth Podcast with OLX's CPO → Agent Teams; This Week in AI founders panel → Judgment. GATE PRESSURE: both Startup Ideas Hermes walkthroughs are titled "clearly explained" and died to the level gate despite being hands-on screen-shares — this is the second time that gate has killed a genuinely practical Startup Ideas episode, and it may need a carve-out for demo walkthroughs. Also rejected a cluster of AI-narrated feeds (Neural intel Pod, Impact Vector, Agentic AI at Work) that rank well on Hermes keywords but have no human practitioner. STRUCTURAL FINDING: OpenClaw Cast has 22 real audio episodes and only 1 was in the library — the "ClawCast is video-only" note applied to the blog feed, not this show. Its back catalogue is highly practical and should be mined.
- `2026-09-01` — "Add a new topic: semantic layer." → Added as active interest #4 and as track T4. Scope covers the product category, the agent-to-data interface angle, ontologies as substrate, and critiques. Specialist analytics feeds added to the in-scope list since this topic barely appears in mainstream AI shows.
- `2026-08-30` — Weekly run #4. 27 since last run, all unjudged, 3 added: How I AI's $20k-on-Devin accounting → Agent Teams; GraphGeeks Brad Bebee on graphs as painkiller → Graphs; AI Daily Brief on the OpenAI rogue-agent incident → Verification. GATES DID REAL WORK AGAIN: the level gate killed three Everyday AI "Start Here" episodes plus ADB's "How to Start AI Coding If You Haven't Yet" and Startup Ideas' "WebMCP clearly explained"; the relevance gate killed all three Build With AI money-making episodes; the MCP-as-subject rule killed Practical AI's Agentic AI Foundation episode. NEW FEED DEFECT: GraphGeeks reuses one `<link>` (https://www.graphgeeks.org/) for every episode, so URL-based dedupe silently collided with last week's GraphGeeks addition. Resolved both via the Apple lookup API and repaired last week's placeholder link. Two near-misses flagged for Tim: ADB "What the Top AI Users Are Doing Differently" (advanced-user gap widened 2.6x → 8.3x) and TCR's Apollo Research episode on RL metagaming and reward seeking, rejected only by the pure-research rule.
- `2026-08-23` — Weekly run #3. 28 in window, 22 unjudged, 3 added: GraphGeeks construction-risk graph AI → Graphs; Latent Space Joon Sung Park on simulation → Agent Teams; Startup Ideas Grok Bot one-person company → Agent Teams. THE LEVEL GATE DID REAL WORK: it killed all five Everyday AI "Start Here" episodes and Build With AI's "AI Concierge Explained in 19 Minutes" automatically. Two judgment calls flagged for Tim: the Joon Sung Park episode leads with a $2B Series B (normally an auto-reject) but the substance is agent-society simulation, and ADB's "9 AI Techniques You Probably Haven't Tried" was rejected as a roundup despite covering team agents. Startup Ideas again shipped an item with no <link>; resolved via the Apple lookup API.
- `2026-08-23` — "Skills episodes are too basic for me now. And I'm done with 2nd brain. Now I'm interested in open claw, collaborating agents, and graphs." → Retired the L0 Second Brain feed (8 episodes). Cut 7 self-declared beginner episodes across Skills and Identity. Added three topic tracks: OpenClaw (13), Agent Teams (17), Graphs (15), from 44 researched of which 39 had reachable audio. Added the level gate above. Library went 82 → 101. NOTE: the ClawCast, the only feed with sustained OpenClaw internals coverage, is video-only on YouTube/Spotify with no audio enclosures — 5 of its episodes cannot enter a podcast feed and need a YouTube track instead.
- `2026-08-20` — Approved the relevance gate → added above as the first test, ahead of Auto-include. Approved both near-misses: Everyday AI "Scheduling AI" added to Automations; Latent Space "React for Agents" could NOT be added — Latent Space published it as a written post with video and no podcast audio (`podcast_upload_id` is null), so it has no enclosure and cannot play. Listed under Not in the feed with its link instead. Also restructured every description to lead with the show name and carry a clickable link to the original episode.
- `2026-08-17` — "Add the date aired to the feed" → original air date now appears in every episode title as `NN · Layer · YYYY-MM-DD · Title` and as the first line of every description. Synthetic pubDate retained so rank order survives.
- `2026-08-16` — Weekly run #1: 27 candidates in the 8-day window, 4 added (Claude Code for normal people → Skills; AI Deputization Audit → Context; Lindy Teammate → Memory; AI-Native Company → Automations). RULE STRAIN: all three Build With AI episodes this week passed Auto-include on 'live build + non-engineer + favored show' while being about starting an AI services business, with no read-across to any layer. Rejected them manually. Proposed fix pending Tim's call: add a required relevance test — an episode must help build or run *his* system, not somebody's business. Also noted the Latent Space feed now mixes daily AINews newsletter items into the podcast feed; those are auto-rejected as model-release coverage but they inflate the candidate count.
- `2026-08-12` — Cut too much Cognitive Revolution in the v2 rebuild → added the wider-lane exception above; TCR is now mined across its full archive, not sampled.
- `2026-08-12` — "Less infrastructure, more things I can use and implement" → MCP-as-subject moved to auto-reject; build-alongs sort first in every layer.
- `2026-08-11` — Noticed MCP was over-represented → root cause was the research brief naming MCP twice, not a real signal about the field.

## How to give feedback

Anything works. Useful shapes:

- `"#34 was great, more like that"` → I infer the trait and write it into Auto-include
- `"#57 was a waste"` → the trait goes to Auto-reject and the episode is pulled
- `"too much X"` / `"not enough Y"` → I reweight the layers
- `"add show Z"` / `"drop show Z"` → show list changes
- `"I'm past Identity, working on Memory now"` → the thin-layer priority reorders and the weekly run hunts there

Episode numbers from the feed titles are the fastest reference — `01`, `34`, `57`.
