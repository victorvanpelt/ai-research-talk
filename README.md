# Using AI Responsibly for Research

Slides for "Using AI Responsibly for Research", a faculty spark talk at WHU - Otto Beisheim School of Management. The talk asks where we should use AI in research, on a scale from no AI use to the full delegation of all research. Research must be reproducible, whereas AI agents are probabilistic (i.e., the same task can return different results) and can report the same steps differently. Thus, I argue for a skill-first setup, in which a written workflow sets the steps for us and for our AI agents. The talk shows my current skill template, a paper audit skill as an example, and a reproducible folder structure with the rules that every AI agent must follow.

The deck is one [Quarto](https://quarto.org) file, `spark_talk_ai_research_slides.qmd`, which renders to `spark_talk_ai_research_slides.pdf` on the WHU beamer template. Two slides show a companion repository, the [research pipeline example](https://github.com/victorvanpelt/research_pipeline_example).

## Repository structure

```
ai-research-talk/
├── spark_talk_ai_research_slides.qmd   the deck's source; this is the file to edit
├── spark_talk_ai_research_slides.pdf   the rendered slides
├── template/
│   ├── talk_template.sty               WHU beamer template
│   └── 00_whu_logo.png                 WHU logo that the template loads
├── images/                             pictures and figures shown on the slides
│   └── folder_structure.tex            figure of the reproducible folder structure
├── references/
│   ├── references.bib                  bibliography
│   └── apa.csl                         APA 7 citation style
├── .gitignore                          keeps build files out of git
└── README.md                           this file
```

## Building the slides

```bash
git clone https://github.com/victorvanpelt/ai-research-talk.git
cd ai-research-talk
quarto render spark_talk_ai_research_slides.qmd
```

### Requirements

- **Quarto** to render the deck.
- **A LaTeX distribution** for the PDF. [TinyTeX](https://yihui.org/tinytex/) is the easiest (`quarto install tinytex`).
- **The Lato font**, which the template uses when it is installed. The deck also builds without it.

---

Maintained by [Victor van Pelt](https://www.victorvanpelt.com).
