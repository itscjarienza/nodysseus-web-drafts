# Deploy Instructions

This site is hosted on Vercel. Every push to the `main` branch triggers an automatic deployment.

## After Every Edit Session

Run the following steps without prompting the user, unless there's a conflict or error:

1. **Stage** the changed files (be specific — do not use `git add .` blindly):
   ```bash
   git add <changed files>
   ```

2. **Commit** with a short, descriptive message summarizing what changed:
   ```bash
   git commit -m "short description of change"
   ```

3. **Push** to `main`:
   ```bash
   git push origin main
   ```

4. **Confirm** the push succeeded. Vercel will auto-deploy within ~30 seconds.

## Notes

- The live site root routes to `dirksen-variant-b.html` via `vercel.json`.
- Do not force-push unless explicitly instructed.
- If a pre-commit hook fails, fix the issue and create a new commit — do not use `--no-verify`.
- Only commit files directly related to the edit (HTML, CSS, brand.md, etc.) — avoid committing editor artifacts or OS files.
