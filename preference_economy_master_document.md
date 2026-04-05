# The Sovereign Discovery Agent
### An Idea File for the Preference Economy

> *Andrej Karpathy said: in the agent era, you don't share the app — you share the idea. Your agent builds it for your specific needs. This is that idea.*

---

**The Attention Economy is ending.**

For 25 years, Google, Meta, and Amazon have built trillion-dollar businesses on a single lie: that the discovery mechanism of the internet is working for you. It isn't. It is working for the advertiser.

An AI agent doesn't click on ads. It doesn't get distracted by sponsored listings. It executes — based purely on what *you* actually want.

This document is the complete architectural, economic, and strategic blueprint for what comes next.

**Fork it. Build it. Improve it. This idea belongs to anyone willing to execute it.**

---

## What This Is

A privacy-first, user-centric discovery layer that sits between the individual and the internet. Instead of a search engine, the user employs a personal AI agent with a cryptographically secure understanding of their preferences — a **Taste Graph** — that scours the internet, negotiates with other agents, and pays for premium data autonomously.

No ads. No manipulation. No platform optimizing against your interests.

---

## The Eight Parts

| # | Section | What it covers |
|---|---------|----------------|
| 1 | [The Core Engine](#part-1-the-core-engine-and-the-autonomous-taste-graph) | The Taste Graph, cold start problem, implicit signals, local graph architecture |
| 2 | [The Multi-Agent Ecosystem](#part-2-the-multi-agent-ecosystem) | Monitor Agent, Discoverer Agent, Purchaser Agent |
| 3 | [The Payment Architecture](#part-3-the-two-layer-payment-architecture) | Web2 UX + Web3 backend, x402 protocol, the spread, the float |
| 4 | [Technical Roadmap](#part-4-the-technical-build-roadmap) | 4-phase build: Web2 shell → Graph engine → Wallets → Discovery layer |
| 5 | [The Strategic Moat](#part-5-the-strategic-moat-and-the-exit) | Why the Taste Graph creates negative churn and an exit thesis |
| 6 | [Competitive Landscape](#part-6-the-competitive-landscape-and-why-now) | Why Google can't build this. Perplexity, Brave, Apple — and the window |
| 7 | [Privacy as Product](#part-7-the-privacy-philosophy-as-a-product-principle) | The Amnesia Button. Trust as a commercial strategy |
| 8 | [The Long-Term Vision](#part-8-the-long-term-vision-and-the-open-agentic-economy) | The open agentic economy at full scale |

---

## Part 1: The Core Engine and the Autonomous Taste Graph

The foundation of the Sovereign Agent is the **Taste Graph**. If an AI agent is going to make decisions on your behalf, it must develop a highly accurate model of your preferences. The traditional method of building user profiles is fundamentally broken.

### The Flaw of Explicit Input

Historically, software has relied on static onboarding flows — questionnaires asking users to select their favorite genres, preferred aesthetics, dietary restrictions. This fails for two reasons.

First, humans are notoriously bad at articulating what they actually like. Explicit input is aspirational. A user might claim they prefer thought-provoking documentaries, but their actual viewing history reveals a preference for action movies.

Second, human taste is not static. It is contextual and constantly evolving. A profile built six months ago generates stale, irrelevant recommendations.

### Solving the Cold Start Problem

The solution is to launch the agent as a highly capable, **vertical-specific concierge** rather than a general search engine. The user provides a single detailed "seed prompt." The agent delivers value not because it knows the user perfectly yet, but because it performs the heavy lifting — scanning hundreds of galleries or reading dozens of hotel reviews — saving the user hours of manual work.

The value on day one is *computational leverage*. The value on day one hundred is *hyper-personalized intuition*.

### The Power of Implicit Signal

Once the user is engaged, the system deploys an **Autonomous Monitor Agent** to build the Taste Graph — relying entirely on implicit signals. With explicit sovereign consent, it silently observes what the user actually does.

- Browser telemetry: which articles they read, how long they linger on specific images
- API integrations: Spotify listening history, Amazon purchase history
- Feedback loop: if the system suggests three boutique hotels and the user books the second one, the Monitor Agent immediately analyzes why and updates its model

### The Native Graph Architecture

Human taste is not a spreadsheet. It is a web of interconnected concepts. If a user likes a specific mid-century modern chair, that preference links to a broader aesthetic, which influences their choice of restaurants or clothing.

The platform builds a **Headless Graph Engine** directly into the application:

1. **Local Storage Vault** — A local-first database (SQLite or RxDB) that lives entirely inside the app's sandbox on the user's device. The raw data never leaves the device.
2. **Graph Visualization** — An interactive visual representation of the user's mind, rendered using React Flow. The user can literally see how their tastes connect.
3. **Local Embeddings** — Lightweight, on-device embedding models generate mathematical vectors. When the user asks a question, a local vector search pulls the exact right context before sending a highly specific, anonymized prompt to the cloud.
4. **Sync Engine** — A local-first sync engine with end-to-end encryption. The Taste Graph syncs between devices via company servers, but because it is encrypted, the servers only see scrambled ciphertext.

### The Sovereign Enclave and the Amnesia Button

Because the native graph architecture is local-first, privacy is absolute. The **Amnesia Button** is the physical manifestation of this philosophy. The user opens the visual graph, selects any node, and deletes it. The agent instantly forgets it.

This is not just a privacy feature. It is a marketing asset.

---

## Part 2: The Multi-Agent Ecosystem

The platform is a coordinated ecosystem of three specialized agents.

**Agent A — The Monitor**
Runs locally on the user's device. Ingests data streams, calculates the decay of older preferences, and dynamically restructures the vector space when it detects massive contextual shifts in the user's life.

**Agent B — The Discoverer**
The user-facing agent. Operates in the cloud but relies heavily on local context from the Monitor Agent. Bypasses traditional search engines to find exact matches across open data registries, specialized databases, and direct APIs.

**Agent C — The Purchaser**
The backend financial agent. When the Discoverer hits a paywall or needs to negotiate for premium data, the Purchaser steps in. It holds a programmatic smart wallet and executes autonomous microtransactions in milliseconds.

---

## Part 3: The Two-Layer Payment Architecture

The most significant hurdle in disrupting the Attention Economy is the psychology of "Free." The platform solves this with a **Two-Layer Payment Architecture**.

### Layer 1: The User Experience

The user sees this layer only. It feels like a gift card or mobile game credits.

- New users receive **Discovery Credits** on signup — no financial commitment required
- Top up via Apple Pay or Stripe
- Transparent cost per task: *"Scanning 400 databases cost you 2.5 Credits"*
- Paying for actual computational work, not a flat subscription fee

### Layer 2: The Agentic Infrastructure

Operates entirely behind the scenes.

- Stripe fiat → USDC (via Coinbase Developer Platform or Circle)
- Fast blockchain (Solana) for speed and low fees
- Unique programmatic wallet per user agent
- The **x402 protocol**: when the Discoverer hits an HTTP 402 "Payment Required" response, the Purchaser autonomously signs a transaction and retrieves the data in milliseconds
- KYC burden stays centralized — the user never touches crypto

### The Business Model

**The spread:** The company controls the exchange rate between Discovery Credits and actual USDC costs. If the agent spends one cent in compute, the company deducts three cents of credits. The user is thrilled to pay three cents for a perfect recommendation.

**The float:** If 100,000 users each hold a $20 balance, the company sits on $2M of undeployed capital generating yield.

---

## Part 4: The Technical Build Roadmap

**Phase 1 — The Web2 Shell**
Next.js or React Native frontend, Supabase, Stripe. Build the credit ledger. Prove users pay fiat for credits when interacting with a standard LLM wrapper.

**Phase 2 — The Native Graph Engine**
Integrate SQLite into the app sandbox. Implement React Flow visualization. Deploy local embedding models (Transformers.js). Prove the Monitor Agent can silently build a Taste Graph that generates superior recommendations.

**Phase 3 — The Web3 Backend**
Coinbase Developer Platform or Circle Programmable Wallets on Solana. Create unique wallet addresses per user agent. Automate the Stripe → USDC treasury conversion.

**Phase 4 — The Discovery Layer**
Program agents to recognize HTTP 402 requests and execute x402 payments. Build fallback mechanisms using paid scraping APIs for sites that don't yet accept crypto micropayments.

---

## Part 5: The Strategic Moat and the Exit

The ultimate strategic moat is the Taste Graph itself.

After a year of continuous autonomous refinement, the agent knows the user's tastes so intimately that returning to a generic Google search will feel archaic and broken. This creates **negative churn** — the longer a user stays, the more painful it becomes to leave.

This makes the company an unprecedented acquisition target for Perplexity, DuckDuckGo, or Apple — not for immediate revenue, but for the proprietary Taste Graph architecture, the Web2-to-Web3 agentic payment bridge, and the absolute trust it has established with users.

---

## Part 6: The Competitive Landscape and Why Now

### The Incumbent Blind Spot

Google, Meta, and Amazon are each aggressively building AI features. But each is constrained by a structural problem: **their business model is built on advertising.**

An AI agent that works perfectly for the user is an existential threat to their core revenue. If Google's AI always found the most relevant result, users would never scroll past it to see the sponsored links. These companies are incentivized to build AI that is "good enough" to retain users — but not so good that it eliminates advertising.

**They are constitutionally incapable of building a truly sovereign agent.**

### The Infrastructure Convergence

Five years ago, building this required solving a dozen unsolved engineering problems simultaneously. Today:

- ✅ **MCP** (Anthropic) — standardized way for agents to connect to external tools
- ✅ **x402 protocol** (Coinbase) — standardized way for agents to pay for data over HTTP
- ✅ **Solana** — speed and fees necessary for micropayments at scale
- ✅ **On-device embedding models** — powerful enough to run on consumer hardware

The window of opportunity is open right now.

### The Emerging Threat Landscape

**Perplexity AI** — Most immediate threat, but still fundamentally a search engine. It answers queries; it doesn't build a persistent, evolving model of user preferences. No Taste Graph.

**Brave Browser** — Privacy-first user base, beginning to integrate AI. Could theoretically build a Taste Graph. But Brave's core competency is a browser, not an agentic discovery platform.

**Apple** — The most dangerous potential competitor. On-device AI, deep hardware integration, existing consumer trust around privacy. Key advantage of an independent platform: **openness**. Apple's ecosystem is closed. A sovereign agent can work across all platforms, all devices, all data sources.

---

## Part 7: The Privacy Philosophy as a Product Principle

The social contract between tech companies and users has been broken for 20 years. Users gave companies their attention. Companies harvested their behavioral data and sold it to advertisers at industrial scale. The contract was never made explicit.

The result is a deep, pervasive distrust of technology companies.

This platform inverts the contract completely. The user's data stays on their own device, processed by their own agent, stored in their own local graph database. The company never sees the raw content of the Taste Graph.

Trust is a scarce and valuable resource in the technology industry. A company that can credibly and verifiably claim zero access to personal preference data will attract a segment of the market that is currently completely underserved — not just privacy advocates, but the growing mainstream of consumers who are actively looking for an alternative to the surveillance economy.

---

## Part 8: The Long-Term Vision and the Open Agentic Economy

This platform begins as a consumer discovery product. Its long-term potential is the infrastructure for a fully functioning **open agentic economy**.

Every business, service provider, and creator registers their offerings in a machine-readable format. A restaurant publishes its menu, ambiance data, and availability to an open agent registry. A musician publishes their catalog with detailed metadata about mood, tempo, and influence. A bookseller publishes inventory with rich semantic tags.

The Discoverer Agent doesn't search Google. It queries the open registry directly, using the Taste Graph as its filter. It finds the exact match, negotiates the terms, and completes the transaction — without a single ad being served.

This is the Preference Economy at full scale. A distributed, open, and sovereign infrastructure where every user has an agent working exclusively in their interest, and every business competes purely on the quality of its offering rather than the size of its advertising budget.

---

## The Karpathy Principle

> *"In the LLM agent era, there's less need to share specific code or apps. Instead you share the idea — and the other person's agent customises and builds it for their specific needs."*

This document is that idea. Fork it. Build your version. The scarcity of building just hit zero.

**The scarcity of knowing what to build — and why it matters — has never been higher.**

---

## Author

This was written by **oddy_werk**

If you want to think through building this — or something like it — [reach out](https://neonmonk.se) or X handle @oddy_werk.

---

*This document is released without copyright restrictions. Take it. Build it. Make it better. buymeacoffee.com/oddy_werk*
