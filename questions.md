# CPE — Questions & Options (v2)

Source: `index.html`. Two parallel flows after Screen 1.

---

## Screen 0 — Landing / Background Selector

**Free Profile Evaluation** — Tech Career Assessment in 2 mins

**Q. What's your current background?**
- Non-Tech / Career Switcher
- Tech Professional

---

# 🟦 TECH PROFESSIONAL FLOW

## Screen 1 — Your Profile *(3 questions)*

> Hey, let's start with the basics — where you are in your tech journey today.

**Q1. What best describes your current role?**
- Software Engineer · Product Company
- Software Engineer · Service Company
- Software Engineer · Startup
- Software Engineer · FAANG / Big Tech
- DevOps / Cloud / Infra Engineer
- QA / Support / Other Tech Role

**Q2. How many years have you been in tech?**
- 0–2 years · 2–3 years · 3–5 years · 5–8 years · 8+ years

**Q3. Where do you focus most of your work?**
- Backend & APIs
- Frontend & UI
- Full-stack
- System design & architecture

---

## Screen 2 — Skills & Prep *(7 inputs · 2 multi-selects + prep snapshot)*

> Now the real stuff — what you actually know, and where your prep stands. This drives the gap analysis in your report.

**Q4. Pick the skills you actually use today** *(multi-select chips)*
- Python · Java · Go · JavaScript · TypeScript
- SQL · PostgreSQL · MongoDB
- Django/Flask · Spring Boot · Node.js/Express · React
- AWS/GCP/Azure · Docker · Kubernetes
- Kafka/RabbitMQ · Redis
- System Design · Observability

**Q5. Which AI tools do you actually use?** *(multi-select chips)*
- GitHub Copilot · Cursor · ChatGPT · Claude · Gemini
- v0/Bolt · Datadog AI · Notion AI · CodeRabbit
- None yet

**Q6. Your prep snapshot — quick taps** *(5 single-selects on one screen)*

| Dimension | Options |
|---|---|
| DSA / LeetCode practice | 0–10 · 10–50 · 50–100 · 100–200 · 200+ |
| System design comfort | Never tried · Read about it · Can explain · Can design · Lead designs |
| Real projects shipped | 0 · 1 toy · 1–2 real · 3–4 · 5+ |
| Mock interviews done | 0 · 1–2 · 3–5 · 5–10 · 10+ |
| Public GitHub repos | 0 · 1–3 · 3–5 · 5–10 · 10+ |

---

## Screen 3 — Your Goals *(3 questions)*

> Last bit. Tell me where you want to go — and what's pushing you to act now.

**Q7. What's your dream role?**
- Senior Backend Engineer
- Senior Full-Stack Engineer
- Senior Frontend Engineer
- Data Science / ML Engineer
- AI / ML Engineer
- DevOps / Cloud Engineer
- Tech Lead / Staff Engineer
- Not sure yet

**Q8. What kind of company are you targeting?**
- FAANG / Big Tech
- Product Unicorns
- High-Growth Startups
- Better Service Company

**Q9. Why are you doing this now?** *(multi-select chips)*
- Worried about layoffs
- Stuck in current role
- Want a bigger salary
- Switching domains
- Worried about AI
- Just exploring

---

# 🟨 NON-TECH / CAREER SWITCHER FLOW

## Screen 1 — Background *(3 questions)*

> Welcome! Let's start with where you are today, so I can build a roadmap that fits your background.

**Q1. What's your current professional background?**
- Sales / Marketing / Business
- Operations / Consulting / PM
- Design (UI/UX, Graphic, Product)
- Finance / Accounting / Banking
- Other Non-Tech / Fresh Grad

**Q2. How many years of work experience do you have?**
- 0 (Fresh grad) · 0–2 · 2–3 · 3–5 · 5+

**Q3. What have you tried so far?** *(multi-select chips)*
- Online courses · YouTube tutorials · Read blogs/books
- Built a small project · Bootcamp/workshop · Wrote some code
- Just exploring · Nothing yet

---

## Screen 2 — Readiness *(3 questions)*

> Now let's get a sense of where your prep stands today — even if it's zero.

**Q4. How comfortable are you with coding right now?**
- Confident — solve simple problems independently
- Learning — follow tutorials, struggle alone
- Beginner — understand concepts, can't code yet
- Complete beginner — haven't tried yet

**Q5. How much time can you dedicate each week?**
- 10+ hrs · 6–10 hrs · 3–5 hrs · 0–2 hrs

**Q6. Which AI tools do you actually use?** *(multi-select chips)*
- ChatGPT · Claude · Gemini · GitHub Copilot · Cursor
- v0/Bolt · Notion AI · None yet

---

## Screen 3 — Goals *(3 questions)*

> Last bit. Tell me where you want to go — and what's pushing you to act now.

**Q7. Which tech role excites you the most?**
- Backend Engineer · Frontend Engineer · Full-Stack Engineer
- Data Science / ML Engineer · AI / ML Engineer · DevOps / Cloud Engineer
- Not sure yet

**Q8. What type of company would you love to work for?**
- Any tech company (experience first)
- Product companies
- Service companies
- FAANG / Big Tech (long-term)

**Q9. Why are you doing this now?** *(multi-select chips)*
- Worried about my current career
- Want a bigger salary
- Want flexibility / remote work
- Job stability in tech
- Worried about AI replacing my job
- Just exploring

---

## Notes

- Both flows: 3 screens · ~9 inputs each · ~3-4 minutes total
- **No lead capture** — handled by the Scaler page after the report CTA
- **Multi-selects (chips):** skills, AI tools, "what you've tried", "why now"
- **Prep snapshot grid:** 5 single-selects compressed onto one screen (Tech Step 2)
- Both flows converge to `report.html`

## What feeds the report

| Report element | Source question |
|---|---|
| LinkedIn skill chips (have) | Tech Q4 / Non-tech Q3 |
| LinkedIn skill chips (missing) | Derived from Q4 vs target role expectations |
| AI replaceable skills | Derived from Q4 ∩ AI-vulnerable list |
| You vs Industry · DSA practice | Tech Q6 row 1 |
| You vs Industry · System design | Tech Q6 row 2 |
| You vs Industry · Real projects | Tech Q6 row 3 |
| You vs Industry · Mock interviews | Tech Q6 row 4 |
| You vs Industry · Public visibility | Tech Q6 row 5 (GitHub) |
| You vs Industry · AI tools | Tech Q5 / Non-tech Q6 |
| Market view · target role | Q7 / Q8 |
| Mentor message tone | Q9 (why now) |
| Program mapping | Q7 (target role) |
