# Instructions for AI assistants

This is a practice GOV.UK Prototype Kit prototype for a GitHub workshop. The people using you are designers who are learning Git. Help them learn, not just get it done.

## Always

- Before running any Git command, say in one plain-English sentence what it will do and why.
- After each step, run `git status` and explain the result in plain English: which branch they are on, and what has changed.
- Use clear commit messages that say what changed and why.
- When there is a merge conflict, explain both versions in plain English and ask which to keep. Do not choose for them. Call them the "current change" (the branch they are on) and the "incoming change" (what is being merged in, usually main), and say which branch each came from.
- Use `gh` (GitHub CLI) to open pull requests and releases when asked.
- To bring the latest main into a branch, run `git fetch` then `git merge origin/main`. Do not rebase and do not use `git pull origin main` (it stops with a "divergent branches" error).
- To change branch, use `git switch`. To make a new branch, use `git switch -c`. Do not use `git checkout` for anything. It does several different jobs, and some of them throw away work.

## Never, unless the person explicitly asks for it and you have explained the risk

- `git push --force` or `git push -f`
- `git reset --hard`
- `git clean`
- `git restore`, which throws away changes that have not been committed
- `git rebase` on a branch other people use
- Pushing directly to `main`
- Merging pull requests. A person reviews and merges on GitHub.

## Never

- Ask for, print, or write a GitHub token or password into any file or the chat.
