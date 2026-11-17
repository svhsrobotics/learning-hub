# Add Pedro Pathing to Your Code

<p class="hub-lead"><b>Pedro Pathing</b> is a free library that drives your robot along paths in autonomous. Adding it to your team's robot project takes <b>3 lines in one build file</b> and <b>one copied folder</b>. Each team does this once, on a branch.</p>

> **What this page covers:** from "no Pedro" to "the project builds with Pedro in it." Tuning Pedro on your robot comes after this and isn't on this page. New to Pedro? Start with <a href="coding/pedro-explainer.html">Autonomous with Pedro Pathing</a>.

<p class="hub-why">Each team adds Pedro to its own project, not a shared copy. Pedro put out three versions between September and October 2026, and every robot's Pedro settings are different anyway. This is the "Manual Installation" on Pedro's own website, pedropathing.com.</p>

## Before you start

- Android Studio open with **your team's robot project**, and a build that works.
- About 15 minutes. No robot needed.

## Part 1: add the library

**1. Make a branch** named `pedro-setup`, starting from `master` (see <a href="#/coding/git-and-github?id=trying-something-risky-experiment-branches">Trying something risky</a>).

<p class="hub-why">If something breaks, the robot's working code on <code>master</code> is untouched.</p>

**2. Open `build.dependencies.gradle`.** It's in the top folder of the project, not inside `TeamCode`. If you can't see it, switch the dropdown at the top of the Project panel from **Android** to **Project**.

<p class="hub-why">This file is the project's shopping list of libraries.</p>

**3. Add the 3 lines marked NEW.** Change nothing else. When you're done, the file looks like this:

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 620 341" role="img" aria-label="The file build.dependencies.gradle after the change, with the three new lines highlighted"><rect x="2" y="2" width="616" height="337" rx="10" fill="#fff" stroke="#18181b" stroke-width="2"/><path d="M2 12a10 10 0 0 1 10-10h596a10 10 0 0 1 10 10v20H2z" fill="#f6f4f4"/><path d="M2 32h616" stroke="#18181b" stroke-width="1.5"/><text x="16" y="23" font-size="14" font-weight="800">build.dependencies.gradle</text><text x="604" y="23" text-anchor="end" font-size="12.5" fill="#5f5f66">top folder of the project</text><text x="20" y="52" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">repositories {</text><text x="20" y="73" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">    mavenCentral()</text><rect x="10" y="79" width="600" height="21" rx="4" fill="#fff4c2" stroke="#8a6d00" stroke-width="1.2"/><rect x="558" y="82" width="44" height="16" rx="8" fill="#8a6d00"/><text x="580" y="94.5" text-anchor="middle" font-size="11" font-weight="800" fill="#fff">NEW</text><text x="20" y="94" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" font-weight="700" xml:space="preserve">    maven { url &#x27;https://repo.dairy.foundation/releases/&#x27;}</text><text x="20" y="115" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">    google() // Needed for androidx</text><text x="20" y="136" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">}</text><text x="20" y="157" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve"></text><text x="20" y="178" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">dependencies {</text><text x="20" y="199" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">    implementation &#x27;org.firstinspires.ftc:Inspection:12.0.0&#x27;</text><text x="20" y="220" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#5f5f66" font-style="italic" xml:space="preserve">    ... 7 more of FIRST&#x27;s lines, unchanged ...</text><text x="20" y="241" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">    implementation &#x27;androidx.appcompat:appcompat:1.2.0&#x27;</text><rect x="10" y="247" width="600" height="21" rx="4" fill="#fff4c2" stroke="#8a6d00" stroke-width="1.2"/><rect x="558" y="250" width="44" height="16" rx="8" fill="#8a6d00"/><text x="580" y="262.5" text-anchor="middle" font-size="11" font-weight="800" fill="#fff">NEW</text><text x="20" y="262" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" font-weight="700" xml:space="preserve">    implementation &#x27;com.pedropathing:revhub:3.0.2&#x27;</text><rect x="10" y="268" width="600" height="21" rx="4" fill="#fff4c2" stroke="#8a6d00" stroke-width="1.2"/><rect x="558" y="271" width="44" height="16" rx="8" fill="#8a6d00"/><text x="580" y="283.5" text-anchor="middle" font-size="11" font-weight="800" fill="#fff">NEW</text><text x="20" y="283" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" font-weight="700" xml:space="preserve">    implementation &#x27;com.pedropathing:tuning:1.0.3&#x27;</text><text x="20" y="304" font-size="12.5" font-family="JetBrains Mono, Consolas, monospace" fill="#18181b" xml:space="preserve">}</text></svg><figcaption>The finished file. Only the 3 yellow lines are new.</figcaption></figure>

The 3 lines to copy:

```groovy
    maven { url 'https://repo.dairy.foundation/releases/'}
    implementation 'com.pedropathing:revhub:3.0.2'
    implementation 'com.pedropathing:tuning:1.0.3'
```

<p class="hub-why">The first line tells Android Studio which "store" to shop at. The other two say what to get: Pedro, and Pedro's tuning tool. You never copy Pedro's library code by hand.</p>

**4. Sync.** Click **Sync Now** if a blue bar appears. If it doesn't, click the elephant icon in the toolbar (**Sync Project with Gradle Files**).
**Check:** at the bottom of the Project panel, **External Libraries** now lists `com.pedropathing` entries.

<p class="hub-why">Syncing is when Android Studio actually downloads the libraries.</p>

**5. Build:** **Build > Assemble Project**, in the menu bar at the top of the screen. You should see **BUILD SUCCESSFUL**.
On Windows, the menu bar is hidden behind the ☰ icon at the top left of Android Studio.

## Part 2: copy the pedro folder

**6. Copy Pedro's `pedro` folder.**

1. Go to **github.com/Pedro-Pathing/Quickstart**, click the green **Code** button, then **Download ZIP**.
2. Open your **Downloads** folder in Finder. If you see a `.zip` file, double-click it to unzip it.
3. In the unzipped folder, open `TeamCode/src/main/java/org/firstinspires/ftc/teamcode`, click the `pedro` folder once and press **Command-C** to copy it.
4. In Android Studio, right-click your project's `teamcode` folder and choose **Open In > Finder**. Finder opens the folder that holds `teamcode`.
5. Open `teamcode` and press **Command-V** to paste the `pedro` folder next to your own code.

On Windows: use File Explorer, unzip with right-click > **Extract All**, copy and paste with Ctrl-C and Ctrl-V, and in Android Studio choose **Open In > Explorer**.

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 560 276" role="img" aria-label="Folder tree: the pedro folder goes inside teamcode, next to your team's own files, and holds Constants.java, Tuning.java and a procedures folder"><path d="M14 18h7l2 3h9v10h-18z" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="40" y="30" font-size="14" font-weight="600" fill="#18181b">TeamCode</text><path d="M28 38V55h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M44 48h7l2 3h9v10h-18z" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="70" y="60" font-size="14" font-weight="600" fill="#5f5f66">src &gt; main &gt; java &gt; org &gt; firstinspires &gt; ftc</text><path d="M58 68V85h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M74 78h7l2 3h9v10h-18z" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="100" y="90" font-size="14" font-weight="800" fill="#18181b">teamcode</text><path d="M88 98V115h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M106 107h10l4 4v12h-14z" fill="#fff" stroke="#5f5f66" stroke-width="1.5"/><text x="130" y="120" font-size="14" font-weight="600" fill="#5f5f66">your team&#x27;s own files (for example RobotHardware.java)</text><path d="M88 128V145h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><rect x="98" y="131" width="448" height="26" rx="6" fill="#fff4c2" stroke="#8a6d00" stroke-width="1.5"/><path d="M104 138h7l2 3h9v10h-18z" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="130" y="150" font-size="14" font-weight="800" fill="#18181b">pedro</text><text x="538" y="150" text-anchor="end" font-size="12.5" font-weight="800" fill="#8a6d00">copy this whole folder here</text><path d="M118 158V175h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M136 167h10l4 4v12h-14z" fill="#fff" stroke="#5f5f66" stroke-width="1.5"/><text x="160" y="180" font-size="14" font-weight="600" fill="#18181b">Constants.java</text><path d="M118 188V205h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M136 197h10l4 4v12h-14z" fill="#fff" stroke="#5f5f66" stroke-width="1.5"/><text x="160" y="210" font-size="14" font-weight="600" fill="#18181b">Tuning.java</text><path d="M118 218V235h12" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><path d="M134 228h7l2 3h9v10h-18z" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="160" y="240" font-size="14" font-weight="600" fill="#18181b">procedures</text></svg><figcaption>Where the pedro folder goes in your project.</figcaption></figure>

**Check:** `teamcode > pedro` has `Constants.java`, `Tuning.java` and a `procedures` folder (9 files in all).

<p class="hub-why">The exact place matters: every file in it starts with <code>package org.firstinspires.ftc.teamcode.pedro;</code>, and Java needs the folder to match that address. A ZIP, because GitHub has no button to download just one folder.</p>

**7. Build again.** It should still say **BUILD SUCCESSFUL**.

<p class="hub-why"><code>Constants.java</code> is almost empty, and that's fine. Its numbers describe one robot. Tuning on your robot fills them in.</p>

## Part 3: save it

**8. Commit and push the branch.** Merge it into `master` when your team is ready.

<div class="hub-trap"><b>Watch out</b><ul style="margin:6px 0 0;padding-left:20px"><li><b style="display:inline">Don't change any other build file.</b> Pedro's own starter project also changes a setting in two of FIRST's build files. Pedro 3 builds without that change. Changing FIRST's files causes conflicts when your repo takes FIRST's updates.</li><li><b style="display:inline">Never accept the "Android Gradle Plugin" upgrade</b> Android Studio offers (<a href="#/coding/laptop-setup?id=step-7-first-gradle-sync-and-never-accept-the-agp-upgrade">Setting up your laptop</a>, step 7).</li><li><b style="display:inline">Use the version numbers on this page.</b> Pedro's install page lists an older tuning version (1.0.0) than its own starter project uses (1.0.3).</li><li><b style="display:inline">Pedro 3 code only.</b> Most Pedro examples online are for version 2 and won't build.</li></ul></div>

<p style="font-size:14px;color:#5f5f66">Tested November 12, 2026: Pedro 3.0.2 and tuning 1.0.3 on FIRST's SDK 12.0, with Android Studio 2026.2.1 on Windows.</p>
