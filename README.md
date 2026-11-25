# hci2k-running-plan-disclosure

Diary data pipeline for the HCI2000 study *Effects of Training Plan Disclosure Pacing on Runners' Cognitive Load and Perceived Exertion*.

## Data privacy (read first)

Real participant data must never be committed (consent form, RA 10173). `data/` and `processed/` are git-ignored, and the notebook is committed **without outputs**, because its outputs print diary answers and ratings.

Before every commit:

- `git status` shows nothing under `data/` or `processed/`.
- Clear all outputs in the notebook (Jupyter: *Edit → Clear Outputs of All Cells*; VS Code: *Clear All Outputs*).

## Running

1. `pip install -r requirements.txt`
2. Put two files in `data/`:
   - `diary_responses.csv`: the Google Forms export of the post-run diary.
   - `participant_key.csv`: columns `participant_code, condition, experience_group`.
3. Open `Diary_Data_Pipeline.ipynb` and *Run all*. Tables and figures are written to `processed/`.
