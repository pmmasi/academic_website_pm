# Pedro Masi — Academic Website Plan (Quarto)

> **Goal:** Build a Quarto-based personal academic website for the job market, modeled on
> [kadengrace.co](https://kadengrace.co/) and [Bingze Xu (UMD)](https://sites.google.com/umd.edu/bingzexu).
> `[PLACEHOLDER]` marks the few items still missing; everything else is drawn from the CV.

---

## Project Structure

```
website/
├── _quarto.yml            # site-wide config (navbar, theme, output-dir)
├── index.qmd              # Home / About
├── research.qmd           # Research (working papers, in progress)
├── teaching.qmd           # Teaching (instructor of record + TA)
├── cv.qmd                 # CV page (embedded PDF)
├── extracurricular.qmd    # Extracurricular / outreach
├── styles.css             # custom CSS overrides
├── Academic_CV_Pedro.pdf  # source CV (already in folder)
├── pedro_portrait/
│   └── HBO07380 edited.jpeg   ← primary headshot to use
└── stem_extracurricular/      # Centro Hispano outreach photos (6 images)
```

---

## `_quarto.yml` — Site Configuration

```yaml
project:
  type: website
  output-dir: docs          # GitHub Pages-friendly

website:
  title: "Pedro Masi"
  navbar:
    left:
      - href: index.qmd
        text: Home
      - href: research.qmd
        text: Research
      - href: teaching.qmd
        text: Teaching
      - href: cv.qmd
        text: CV
      - href: extracurricular.qmd
        text: Extracurricular

format:
  html:
    theme: [flatly, styles.css]
    toc: false
```

---

## Page 1 — `index.qmd` (Home / About)

### Layout

- Two-column layout: **left** = headshot, **right** = bio text + links
- Headshot: `pedro_portrait/HBO07380 edited.jpeg`

### Content

```markdown
::: {layout-ncol=2}
![](pedro_portrait/HBO07380 edited.jpeg){width=220px style="border-radius:8px;"}

## Pedro Masi

I am a PhD candidate in Business Analytics and Statistics at the
Haslam College of Business, University of Tennessee, Knoxville.
My research lies at the intersection of AI and causal inference.
I apply text mining and embedding techniques to measure technology
adoption and its impact on labor and financial outcomes, converting
unstructured patent and job-posting text into structured representations
that feed econometric models estimating the effects of AI exposure on
skill value and firm capital investments.

**Research Fields:**
- Machine Learning & Representation Learning
- Natural Language Processing (NLP)
- Causal Inference

**Education:**
- PhD, Business Analytics and Statistics — University of Tennessee, Knoxville (2023–Present)
- M.S., Finance and Technology — Vrije Universiteit Amsterdam (2020–2021)
- M.S., Agricultural Economics — Kansas State University (2017–2019)
- B.A., Agricultural Economics — Kansas State University (2011–2015)

**Advisor:** [PLACEHOLDER: Advisor name + link]

**Job Market:** I am on the 2026–2027 academic job market.

---

📧 pmmasig@gmail.com &nbsp;|&nbsp;
[UTK Profile](https://haslam.utk.edu/people/profile/pedro-masi/) &nbsp;|&nbsp;
[LinkedIn](PLACEHOLDER_LINKEDIN_URL) &nbsp;|&nbsp;
[CV (PDF)](cv.qmd)
:::
```

---

## Page 2 — `research.qmd` (Research)

### Working Papers

```markdown
### AI Upskilling: Decoupling Skill Demand and Skill Premium

*Pedro Masi, Yuanyang Liu, and Chuanren Liu*

**Status:** Under review — *Information Systems Research* (ISR)

[Abstract ▼] &nbsp; [PDF] &nbsp; [Slides]

---

### Herding Toward AI: How Following the Trend Affects Firm Investments

*Pedro Masi, Howard Zhong, Yuanyang Liu, and Chuanren Liu*

**Status:** In preparation — target *MIS Quarterly* (MISQ)

[Abstract ▼] &nbsp; [PDF] &nbsp; [Slides]

---

### Decoding AI Innovation: A Transformer-Based Approach to Patent Landscaping

*Pedro Masi, Yuanyang Liu, and Chuanren Liu*

**Status:** In preparation for submission

[Abstract ▼] &nbsp; [PDF]
```

> **Action needed:** Add 2–3 sentence abstracts for each paper once finalized.

### Conference Presentations

```markdown
- **"Herding Toward AI"** — Americas' Conference on Information Systems (AMCIS),
  Reno, NV, August 2026 *(accepted, forthcoming)*
- **"AI and the Market Value of Skills"** — DePaul Doctoral/Junior Faculty Research
  Symposium, Chicago, IL, March 2026
- **"AI Upskills Human-Centric and Fundamental Computer Science Knowledge"**
  - Workshop on Information Technologies & Systems (WITS), Nashville, TN, Dec 2025
  - Conference of Information Systems & Technology (CIST), Atlanta, GA, Oct 2025
- **"Tracking the New Frontiers of Work in Tennessee"** — AI Tennessee Workshop,
  Knoxville, TN, Jan 2025
- **"AI Talk: Can Executives Keep Their Promises?"** — INFORMS Annual Conference,
  Seattle, WA, Oct 2024
- **"AI for Business Innovation"** — Business Analytics Forum, UTK, Aug 2024
```

### Grants

```markdown
**AI Tennessee Initiative Seed Grant** — Collaborator.
Research on Artificial Intelligence and the Future of Work; supervised master's
students and contributed to research design and dashboard-based data visualization.
```

---

## Page 3 — `teaching.qmd` (Teaching)

### Instructor of Record

```markdown
| Course    | Title                        | Semester  | Syllabus |
|-----------|------------------------------|-----------|----------|
| STAT 201  | Introduction to Statistics   | Fall 2025 | [Syllabus PDF](PLACEHOLDER_syllabus_stat201.pdf) |
```

> **Action needed:** Attach the STAT 201 Fall 2025 syllabus PDF.

### Guest Lectures

```markdown
- "Clustering Techniques" — Data Mining (BZAN 542), UTK, Sept 2025
- "Probability Theory" — Introductory Statistics (STAT 201), UTK, Mar 2025
```

### Teaching Assistant

```markdown
| Course    | Title                          | Instructor           | Semester    |
|-----------|--------------------------------|----------------------|-------------|
| STAT 505  | Quantitative Methods MBA       | Prof. Allen Pannell  | Spring 2026 |
| BZAN 557  | Text Mining                    | Prof. Wenjun Zhou    | Spring 2026 |
| STAT 201  | Introduction to Statistics     | Prof. Adam Spanbauer | Summer 2025 |
| BUAD 503  | Business Communications MBA    | Prof. Angel Norman   | Summer 2024 |
| BZAN 555  | Supply Chain Analytics         | Prof. Sean Willems   | Spring 2024 |
| BZAN 542  | Data Mining Methods            | Prof. ChuanRen Liu   | Fall 2023   |
```

> **Action needed:** Add syllabi for TA courses if desired.

### Teaching Statement *(optional)*

```markdown
[PLACEHOLDER: 1–2 paragraph teaching philosophy. Link to Teaching Statement PDF if available.]
```

---

## Page 4 — `cv.qmd` (Curriculum Vitae)

```markdown
## Curriculum Vitae

[Download PDF](Academic_CV_Pedro.pdf){.btn .btn-primary}

<iframe src="Academic_CV_Pedro.pdf" width="100%" height="900px"></iframe>
```

> CV PDF is already in the project folder as `Academic_CV_Pedro.pdf`.

---

## Page 5 — `extracurricular.qmd` (Extracurricular)

### STEM Outreach — Centro Hispano

```markdown
### Robotics Education for Kids — Centro Hispano

*Volunteer, Spring 2023*

Assisted in teaching basic robotics concepts to elementary school students,
including programming and building simple robots, while fostering enthusiasm
for STEM subjects through interactive and engaging activities.

::: {layout-ncol=3}
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM.jpeg)
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM (1).jpeg)
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM (2).jpeg)
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM (3).jpeg)
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM (4).jpeg)
![](stem_extracurricular/WhatsApp Image 2026-05-10 at 9.17.39 AM (5).jpeg)
:::
```

### Other Interests *(optional)*

```markdown
### [PLACEHOLDER: Interest / Hobby]

[PLACEHOLDER: Short paragraph.]
```

---

## Assets Checklist

| Asset | Status | Notes |
|-------|--------|-------|
| Headshot | ✅ Ready | `pedro_portrait/HBO07380 edited.jpeg` |
| Outreach photos (6) | ✅ Ready | `stem_extracurricular/` |
| CV PDF | ✅ Ready | `Academic_CV_Pedro.pdf` |
| Syllabus — STAT 201 (Instructor) | ⬜ Needed | PDF for Fall 2025 |
| Syllabi — TA courses | ⬜ Optional | Per planning notes |
| Paper abstracts | ⬜ Needed | 2–3 sentences per working paper |
| Paper PDFs / preprints | ⬜ Needed | One per working paper |
| Chuanren Liu name + link | ⬜ https://www.linkedin.com/in/chuanren/ | For index.qmd |
| LinkedIn URL | ⬜ https://www.linkedin.com/in/pedro-masi/ | For index.qmd |

---

## Build & Publish

```bash
# Preview locally
quarto preview

# Render to docs/
quarto render

# Deploy to GitHub Pages
# 1. Push docs/ to GitHub
# 2. Set Pages source to /docs on main branch
```

---

## Content Filling Order (recommended)

1. Add advisor name + LinkedIn URL in `index.qmd`
2. Add abstracts to the three working papers in `research.qmd`
3. Attach STAT 201 syllabus PDF and link it in `teaching.qmd`
4. Render and preview; fix layout issues
5. Deploy
