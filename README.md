# GitHub 101 practice prototype (github-101-practice-prototype)

A practice GOV.UK Prototype Kit prototype for the GitHub 101 for designers workshop. You can change anything here. Nothing in it is used for real work.

The fictional service is "Apply for a community garden plot".

## Before the workshop

1. Clone this repo. In your terminal, go to the folder where you keep prototypes and run:

   ```
   git clone https://github.com/CPS-Innovation/github-101-practice-prototype.git
   cd github-101-practice-prototype
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
| `main` | The real version. Do not push to it directly. |
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
| On GitHub, select Squash and merge, then Delete branch. | Your change is now in main |
| Switch to main, pull, and delete my old branch. | Your Mac is ready for the next change |

Type these yourself to check where you are:

```
git status
git branch
git log --oneline -5
```

## Merge conflicts: current and incoming

When Git cannot merge two changes to the same lines, it marks them in the file like this:

```
<<<<<<< HEAD
<h1 class="govuk-heading-xl">Get a plot in your local community garden</h1>
=======
<h1 class="govuk-heading-xl">Grow your own food in a community garden</h1>
>>>>>>> main
```

| Word | What it means | In the example |
| --- | --- | --- |
| Current change | What's on the branch you're on now (HEAD). Usually your work. | The top half, from your branch |
| Incoming change | What you're merging in. Usually main, with other people's work. | The bottom half, from main |

Editors such as VS Code give you buttons for each conflict:

- **Accept current change**: keep your version, drop theirs
- **Accept incoming change**: keep their version, drop yours
- **Accept both changes**: keep both. For a heading, that means two headings, which is usually wrong
- **Compare changes**: show them side by side

Which button to use is a design decision. Choose the version you want, check the file looks right, then commit.

During a rebase, current and incoming swap round. That's one reason we ask the AI not to rebase.
