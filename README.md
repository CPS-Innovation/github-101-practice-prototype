# GitHub 101 practice prototype

A practice GOV.UK Prototype Kit prototype for the GitHub 101 for designers workshop. Nothing here matters, so break it, fix it and try things out.

The fictional service is "Apply for a community garden plot".

## Before the workshop

1. Clone this repo. In your terminal, go to the folder where you keep prototypes and run:

   ```
   git clone REPO-URL
   cd github-101-practice
   ```

2. Install and run it:

   ```
   npm install
   npm run dev
   ```

3. Open http://localhost:3000. You should see the "Apply for a community garden plot" start page.

4. Open your AI assistant (Claude Code, Codex, Copilot or similar) in the same folder, in a second terminal tab.

5. Ask your AI: "Run git status and tell me what it means." If it answers, you're ready.

## What's in here for the workshop

| Thing | What it's for |
| --- | --- |
| `main` | The real version. Don't push to it directly. |
| Tag `research-round-1` | Snapshot: start page and one question |
| Tag `research-round-2` | Snapshot: reworded question, plus a new one |
| Branch `demo-new-page` | Has an extra page at /demo-new-page. Switch to it to watch the prototype change. |
| Branches `heading-a` and `heading-b` | Both change the start page heading, so merging both causes a conflict. |
| `app/views/people/_template.html` | Copy this to make your own page in the hands-on exercise. |
| `AGENTS.md` and `CLAUDE.md` | Instructions that tell AI assistants to explain before acting and avoid dangerous commands. |

## The daily loop

| Say to your AI | What happens |
| --- | --- |
| Pull the latest from main and tell me what changed. | Your Mac catches up with GitHub |
| Make a new branch called your-name/about-me from the latest main. | A new label for your work |
| Commit my changes with a clear message about what I changed. | A save point on your Mac |
| Push my branch to GitHub. | GitHub gets your save points |
| Open a pull request for my branch and give me the link. | A page on GitHub asking to merge into main |
| Switch to main, pull, and delete my old branch. | Ready for the next change, after your PR is merged |

Type these yourself to check where you are:

```
git status
git branch
git log --oneline -5
```
