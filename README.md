# CNN Cats vs Dogs → LinkedIn vs Interpol (Bonus)

This project is a two-part computer vision journey:

1. **Learn the basics with a classic task:** classify **cats vs dogs**.  
2. **Try a fun bonus challenge:** classify face photos into **“LinkedIn-like” vs “Interpol-like”** groups.

The goal is less about deep CNN theory and more about the **project idea, experimentation flow, and what we learn from the results**.

---

## Project Concept

### Phase 1 — Cats vs Dogs (Core Project)
The first part builds a standard image classification pipeline:
- prepare and split the dataset
- train a baseline CNN
- evaluate performance
- improve the model with transfer learning (MobileNetV2 + augmentation)

This phase is the “clean” learning track: build something reliable on a well-known binary classification task.

### Phase 2 — LinkedIn vs Interpol (Fun Bonus)
The second part is an exploratory challenge:
- use a face dataset as a proxy for “LinkedIn-style” profile pictures
- use a wanted-criminal image dataset as “Interpol-style” images
- train a classifier and check if performance is truly meaningful

This phase is intentionally playful and highlights an important ML lesson:  
**high accuracy can come from dataset shortcuts (bias/artifacts), not true understanding.**

---

## What the Notebook Covers

The notebook (`main.ipynb`) walks through:
- data extraction and exploration
- train/test split creation
- baseline CNN training
- transfer learning upgrade
- evaluation with confusion matrix and metrics
- bonus face classification experiment
- bias check using circular masking to reduce framing artifacts

---

## Datasets Used

- **Cats vs Dogs filtered dataset** (local zip in notebook workflow)  
- **CelebA** (used as LinkedIn-like face proxy)  
- **Most Wanted Criminals / Interpol-style dataset** (Kaggle source in notebook)

> Note: the LinkedIn/Interpol framing is a **project narrative for experimentation**, not an identity or ethics benchmark.

---

## Key Results (from the notebook run)

- **Cats vs Dogs baseline CNN:** moderate performance (~0.69 test accuracy in this run)
- **Cats vs Dogs with transfer learning:** major improvement (near 0.99 accuracy in this run)
- **LinkedIn vs Interpol bonus:** very high scores, which motivated a bias check
- **After circular masking:** still very high score in this run, used to test whether framing cues dominated learning

Results may vary depending on execution environment, random seeds, and dataset sampling.

---

## Why This Project Is Interesting

- It starts with a classic beginner-friendly problem.
- It evolves into a more creative experiment.
- It demonstrates a real ML pitfall: **“good metrics” do not always mean “good reasoning.”**
- It encourages thinking about data quality, shortcut learning, and fairness in evaluation.

---

## Run the Project

This project is notebook-based.

1. Open `main.ipynb` (Google Colab recommended).
2. Make sure dependencies are available (`tensorflow`, `scikit-learn`, `matplotlib`, `seaborn`, `Pillow`, `kagglehub`, `datasets`).
3. Run cells in order.
4. For the bonus part, ensure Kaggle access works in your environment.

---

## Repository Structure

```text
.
├── main.ipynb   # Full workflow: cats/dogs + bonus experiment
└── README.md
```

---

## Future Improvements

- Use stricter data curation for the bonus task
- Add stronger bias/leakage checks
- Evaluate across more diverse face datasets
- Package notebook steps into reusable scripts/modules