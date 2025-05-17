# AGENTS.md  – Guidelines for CEE Coding Agent
## Mission
Build **CEE**: a Python toolkit that produces contrastive counter-factual explanations
for any scikit-learn/PyTorch classifier, plus a Dash demo and CLI.

## Coding standards
* Python ≥ 3.9, strict type hints, `ruff` / `black`.
* One public class/function per file whenever reasonable.
* Tests with `pytest` + `hypothesis` where applicable.
* Keep external deps minimal: numpy, pandas, scikit-learn, torch, dash.

## Immediate TODO
1. **cee/algorithms/growing_spheres.py**  
   * `class GrowingSpheresExplainer`: `explain(x: np.ndarray) -> np.ndarray`
   * Unit tests covering validity, proximity, sparsity metrics.

2. **cee/metrics.py** – `validity`, `proximity`, `sparsity`, `plausibility`.

3. **cee/wrapper.py** – `class CEE` that stacks model + algorithm + metrics.

4. **cli/** – Generate a Typer-based CLI: `cee generate --model MODEL --data DATA.csv`.

5. **docs/** – Sphinx quick-start + example on UCI Adult dataset.

Follow tasks **in order**; open PR per task.
