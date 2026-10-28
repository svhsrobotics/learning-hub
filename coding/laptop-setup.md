# Setting Up Your Laptop for Coding

**The short version:** install Android Studio and Git, make your own GitHub account, get added to the team, download (clone) your team's code, open it, build it, and send it to the robot. Plan on about an hour, mostly waiting for downloads. **Do this with a mentor or your code captain nearby the first time.**

This page is for **Windows** laptops. Each step has a **Why** line, so you know what you're doing and not just clicking.

## Before you start

| You need | Why |
|---|---|
| A Windows laptop (or a Mac) that you can install programs on | Android Studio is a big program. **School Chromebooks can't run it.** If you don't have a laptop that works, ask a mentor about team laptops. |
| At least 8 GB of free disk space, 8 GB of memory (RAM), and a good internet connection | Those are the minimums for Android Studio on Google's [system requirements page](https://developer.android.com/studio/install); a solid-state drive with 32 GB free is better. The robot project downloads a few more gigabytes the first time. (Google lists bigger numbers for the Android emulator, which robot code doesn't use.) |
| Permission to install software | On a school or family computer, ask whoever manages it first. |
| About an hour | Most of it is waiting for downloads. Bring something to read. |

## Step 1. Install Android Studio
1. Go to **developer.android.com/studio** and download Android Studio for Windows.
2. Run the installer and keep the default options.
3. The first time it opens, let the setup wizard download what it wants (the "Standard" setup is fine).

**Which version?** This season's robot software (SDK 12.0) needs **Android Studio Narwhal 3 Feature Drop or newer**. The current download is newer than that, so the latest version is fine. FIRST's official docs, at **ftc-docs.firstinspires.org**, list what each SDK version needs.

**Why Android Studio?** The Control Hub runs Android (the same system as many phones). Android Studio is the official tool for building Android apps, and our robot code becomes an Android app.

## Step 2. Install Git for Windows
1. Go to **git-scm.com** and download Git for Windows.
2. Run the installer. The default options are fine. Click Next until it finishes.
3. Check it worked: open **Git Bash** from the Start menu and type:
   ```
   git --version
   ```
   It should print a version number. If it says "not recognized", restart the laptop and try again.

**Why Git?** Git keeps every saved version of the code and lets the whole team share it without overwriting each other's work. It's like save points in a video game. See [Git and GitHub](coding/git-and-github.md).

## Step 3. Make your own GitHub account
1. Go to **github.com** and sign up.
2. **Use your own account, not a shared team login.**
3. Pick a username you're happy for others to see. It doesn't need your full name.
4. **If you're under 13, stop here and talk to a mentor and your parent or guardian first.** GitHub has its own rules about age, and the adults will sort out what's allowed.
5. **Team rule:** turn on **Keep my email addresses private**. It's in GitHub's **Settings > Emails**. Ask a mentor if you can't find it.

**Why your own account?** Every change you save is stamped with your name, so your work is credited to you. That matters for judging (students are supposed to program their own robot) and lets you show your work later.

**Why is this a team rule?** Our team repos are public, and Git writes an email address on every change you save. Anyone on the internet could read it. With this setting on, GitHub gives you a private stand-in address to use instead, so your real email never appears.

## Step 4. Tell Git who you are
Open Git Bash and type these three lines. Use your **GitHub username** and the private address GitHub shows you on that same **Settings > Emails** page (it ends in `@users.noreply.github.com`):
```
git config --global user.name "your-github-username"
git config --global user.email "the-email-github-shows-you"
git config --global pull.rebase false
```
**Why:** Git stamps every snapshot with this name and email. If they match your GitHub account, GitHub credits the work to you. The third line tells Git to combine work in the simplest, safest way when you pull (it never rewrites history), and stops Git from asking you about it every time.

## Step 5. Get added to the team on GitHub
1. Send your **GitHub username** (not your password, ever) to your code captain or a mentor.
2. You'll get an email invitation to join the **svhsrobotics** organization on GitHub. Click **Accept**.

**Why:** all of the program's code lives in the svhsrobotics organization on GitHub. Everyone can *read* every team's code, which is how the teams learn from each other.

## Step 6. Download (clone) your team's code
Your team's repo:

| Team | Repo |
|---|---|
| Gamma | `svhsrobotics/BIOBUZZ2627-Gamma` |
| Psi | `svhsrobotics/BIOBUZZ2627-Psi` |
| Robotica | `svhsrobotics/BIOBUZZ2627-Robotica` |

**Using Android Studio's buttons (easiest):**
1. On Android Studio's welcome screen, click **Clone Repository** (or, with a project open, **File > New > Project from Version Control**).
2. URL: `https://github.com/svhsrobotics/BIOBUZZ2627-Gamma.git` (use your team's name).
3. Directory: `C:\FTC\BIOBUZZ2627-Gamma`
4. Click **Clone**. If a GitHub sign-in window pops up, sign in with your own account.

**Or by typing (in Git Bash):**
```
mkdir C:/FTC
cd C:/FTC
git clone https://github.com/svhsrobotics/BIOBUZZ2627-Gamma.git
```

**Why `C:\FTC` and not Documents, Desktop, or OneDrive?** OneDrive and similar sync tools copy files while Git and Android Studio are working on them, and they fight. Windows also has trouble with very long folder paths, and our project already has deep folders. A short path avoids both problems.

**Why clone instead of downloading a ZIP?** A ZIP is one frozen copy with no history. A clone stays connected to GitHub, so you can pull teammates' changes and push yours.

## Step 7. First Gradle sync, and never accept the AGP upgrade
1. If Android Studio didn't open the project after cloning, use **File > Open** and pick `C:\FTC\BIOBUZZ2627-Gamma` (the top folder, not TeamCode).
2. Wait. Android Studio runs a **Gradle sync** (a progress bar at the bottom of the window). The first one can take 5 to 15 minutes because it downloads FIRST's libraries.
3. If a pop-up offers to **upgrade the Android Gradle Plugin** ("AGP Upgrade Assistant"), **say no**. Close it, or choose "Don't ask for this project."

**Why sync?** Gradle reads the build recipe and downloads everything the project needs. Until the sync finishes, Android Studio shows lots of red errors that aren't real.

**Why never accept the AGP upgrade?** FIRST picks exact build-tool versions that work with their robot software. The upgrade assistant rewrites FIRST's build files to newer versions, which can break the build, and it creates changes in FIRST's files that clash with future SDK updates. Our program has already had this happen once. It's like a game "helpfully" updating itself the morning of a tournament.

**Other pop-ups:** if Windows Defender or Android Studio suggests excluding the project folders from virus scanning, **ask a mentor** before clicking. It makes builds much faster, but it changes a security setting, so an adult should decide.

## Step 8. Build it once
Use **Build > Assemble Project** from the menu. (Older guides say "Make Project". Newer Android Studio doesn't have that menu item.) Wait for the bottom bar to say the build finished.

**Why build before touching the robot?** If it builds on your laptop, the problem isn't your setup. That makes later problems much easier to track down.

## Step 9. Connect to the Control Hub
1. Turn the robot on. Wait about 30 seconds for the Control Hub to start.
2. **Over Wi-Fi:** on your laptop, join the robot's Wi-Fi network. It's named after the team number, like `19831-RC` (rule R705 sets this naming). Get the password from your code captain. **Never post the password anywhere.**
3. **Or over a USB cable:** plug a USB-C cable from the laptop into the Control Hub.
4. In Android Studio, look at the **device dropdown** at the top (next to the green Run arrow). The Control Hub should appear in the list.

**Why Wi-Fi?** No cable to trip over while the robot drives. **Why USB sometimes?** It's faster and more reliable when Wi-Fi is acting up.

**Heads up:** while your laptop is on the robot's Wi-Fi, it usually has **no internet**. So pull from GitHub *before* you connect, and push *after* you disconnect. At events, laptops must be off the robot's Wi-Fi during matches (rule R704.C).

## Step 10. Send your code to the robot (deploy)
1. Make sure the run configuration next to the Run arrow says **TeamCode**.
2. Make sure the Control Hub is picked in the device dropdown.
3. Click the green **Run** arrow (or press Shift+F10).
4. Wait for "Install successfully finished" or similar at the bottom.

**Why:** the Run button builds the app and installs it on the Control Hub. Your new code is used the next time someone picks an OpMode on the Driver Station.

## Step 11. Run your OpMode on the Driver Station
1. **Safety first:** the first time, put the robot **up on a block or stand so the wheels can't touch the floor**, and tell everyone nearby you're about to run it.
2. On the Driver Station, open the program list. TeleOp programs and Autonomous programs are in separate lists.
3. Pick your OpMode. Press **INIT**, then **START (the play button)**.
4. Press **STOP (the square)** when you're done.

**Why the block?** New code does surprising things. A robot with its wheels in the air can't drive off the table or into someone's ankles.

## You're set up!
Next: read [From laptop to robot](coding/laptop-to-robot.md) to understand what just happened, and [Git and GitHub](coding/git-and-github.md) for your everyday routine.

## If something goes wrong

| Problem | Try this |
|---|---|
| Lots of red errors right after opening | Wait for Gradle sync to finish. Then **File > Sync Project with Gradle Files** (Ctrl+Shift+O). |
| "git is not recognized" | Restart the laptop after installing Git. |
| Control Hub not in the device list | Check the laptop is on the robot's Wi-Fi (or the cable is plugged in), wait for the hub to finish starting, then ask your code captain. |
| Your OpMode isn't on the Driver Station | Did the install finish? Is it marked `@Disabled`? Is the name in `@TeleOp(name = "...")` unique? |
| An error you don't understand | **Stop.** Copy the message (or take a photo) and ask. Don't click random fixes. |
