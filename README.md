# R fake clinical trial

Playing with R on a **made-up** clinical trial dataset: patients in a control group and an intervention group, with depression, anxiety and "other issues" scores before and after. Every number in it is invented, so no real patient data is involved.

## Why it exists

A practice project to get comfortable with R and the tidyverse, using the Kaggle dataset **Fake Clinical Trial** (`Clinical trial made up data.csv`).

## What is in here

- `r-for-clinical-trial.ipynb`: the notebook (R kernel)
- `r-for-clinical-trial.r`: the same notebook as exported by Kaggle. Despite the `.r` extension it is a JSON notebook file, not a plain R script.

## What it does

1. Loads the CSV and renames the columns (`Pre_Intervention_Depression`, `Post_Intervention_Anxiety`, ...).
2. Fixes column types.
3. Prints summaries and a correlation matrix drawn with `corrplot`.
4. Plots pre-intervention depression vs. anxiety, and pre vs. post depression for the intervention group.

The notebook was saved without outputs, so there are no numbers to quote. Run it to see them.

## How to run it

The dataset is **not** in this repo. Download it from Kaggle, then edit the `read_csv` path in the first code cell (it points at `/kaggle/input/fake-clinical-trial/`). You need R plus an R Jupyter kernel (IRkernel), and these packages:

```r
install.packages(c("tidyverse", "corrplot"))
```

Easiest option: open it directly on Kaggle, where R and the data are ready.

## What I learned

R's `summary()` and `corrplot` are a very fast way to get a feel for a table, and `read_csv` is happy to guess column types wrong, so check them.

## Heads-up

- No license file yet, so by default all rights are reserved.
- I have not re-run the notebook.
