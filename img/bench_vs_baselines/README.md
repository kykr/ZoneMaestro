# 3D Indoor Scene Generation - Perceptual Evaluation

## User Study Website

### Quick Start

1. **Current directory structure** (already correct in this repo):
   ```
   img/bench_vs_baselines/
   ├── index.html
   ├── README.md
   ├── case1/
   │   ├── user_input.txt
   │   ├── layoutgpt.png
   │   ├── diffuscene.png
   │   ├── holodeck.png
   │   ├── idesign.png
   │   ├── layoutvlm.png
   │   ├── respace.png
   │   └── ours.png
   ├── case2/
   │   └── ...
   └── case9/
       └── ...
   ```

2. **Push to GitHub**:
   ```bash
   cd yuanxing_icml2026_latex
   git add .
   git commit -m "Prepare benchmark user study page"
   git push origin main
   ```

3. **Enable GitHub Pages**:
   - Go to repo Settings → Pages
   - Source: Deploy from a branch → `main` / `/ (root)`
   - Save → site root will be `https://YOUR_USERNAME.github.io/YOUR_REPO/`
   - User study page URL will be:
     `https://YOUR_USERNAME.github.io/YOUR_REPO/img/bench_vs_baselines/`

4. **For anonymous access** (ICML rebuttal):
   - Go to https://anonymous.4open.science/
   - Create anonymous repository from your GitHub repo
   - Share the anonymous link with reviewers

### How It Works

- Each evaluator opens the link, enters a Participant ID, and evaluates 9 cases
- Methods are displayed as "Method A–G" in **randomized order** (different per page load)
- After submitting, evaluator downloads a CSV file containing their responses
- The CSV includes both anonymous labels AND the real method mapping for your analysis

### Analyzing Results

The downloaded CSV has columns:
- `participant_id`: evaluator ID
- `case_id`: case1–case9
- `dimension`: zone / placement / combination
- `Method_A` through `Method_G`: 1 (selected) or 0 (not selected)
- `Method_A_real` through `Method_G_real`: actual method name (e.g., "ours", "respace")

To compute Satisfaction Rate per method per dimension, use the real method name columns to map anonymous labels back to actual methods.
