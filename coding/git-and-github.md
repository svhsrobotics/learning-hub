# Git and GitHub: How We Save and Share Code

**The short version:** every day it's **pull, edit, build, test, commit, push**. Keep `master` working. Try risky things on a branch. Tag the code before every event. Never force push. If Git says something you don't understand, stop and ask.

## How Git works: a chain of snapshots
Git doesn't just store "the code". It stores a **chain of snapshots** (commits). Each snapshot points back to the one before it. When you clone a repo, you get the whole chain, not just the latest files.

Think of save points in a video game: you can always go back to an earlier save, and you can see what changed between saves.

### The photocopied lab notebook
Three students each photocopy the same lab notebook and keep writing in their own copy. Later, one of them fixes a mistake on page 12. Because all three copies started from the same original pages, it's easy to see that page 12 changed and copy just that fix into the other two.

If one student had **retyped** the notebook from scratch, nobody could tell what was original and what was new.

That's how Git merges work. Because copies share the same early snapshots, Git can look back to the last snapshot they had in common, see what each side changed, and combine just those changes. That's why we always **clone** (keep the history) and never start fresh from a ZIP.

## Our GitHub setup
<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 460 336" role="img" aria-label="FIRST's code is forked into the starter repo BIOBUZZ2627No-Roadrunner, which is forked once per team"><defs><marker id="repo-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0 0L10 5L0 10z" fill="#5f5f66"/></marker></defs><rect x="110" y="6" width="240" height="50" rx="10" fill="#f6f4f4" stroke="#5f5f66" stroke-width="1.5"/><text x="230" y="27" text-anchor="middle" font-size="14" font-weight="800">FIRST's FtcRobotController</text><text x="230" y="45" text-anchor="middle" font-size="12.5" fill="#5f5f66">SDK 12.0</text><path d="M230 56v26" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#repo-arrow)"/><text x="242" y="74" font-size="12.5" fill="#5f5f66">fork: Sync fork brings SDK updates</text><rect x="60" y="86" width="340" height="104" rx="12" fill="#fbecee" stroke="#A60012" stroke-width="2"/><text x="230" y="110" text-anchor="middle" font-size="15" font-weight="800">BIOBUZZ2627No-Roadrunner</text><text x="230" y="127" text-anchor="middle" font-size="12.5" fill="#5f5f66">the starter repo, run by the lead programmer</text><rect x="76" y="138" width="308" height="20" rx="10" fill="#fff" stroke="#A60012"/><text x="230" y="152" text-anchor="middle" font-size="12" font-family="monospace">master: FIRST's SDK 12, as is</text><rect x="76" y="162" width="308" height="20" rx="10" fill="#fff" stroke="#8a6d00" stroke-dasharray="4 3"/><text x="230" y="176" text-anchor="middle" font-size="12" font-family="monospace">roadrunner: + Road Runner (optional)</text><path d="M230 190L80 248M230 190v58M230 190L380 248" fill="none" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#repo-arrow)"/><text x="230" y="222" text-anchor="middle" font-size="12.5" font-weight="700" fill="#18181b" stroke="#fff" stroke-width="5" paint-order="stroke">one fork per team</text><rect x="4" y="252" width="148" height="56" rx="10" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="78" y="274" text-anchor="middle" font-size="11.5" font-weight="800">BIOBUZZ2627-Gamma</text><text x="78" y="294" text-anchor="middle" font-size="12" fill="#5f5f66">master = robot code</text><rect x="156" y="252" width="148" height="56" rx="10" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="230" y="274" text-anchor="middle" font-size="11.5" font-weight="800">BIOBUZZ2627-Psi</text><text x="230" y="294" text-anchor="middle" font-size="12" fill="#5f5f66">master = robot code</text><rect x="308" y="252" width="148" height="56" rx="10" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="382" y="274" text-anchor="middle" font-size="11.5" font-weight="800">BIOBUZZ2627-Robotica</text><text x="382" y="294" text-anchor="middle" font-size="12" fill="#5f5f66">master = robot code</text><text x="230" y="330" text-anchor="middle" font-size="12.5" fill="#5f5f66">Everyone can read every repo.</text></svg><figcaption>All four repos are in the svhsrobotics organization on GitHub.</figcaption></figure>

| Repo | What's in it |
|---|---|
| `BIOBUZZ2627No-Roadrunner` (the **starter repo**) | FIRST's SDK 12.0 as is, with no extra files of ours. An optional `roadrunner` branch has Road Runner set up, untuned |
| `BIOBUZZ2627-Gamma` | Gamma's robot code |
| `BIOBUZZ2627-Psi` | Psi's robot code |
| `BIOBUZZ2627-Robotica` | Robotica's robot code |

**Everyone can read every repo.** Reading other teams' code is a great way to learn.

**Why `master`?** It's the name FIRST uses for its main branch, so every repo keeps it. Some other projects call it `main`; it's the same idea.

### Why one repo per team?
Last season all teams shared one repo with a branch per team. It caused real problems:
- **Anyone could change anyone's code.** GitHub can only set permissions per repo, not per branch.
- **Every team carried every other team's files**, and other teams' test programs showed up on every team's Driver Station.
- **Shared files drifted apart.** The same settings file ended up in 3 different versions.
- **Branches piled up.** Most were abandoned, and it was hard to find the real code.

Separate repos fix all of that. The starter repo in the middle keeps the one good part: fix something once, and every team can pull the fix in.

### Why a starter repo?
It's the one place for things every team needs: FIRST's SDK, shared helper code, and the Road Runner setup. Fix something once there, and every team can bring the fix in.

### Forks: copies that remember where they came from
The starter repo is a **fork** of FIRST's repo, and each team repo is a fork of the starter repo. A fork is a full copy on GitHub with the same history (the photocopied notebook), and it remembers its parent. That's what [FIRST's own docs](https://ftc-docs.firstinspires.org/en/latest/programming_resources/tutorial_specific/android_studio/fork_and_clone_github_repository/Fork-and-Clone-From-GitHub.html) tell teams to do.

Because a fork remembers its parent, GitHub shows when your repo is behind ("This branch is 3 commits behind"), and a **Sync fork** button brings the new work in. Updates never arrive on their own: a person clicks the button when the team is ready to build and test.

## Everyday workflow
You'll mostly use **Android Studio's Git buttons**. The typed commands do the same thing and are shown so you know what the buttons really do. (Menu names can move a little between Android Studio versions.)

| Step | Android Studio | Typed command (in the Terminal) | Why |
|---|---|---|---|
| 1. Get the latest | **Git > Pull** (or the blue down arrow, "Update Project", Ctrl+T) | `git pull` | Start from everyone's newest code so your changes don't collide with theirs |
| 2. Edit, build, test | Build > Assemble Project, then Run on the robot | | **`master` must always build.** Test before you share |
| 3. Save a snapshot | **Git > Commit** (Ctrl+K). Tick the files, type a message, click **Commit** | `git add .` then `git commit -m "Message"` | A snapshot you can always come back to |
| 4. Share it | **Git > Push** (Ctrl+Shift+K), then **Push** | `git push` | Teammates can now pull your work |

The Terminal is inside Android Studio: **View > Tool Windows > Terminal**.

### Good commit messages
- Good: `Slow mode now 30% for lining up shots`
- Bad: `stuff`, `fix`, `asdf`

**Why:** when something breaks, the history is how we find out what changed. Small commits with clear messages make it easy to find and undo exactly one change.

### Commit vs push
**Commit** saves a snapshot on your laptop. **Push** uploads your snapshots to GitHub. You can commit many times and push once. Nobody sees your commits until you push.

## Trying something risky: experiment branches
`master` is always the code that's on the robot and drives. To try something big, make a branch.

| Step | Android Studio | Typed command |
|---|---|---|
| Make a branch | Click the branch name (top left or bottom right of the window) > **New Branch**, name it `launcher-test` | `git checkout -b launcher-test` |
| Work and commit as normal | Same as above | Same as above |
| Share the branch | **Git > Push** | `git push -u origin launcher-test` |
| It works! Bring it into master | Switch to `master` (branch menu > master > **Checkout**), **Pull**, then branch menu > `launcher-test` > **Merge into Current**, then **Push** | `git checkout master` then `git pull` then `git merge launcher-test` then `git push` |
| It didn't work | Switch back to `master`, then branch menu > `launcher-test` > **Delete** | `git checkout master` then `git branch -D launcher-test` |

**Why:** an experiment branch lets you try a big change without risking the robot's working code. If it works, merge it. If not, delete it and `master` never knew. **Delete branches once they're merged or abandoned**, so they don't pile up like last year. Your code captain can help.

When you switch branches, your folder changes to show that branch's files. Files that "disappear" are safe on the other branch.

## Getting shared fixes from the starter repo
Usually the code captain does this, on the GitHub website:

1. Open your team's repo. If it says **"This branch is X commits behind svhsrobotics/BIOBUZZ2627No-Roadrunner:master"**, there's an update.
2. Click **Sync fork**, then **Update branch**.
3. On your laptop: **Git > Pull**, then build and test before the next match.

**Why build after syncing:** Sync fork only combines the code on GitHub. It never builds it. `master` must always build, so check on a laptop before anyone needs the robot.

**If Sync fork says there's a conflict,** stop. **Never click "Discard commits"**: that throws away your team's own work.

## Adding Road Runner to your team's repo
Road Runner is optional, so it waits on the starter repo's `roadrunner` branch until a team asks for it. Robotica uses it; Gamma and Psi may never need it. When your team is ready (your robot drives, and your odometry pods are mounted):

1. In your team's repo: **Pull requests > New pull request**, then click **compare across forks**.
2. **Base repository:** your team's repo, branch `master`. **Head repository:** `svhsrobotics/BIOBUZZ2627No-Roadrunner`, branch `roadrunner`.
3. **Create pull request**, then **Merge pull request**.
4. On your laptop: **Git > Pull**, build, then start tuning on your own robot.

**Why a pull request:** it shows exactly which files are coming in before anything changes, and it's all on the website.

## Before every event: tag what's on the robot
```
git tag meet1-2026-11-14
git push origin meet1-2026-11-14
```
(Use the real event's name and date. This one is just an example.)
(Android Studio: **Git > New Tag**. Tags may need to be pushed separately; tick "Push tags" in the Push window.)

**Why:** a tag is a bookmark that never moves. If something breaks after the meet, we can always get back to exactly the code that worked. Without tags, it's hard to know later exactly what code ran at which event.

Also before an event: mark test OpModes `@Disabled` so the Driver Station list stays short and nobody picks the wrong one.

## Merge conflicts (don't panic)
A merge conflict means two people changed **the same lines**, and Git won't guess which version is right. It's normal and fixable.

1. Android Studio shows the conflicted files in red and opens a **Conflicts** window (or use **Git > Resolve Conflicts**).
2. Click **Merge...** to see three panels: your version, the other version, and the result in the middle.
3. Decide what the code should be. Often it's a bit of both. Use the arrows to take changes from each side.
4. Click **Apply**, build to make sure it works, then commit and push.

If you're typing instead: the file shows both versions between `<<<<<<<` and `>>>>>>>` markers. Edit it to the right code, delete the markers, build, then `git add .`, `git commit`, `git push`.

**Not sure which version is right? Stop and ask the person who made the other change.** Pulling often and keeping commits small keeps conflicts rare and tiny.

## Our rules
1. **`master` always builds.** If someone pulls broken code right before a match, they can't deploy anything.
2. **Never force push** (`git push --force`, or "Force Push" in Android Studio). A normal push adds snapshots to the chain. A force push replaces the chain on GitHub with yours, and can silently erase teammates' work. (`master` is planned to be protected so GitHub blocks it anyway.)
3. **Stop and ask.** If Git shows a message you don't understand, stop before clicking anything. Almost everything is easy to fix if we stop early.
4. **Pull before you start, push when you finish.**
5. **Use your own GitHub account.**
6. **Check where a pull request is going.** On a fork, GitHub suggests the parent repo first. Our pull requests stay inside our own repos. **Never send one to FIRST's repo.**

## Cheat sheet

| I want to... | Do |
|---|---|
| Get teammates' changes | `git pull` |
| See what I changed | `git status` |
| Save a snapshot | `git add .` then `git commit -m "What changed"` |
| Share my snapshots | `git push` |
| Start an experiment | `git checkout -b my-experiment` |
| Go back to master | `git checkout master` |
| Get shared starter fixes | On GitHub: **Sync fork > Update branch**. Then `git pull` and build |
| Tag before an event | `git tag meet1-2026-11-14` then `git push origin meet1-2026-11-14` |

## Questions people ask
**Can Gamma use code the older teams wrote?**
Yes. Shared things go in the starter repo, and your team brings them in with **Sync fork**. For one-off things, anyone can read any team's repo and copy a file over, with a comment at the top saying where it came from.

**Can we share tuning numbers between robots?**
No, and that's not a Git limit. Tuning numbers describe one robot's weight, wheels and motors. Another robot's numbers would make yours drive wrong. Teams share the setup and the know-how, and each robot gets tuned on its own.

**Why not one repo with a branch per team, like last year?**
GitHub can't restrict who changes which branch, every branch carried every team's files, and shared files drifted into different versions. Separate repos keep each team's code clean and safe.

**What if two people change the same file?**
Different lines: Git merges them automatically. Same lines: a merge conflict, and a person decides (see above).

**What's the difference between commit and push?**
Commit saves a snapshot on your laptop. Push uploads your snapshots to GitHub.

**Why can't I just copy the code onto a USB stick?**
A USB stick holds one version, with no history and no record of who changed what. If it breaks, there's no going back. Git keeps every version.

**Why do I need my own GitHub account?**
So your work is credited to you. It shows who built and programmed what, which helps in judging and helps you show your work later.

**What happens when FIRST releases an SDK update?**
The lead programmer clicks **Sync fork** on the starter repo and checks that it builds. Then each code captain clicks **Sync fork** on their team's repo, pulls, and builds. Because every repo shares FIRST's history, that's a normal merge, not a rebuild.

**Why are our repos forks instead of copies?**
FIRST's docs say teams should fork their repo. A fork keeps the full history like any copy, and it also remembers its parent, so GitHub can show when you're behind and bring updates in with one button.

**I broke master. Now what?**
Don't panic and don't force push. Every old version is still in the history. Tell your code captain or a mentor. Usually the fix is a new commit that undoes the bad one (`git revert`), which keeps the history honest and loses nothing.
