# Thesis repo: rules for Claude

Bachelor thesis of Francisco Waggershauser, KIT ECON, Chair of Economic Theory.
Working title (since 13.10.2026, may change until submission): *When Does Round-Robin Achieve EFX? A Simulation-Based Average-Case Analysis*.
Supervisor Matthias Ammann. Synced with Overleaf via GitHub, Overleaf only sees `main`.

## Workflow
- Pull `main` before every edit. Francisco may have pushed from Overleaf in the meantime.
- Never edit a passage Francisco is currently working on in Overleaf.
- One chapter per file. New chapters go into `main.tex` via `\include`, result blocks into
  `chapters/04_results/04_results.tex` via `\input`.
- Figures are copied into `figures/` by hand. Reference them by file name only
  (`\includegraphics{block2_fig_q.pdf}`), `\graphicspath` points to `figures/`.
- No generated number macros. Numbers are typed in, and every number comes from the
  confirmatory run `results/aggregate_R20000_seed20260927/` (see Befundstand in the project).

## Writing
- Thesis text in English, chat in German.
- No dashes (hyphen or em dash) as sentence punctuation. Compound words and math are fine.
- Every claim carries exactly one status: proven, measured, or conjectured. Never blur it.
- Cite named results by content, not by number alone.
- Axis and text labels: Gini instead of theta, Spearman instead of rho; every Gini value
  with theta in parentheses.

## Notation (macros in `notation.tex`, use them)
- `\astar` = alpha*, `\aij` = alpha_ij, `\Surv` / `\Survhat` = S_X / hat S_X.
- theta for dispersion (never tau, tau is Kendall), eta for private noise.
- q = m mod n is the remainder (literature often uses q for the quotient; say so once).
- Theorem environments: theorem, lemma, proposition, corollary, conjecture, definition,
  example, remark (shared counter per chapter).
