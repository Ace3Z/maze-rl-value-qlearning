# maze-rl-value-qlearning



Comparative study of **Value Iteration** and **Tabular Q-learning** on a deterministic **10 × 10 maze** that forces the agent to visit a **sub-goal** before the final goal. All code, experiments and visualisations are provided in Jupyter notebooks.

---

## 📁 Project contents
| File | Purpose |
|------|---------|
| `Code.ipynb` | Main notebook: environment, algorithms, plots |
| `Extended Version Proj Maze.ipynb` | Second notebook with an alternative sub-goal layout |
| `Report.pdf` | Full write-up of methodology, experiments and results |

---

## 🧠 Algorithms implemented
| Algorithm | Key settings |
|-----------|--------------|
| **Value Iteration** | γ = 0.95, ΔV threshold = 1 × 10⁻⁴; exhaustive sweep over 200 state–action pairs :contentReference[oaicite:0]{index=0} |
| **Tabular Q-learning** | γ = 0.95, α = 0.10, ε = 0.05 (tuned with Optuna for fastest convergence) :contentReference[oaicite:1]{index=1} |

---

## 🌍 Environment
* 10 × 10 grid with walls (black), start (yellow), sub-goal (blue) and end goal (green).  
* **Deterministic** transitions; illegal moves leave the agent in place.  
* **Reward scheme**: step −0.1, wall −1, sub-goal +1, goal +10, premature-goal −10. :contentReference[oaicite:2]{index=2}

---

## 🚀 Quick start  

```bash
git clone https://github.com/your-username/maze-rl-value-qlearning.git
cd maze-rl-value-qlearning
# create environment (example using conda)
conda create -n maze-rl python=3.10
conda activate maze-rl
pip install numpy matplotlib tqdm optuna jupyter
jupyter lab
# open Code.ipynb and run all cells
```
