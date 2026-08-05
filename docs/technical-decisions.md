# Technical decisions — Kids Studio

Engineering choices that demonstrate **how** the system was built, not just **what** tools were used.

### Blocking QA, not checkbox QA

Export literally cannot proceed if child-safety QA fails — it's a pipeline dependency, not a warning banner.

### Credits before compute

Every paid step checks balance first; pipelines pause and auto-resume instead of failing silently mid-render.

### FFmpeg in API container

Render/subtitle/thumbnail are compute steps you own — not outsourced to yet another API.

