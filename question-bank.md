# CPE Question Bank — v1

The dynamic question bank for the **Skills & Prep** step of the questionnaire. The shape is the same across every role × tier:

- **Q1 — Brain tickler · Craft fluency** *(role-specific, "quick check" mini-question)*
- **Q2 — Brain tickler · AI judgment** *(role-specific, "what would you do" mini-question)*
- **Q3 — Self-rating · System / Architecture** *(role-specific scale)*
- **Q4 — Self-rating · Real-world output** *(role-specific scale)*

4 questions per cell. ~60–75 seconds to complete. **2 thinking moments + 2 self-portraits.**

---

## Role × Tier mapping

| User picks (Q1 of Step 1) | Track ID | Notes |
|---|---|---|
| Software Engineer · Service Company | `software_easy` | Easier calibration |
| Software Engineer · Product Company | `software_medium` | Standard calibration |
| Data Scientist / ML Engineer | `dsml` | DSML track |
| AI / ML Engineer · LLMs / RAG / Agents | `aiml` | AIML track |
| DevOps / Cloud / Infra Engineer | `devops` | DevOps/SRE track |
| QA / Support / Other Tech Role | `software_easy` | Defaults to easier SE bank |
| (Non-Tech / Career Switcher branch) | `non_tech` | Lighter, no DSA |

| Years bucket (Q2 of Step 1) | Tier loaded |
|---|---|
| `0–2 years` (or fresh grad for non-tech) | `tier1` — Building blocks |
| `2–3 years`, `3–5 years` | `tier2` — Pattern recognition + tradeoffs |
| `5–8 years`, `8+ years` (or `5+` for non-tech) | `tier3` — Judgment + ownership |

**Tone:** Easy → light-medium across the board. Even Tier 3 should never feel like a FAANG interview question. The vibe is *"a thoughtful question your friend would ask you over coffee."*

---

## TRACK · `software_easy` (Service Company SE — calibrated easier)

### Tier 1 — 0–2 years

**Q1 · Quick check — Craft**
> You have a list of 100 numbers. You need the largest one. What's the simplest way?
- Sort the list, take the last item
- Loop once, track the biggest as you go
- Add them all up, divide by count
- I'd Google it

**Q2 · Quick check — AI**
> You ask ChatGPT to write a function. It gives you code. What do you do first?
- Copy-paste it and run
- Read it line by line first
- Ask ChatGPT to explain what it wrote
- I haven't really used ChatGPT for code yet

**Q3 · Self-rating — System / Architecture**
> Have you ever built or worked on a multi-file project?
- Yes — I've built a small app with multiple files and a database
- Yes — I've worked inside a small codebase as part of a team
- I've followed a tutorial that touched multiple files
- I've only written single-file scripts so far
- Not yet

**Q4 · Self-rating — Real-world output**
> What's the most you've shipped that's actually running somewhere?
- A working app or tool with real users (even a few)
- A side-project that runs on my laptop end-to-end
- College / bootcamp project, fully working
- Tutorial follow-alongs only
- Not yet

---

### Tier 2 — 2–3 / 3–5 years

**Q1 · Quick check — Craft**
> You need to find if a username exists in a list of 1 million users. Which is fastest?
- Loop through the list and check each one
- Sort the list first, then binary search
- Put the usernames in a set / hashmap, then check
- I'd let the database handle it

**Q2 · Quick check — AI**
> Copilot autocompletes a function for you. It looks right. Before you commit it, what do you do?
- Run the existing tests
- Read every line and trace the logic
- Ship it if the tests pass
- I don't use Copilot regularly yet

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with how a typical web app is wired together?
- I can explain how a request flows from frontend → API → DB and back
- I know the pieces but get confused about where things break
- I can build features inside a codebase but the big picture is fuzzy
- I follow tickets and write code for what I'm told
- I haven't worked on a real web app yet

**Q4 · Self-rating — Real-world output**
> What's the most complex thing you've shipped to production?
- A multi-feature module used by real customers
- A standalone feature inside a larger product
- A small fix or improvement that went live
- Internal tools or PoCs only
- Nothing in production yet

---

### Tier 3 — 5–8 / 8+ years

**Q1 · Quick check — Craft**
> A page on your app suddenly takes 5 seconds to load. The DB is fine. Where do you look first?
- Network tab — check API call sizes and timings
- Frontend bundle / render performance
- Server logs for slow endpoints
- All of the above, in parallel

**Q2 · Quick check — AI**
> Your team is debating whether to let Copilot write tests for a critical billing flow. Your take?
- Yes — but every test must be reviewed and the suite must catch real bugs
- Yes — Copilot tests are fine, faster than writing them ourselves
- No — testing critical flows is too risky to automate
- I'd defer to whoever owns the billing module

**Q3 · Self-rating — System / Architecture**
> You're asked to design a small new module for your team's product. How do you approach it?
- Sketch the data model + API + integration points, talk it through with the team
- Build a quick prototype and iterate
- Ask a senior to walk me through how they'd do it
- I'd start coding and figure it out as I go
- I haven't been asked to design something on my own

**Q4 · Self-rating — Real-world output**
> What's the most senior thing you've owned end-to-end?
- A full feature or service that I designed, built, and still maintain
- A feature I built but a senior reviewed the design
- Pieces of features inside someone else's design
- Bug fixes and small improvements
- Mostly support / maintenance work

---

## TRACK · `software_medium` (Product Company SE — standard calibration)

### Tier 1 — 0–2 years

**Q1 · Quick check — Craft**
> You have a list of users and need to look up one by ID, repeatedly. What's the fastest way?
- Loop through the list each time
- Sort the list and binary search
- Use a hashmap / dictionary keyed by ID
- I'd ask the senior dev

**Q2 · Quick check — AI**
> You ask Cursor to write a function that handles user input. It generates the code. What do you do first?
- Run the tests
- Read every line, especially the validation part
- Ship it if it compiles cleanly
- I'd write it myself, I don't trust AI yet

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with how a typical product company codebase is structured?
- I can navigate a multi-service codebase and find what I need
- I know my team's part well, the rest is a black box
- I can read code but get lost in big repos
- I've mostly worked on small scripts and college projects
- I haven't worked in a real codebase yet

**Q4 · Self-rating — Real-world output**
> What's the most you've shipped that real users used?
- A feature or two in production at my current company
- An internship project that went live
- A side-project with a few real users
- College / bootcamp projects only
- Nothing in production yet

---

### Tier 2 — 2–3 / 3–5 years

**Q1 · Quick check — Craft**
> Your service does 10K reads/sec on a single Postgres table. Latency is climbing. First thing you'd try?
- Add an index on the most-queried column
- Add a read replica
- Cache hot rows in Redis
- Profile the slow queries first

**Q2 · Quick check — AI**
> Copilot generates a function that handles user payments. It looks correct. What do you do first?
- Run the tests
- Read every line, especially the auth and money paths
- Ship it if the tests pass
- I wouldn't trust Copilot for payment code

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with system design fundamentals?
- I've designed services with caching, queues, scaling decisions and defended them in reviews
- I can sketch the basic shape — DBs, APIs, where data flows
- I understand the pieces but couldn't put one together end-to-end
- I've heard the terms but never tried it myself
- This area is new to me

**Q4 · Self-rating — Real-world output**
> What's the most you've shipped that real users actually used?
- Multi-service features in production used by thousands
- A solo project shipped end-to-end with auth, DB, deploys
- A feature inside someone else's product I'm proud of
- Internal tools only
- Nothing in production yet

---

### Tier 3 — 5–8 / 8+ years

**Q1 · Quick check — Craft**
> Your team's API latency P99 doubled overnight. Nothing changed in your code. First place to look?
- Recent deploys across all upstream services
- Database — slow query log, connection pool
- Infra — CPU, memory, network on the hosts
- All of the above, in parallel

**Q2 · Quick check — AI**
> Your team's PR review backlog is killing release velocity. How would you wire AI in to fix it?
- Add CodeRabbit / Copilot review on every PR + lightweight human sign-off for critical paths
- Use Copilot to write better PR descriptions so humans review faster
- Use AI to triage which PRs need senior review vs auto-approve
- I'm not convinced AI is reliable enough to review code yet

**Q3 · Self-rating — System / Architecture**
> When you're asked to design a new service, how do you approach it?
- I lead the design doc, defend tradeoffs in review, and own the integration points
- I write the design and get a senior to sanity-check it
- I follow our team's templates and patterns
- I usually pair with someone more senior on design
- I haven't owned a design end-to-end yet

**Q4 · Self-rating — Real-world output**
> What's the most senior thing you currently own?
- A whole service or platform that I designed and still maintain
- A major feature I built end-to-end
- Pieces of larger systems
- Bug fixes and small features
- Mostly support / maintenance

---

## TRACK · `dsml` (Data Scientist / ML Engineer)

### Tier 1 — 0–2 years

**Q1 · Quick check — Craft**
> You build a model. Training accuracy is 95%, test accuracy is 60%. What's most likely?
- The model is too simple
- The model is overfitting to the training data
- The training data is too small
- The test data is wrong

**Q2 · Quick check — AI**
> ChatGPT writes you a SQL query that joins three tables and returns "the right number." What do you do first?
- Run it on the full dataset
- Run it on a sample, sanity-check the joins and counts
- Trust it if the number looks reasonable
- I'd write the query myself, I don't trust AI on data

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with the steps in a typical data pipeline (extract → clean → analyse → model)?
- I've built one end-to-end on real data
- I've done parts of it (mostly cleaning + analysis)
- I've followed tutorials but never built one solo
- I understand the steps but haven't done them yet
- Not yet

**Q4 · Self-rating — Real-world output**
> What's the most you've actually built with data?
- A real model trained on real data, used by someone
- A clean analysis report that drove a decision at work / college
- Notebooks for class / Kaggle competitions
- I've followed tutorials and reproduced examples
- Nothing yet

---

### Tier 2 — 2–3 / 3–5 years

**Q1 · Quick check — Craft**
> You're building a churn model. Your features are mostly fine, but there's massive class imbalance (98% non-churn). First fix?
- Train on it as-is, the model will figure it out
- Resample the data (oversample churners or undersample non-churners)
- Switch to a different metric (precision / recall instead of accuracy)
- All of the above — and probably try a different model

**Q2 · Quick check — AI**
> ChatGPT writes you a feature engineering pipeline that "should work." Before you train on its output, what do you do?
- Train on it, see if accuracy is good
- Eyeball the output rows — distributions, nulls, sanity ranges
- Ask ChatGPT to explain each transformation
- I'd write the pipeline myself, AI doesn't know my data

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with the lifecycle of a real ML project (data → train → serve → monitor)?
- I've owned at least one model from data through to monitoring in production
- I've trained models end-to-end but never had to serve / monitor them live
- I've done the data + training side, never deployment
- I mostly do ad-hoc analysis and reports
- Not yet

**Q4 · Self-rating — Real-world output**
> What's the most impactful thing you've shipped with data or ML?
- A model in production that real users / systems depend on
- A model deployed for an internal team
- A polished analysis that changed a business decision
- Solid notebooks and Kaggle results
- Mostly tutorials and class projects

---

### Tier 3 — 5–8 / 8+ years

**Q1 · Quick check — Craft**
> Your model has been live for 3 months. Accuracy is dropping. What's most likely?
- The model is "wearing out" — needs retraining
- The data distribution has shifted (data drift)
- A bug in the inference pipeline
- All of the above — would investigate in that order

**Q2 · Quick check — AI**
> Your team is debating: "Should we use an LLM to label our training data instead of paying annotators?" What do you say?
- Yes — but only with human spot-checks and a clear quality threshold
- Yes — LLMs are accurate enough now, much faster
- No — LLM labels introduce systematic bias
- I'd defer to whoever owns the labelling pipeline

**Q3 · Self-rating — System / Architecture**
> When your team builds a new ML system, how involved are you in the design?
- I lead the design — data, model, serving, monitoring, ownership
- I own the modelling part, work closely with platform / infra
- I handle modelling, others handle serving and infra
- I do analysis / experiments more than systems
- I'm still getting into the systems side

**Q4 · Self-rating — Real-world output**
> What's the biggest model or system you currently own?
- A production ML system I designed, monitor, and retrain
- A model I built that someone else now serves
- Pieces of a larger ML platform
- Strong analysis work, less production
- Mostly research / experiments

---

## TRACK · `aiml` (AI / ML Engineer · LLMs / RAG / Agents)

### Tier 1 — 0–2 years

**Q1 · Quick check — Craft**
> You ask GPT a question and it confidently gives you a wrong answer. What's that called?
- Overfitting
- Hallucination
- Bias
- Drift

**Q2 · Quick check — AI**
> You're using ChatGPT to debug your own code. What's the *best* way to use it?
- Paste the error, copy back the fix
- Paste the error AND the relevant code, then read what it suggests carefully
- Describe the problem in plain English, let ChatGPT guess
- I rarely use it, I'd rather Stack Overflow

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with the basic shape of an LLM-powered app?
- I've built one — prompt → LLM → parse output → show user
- I've followed a tutorial end-to-end but never built one solo
- I understand the pieces but haven't wired one together
- I've used the OpenAI / Claude API once or twice
- I haven't built anything with LLMs yet

**Q4 · Self-rating — Real-world output**
> What's the most you've actually built with AI?
- A small AI product or tool that real people have used
- A side-project (chatbot, summariser, etc.) that works end-to-end
- I've followed tutorials and modified them
- I've used ChatGPT a lot but never built anything
- Nothing yet

---

### Tier 2 — 2–3 / 3–5 years

**Q1 · Quick check — Craft**
> Your RAG chatbot answers confidently but the answers are wrong. First place to look?
- The LLM model — try a bigger one
- The retrieval step — are the right documents even being fetched?
- The prompt — rewrite the system prompt
- The vector DB — switch providers

**Q2 · Quick check — AI**
> Your team wants to ship an LLM agent that can take actions in your product (delete records, send emails). What's your move?
- Build it with strict per-action confirmation prompts and audit logs
- Build it with a guardrail LLM that reviews each action first
- Build it but only allow read-only actions in v1
- Don't build it — too risky for users right now

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with building production LLM systems?
- I've built and shipped a RAG / agent system that real users rely on
- I've built end-to-end prototypes that worked but never went live
- I've built parts (retrieval, prompting, evals) but never the full thing
- I've used LangChain / LlamaIndex tutorials
- I'm still in the experimentation phase

**Q4 · Self-rating — Real-world output**
> What's the most impactful AI thing you've shipped?
- A production AI feature inside a real product, used daily
- An internal AI tool used by my team
- A polished side-project (chatbot, agent, RAG demo)
- Tutorials and prototypes
- Nothing in production yet

---

### Tier 3 — 5–8 / 8+ years

**Q1 · Quick check — Craft**
> Your production LLM system was working. Now answers are slower and lower quality. Nothing changed in your code. First check?
- The provider's API status — they may have changed the model
- Your retrieval index — has anything been re-indexed?
- Your prompt — did anyone touch the system prompt?
- All of the above, in that order

**Q2 · Quick check — AI**
> Your team is debating: build your own LLM eval pipeline, or trust a third-party (LangSmith, Braintrust)? What do you say?
- Build a thin custom eval suite tailored to *our* failure modes — third-party for general regressions
- Use the third-party — eval is hard, don't reinvent
- Build everything in-house — vendor lock-in is risky
- I'd run a quick comparison with both before deciding

**Q3 · Self-rating — System / Architecture**
> When your team designs a new LLM-powered system, how involved are you?
- I lead the design — model choice, retrieval strategy, eval, monitoring, cost
- I own the LLM and retrieval parts, others handle infra
- I do prompting and prototypes, others productionise it
- I mostly do experimentation and research
- I'm still learning the systems side

**Q4 · Self-rating — Real-world output**
> What's the biggest AI system you currently own?
- A production LLM/agent system I designed, evaluate, and improve continuously
- A live AI feature I built and others now maintain
- Pieces of a larger AI platform
- Strong prototypes, less in production
- Mostly experiments and demos

---

## TRACK · `devops` (DevOps / SRE / Cloud / Infra)

### Tier 1 — 0–2 years

**Q1 · Quick check — Craft**
> Your service is returning 503 errors. Where do you look first?
- The application logs
- CPU / memory metrics on the host
- Recent deployments
- All of the above, in parallel

**Q2 · Quick check — AI**
> You ask ChatGPT for a Bash one-liner to clean up old log files. It gives you one. What do you do first?
- Run it in production
- Run it on a test directory first
- Read every flag and understand what each part does
- I'd write it myself, I don't trust AI for shell commands

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with the basic shape of cloud infrastructure (compute, storage, network, IAM)?
- I can spin up and connect these pieces on AWS / GCP without help
- I can do it with documentation but need to look things up
- I've followed tutorials but never built it solo
- I know the terms but haven't wired things up yet
- Not yet

**Q4 · Self-rating — Real-world output**
> What's the most you've actually deployed or run?
- A real service in production with monitoring and alerts
- A side-project deployed to a cloud provider
- A working environment for a college / personal project
- Tutorial walkthroughs only
- Nothing yet

---

### Tier 2 — 2–3 / 3–5 years

**Q1 · Quick check — Craft**
> A pod in your Kubernetes cluster is stuck in `CrashLoopBackOff`. First thing you'd run?
- `kubectl logs <pod>` — check the application output
- `kubectl describe pod <pod>` — check events and status
- Restart the pod and see if it self-heals
- Check the deploy history first

**Q2 · Quick check — AI**
> Claude writes you a Terraform module that "looks fine." You're about to apply it to prod. What do you do first?
- `terraform plan` and read every resource diff carefully
- Apply it to staging first, then prod
- Trust it if Claude was confident
- I'd rewrite it from scratch — AI can't be trusted with infra

**Q3 · Self-rating — System / Architecture**
> How comfortable are you with designing the infrastructure for a new service?
- I can size the cluster, set up CI/CD, monitoring, and alerts on my own
- I can do parts of it but lean on senior folks for the architecture
- I follow our team's templates and patterns
- I mostly handle on-call and small infra changes
- I haven't owned new infra yet

**Q4 · Self-rating — Real-world output**
> What's the most you currently own in infra?
- Multiple services + the CI/CD + monitoring stack around them
- One service end-to-end (deploy, monitor, on-call)
- Pieces of a larger platform someone else owns
- Tickets and small infra work
- Mostly support / on-call

---

### Tier 3 — 5–8 / 8+ years

**Q1 · Quick check — Craft**
> Your team's deploys have started failing intermittently — about 1 in 10. First place you'd look?
- The CI/CD pipeline logs across the failed runs
- The cloud provider's status page
- Recent changes to the deploy scripts or infra
- All of the above, with the failed-run logs first

**Q2 · Quick check — AI**
> Your team is debating: "Should we let an AI agent run our incident response runbooks (restart services, scale up, etc.)?" Your take?
- Yes — but only for read-only diagnosis steps; humans approve actions
- Yes — full agent autonomy for known incidents, page humans on anything new
- No — an agent making infra changes is too risky
- I'd run a small pilot on staging first

**Q3 · Self-rating — System / Architecture**
> When your team is designing a new platform or major infra change, how involved are you?
- I lead the design — capacity, networking, security, observability, cost
- I own significant chunks of the design
- I contribute but follow someone else's lead
- I implement what's been designed
- I'm still building toward design ownership

**Q4 · Self-rating — Real-world output**
> What's the biggest thing you currently own in your infra?
- A whole platform / cluster I designed and now operate
- Major systems I designed alongside a senior
- Pieces of a larger platform someone else owns
- Smaller services + on-call
- Mostly on-call and ticket work

---

## TRACK · `non_tech` (Career Switcher)

Different shape — no DSA / system-design content. **1 daily-life AI brain tickler + 3 self-ratings.**

### Tier 1 — Fresh grad / 0–2 years

**Q1 · Quick check — Daily AI**
> You need to write a tough email at work. How do you handle it?
- I draft it myself, then ask ChatGPT/Claude to polish it
- I let ChatGPT write the whole thing, then send
- I write it from scratch, no AI
- I'd avoid the email or ask a colleague for help

**Q2 · Self-rating — Coding comfort**
> How much have you actually played with code?
- I've followed a beginner course and written some Python / JavaScript
- I've watched videos and tried a few examples
- I've heard the words but never typed code
- I've avoided code so far
- Not interested in code, more in tools / no-code

**Q3 · Self-rating — What you've built**
> Have you actually built or made anything yet?
- A small website / app / tool I'm proud of
- A working tutorial I followed end-to-end
- I've experimented but nothing finished
- I've watched but not tried
- Nothing yet

**Q4 · Self-rating — Time you can commit**
> Realistically, how many hours/week can you put into this?
- 10+ hours / week
- 6–10 hours / week
- 3–5 hours / week
- 0–2 hours / week

---

### Tier 2 — 2–3 / 3–5 years (mid-career switch)

**Q1 · Quick check — Daily AI**
> Your manager asks for a one-page summary of a 30-page report by tomorrow morning. How do you handle it?
- Drop the report into Claude / ChatGPT, edit the summary, send
- Read the report myself, then ask AI to polish my summary
- Read it cover to cover and write it yourself
- I'd ask for an extension

**Q2 · Self-rating — Coding comfort**
> How comfortable are you with code today?
- I can read simple code and modify small things
- I've followed tutorials and built small things
- I've tried code a few times but it didn't stick
- I know what code is but haven't really tried
- I want to start from zero

**Q3 · Self-rating — What you've built**
> What's the most technical thing you've actually built?
- A working tool / app, even a basic one
- A no-code / low-code project that works
- A polished tutorial follow-along
- I've explored but not built
- Nothing yet

**Q4 · Self-rating — Time you can commit**
> How much time can you actually carve out per week alongside your job?
- 10+ hours / week
- 6–10 hours / week
- 3–5 hours / week
- 0–2 hours / week

---

### Tier 3 — 5+ years (senior career switch)

**Q1 · Quick check — Daily AI**
> Your team has too much manual reporting work. You suspect AI could help. What's your move?
- Pilot Claude / ChatGPT on one workflow first, measure time saved, then expand
- Tell the team to start using ChatGPT for everything
- Wait for IT / ops to formally approve a tool
- I'd avoid pushing it — let leadership decide

**Q2 · Self-rating — Coding comfort**
> Where do you stand on technical skills today?
- I've used SQL / Python / Excel macros in my current role
- I've worked closely with tech / engineering teams but don't write code
- I'm purely on the business side, no real tech exposure
- I've tried to learn before but didn't stick with it
- I'm starting from scratch

**Q3 · Self-rating — What you've built**
> What's your most technical accomplishment so far?
- I've built or owned a workflow / tool / dashboard at work
- I've driven a project that involved engineering teams closely
- I've used existing tools well but never built anything
- I've explored tech learning but never finished anything
- Nothing yet

**Q4 · Self-rating — Time you can commit**
> Realistically, how much time can you carve out per week alongside your job?
- 10+ hours / week
- 6–10 hours / week
- 3–5 hours / week
- 0–2 hours / week

---

## Summary

| Track | Tier 1 (0–2 yrs) | Tier 2 (2–5 yrs) | Tier 3 (5+ yrs) |
|---|---|---|---|
| `software_easy` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |
| `software_medium` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |
| `dsml` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |
| `aiml` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |
| `devops` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |
| `non_tech` | ✓ 4 Qs | ✓ 4 Qs | ✓ 4 Qs |

**Total: 18 cells × 4 questions = 72 questions.**

Every cell follows the same shape:
- Q1 — brain tickler, craft fluency
- Q2 — brain tickler, AI judgment
- Q3 — self-rating, system / architecture (or "what you've built" for non-tech)
- Q4 — self-rating, real-world output (or "time commitment" for non-tech)

**Next step:** wire this into the quiz so the user picks role + experience and the right 4 questions render dynamically.
