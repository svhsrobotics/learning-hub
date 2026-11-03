# Try the Virtual Robot

<p class="hub-lead">Drive a robot on the BIOBUZZ field on your laptop screen, with no robot needed. <b>Virtual Robot</b> is a free simulator made by FTC team 8397. It runs real FTC Java code.</p>

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(250px,1fr))">
<div class="hub-card" style="border-top:5px solid #2e7d32"><b>Good for</b>Practicing driving code, gamepad buttons, and autonomous steps like drive, turn and stop at a wall.</div>
<div class="hub-card" style="border-top:5px solid #A60012"><b>Not in it</b>No HIVE, no balls and no camera. For launching and aiming you still need the real robot.</div>
</div>

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 560 330"><rect x="4" y="4" width="552" height="322" rx="10" fill="#fff" stroke="#18181b" stroke-width="2"/><rect x="4" y="4" width="552" height="26" rx="10" fill="#f6f4f4" stroke="#18181b" stroke-width="2"/><text x="16" y="22" font-size="13" font-weight="700">Virtual Robot</text><rect x="14" y="44" width="92" height="186" rx="6" fill="#f6f4f4" stroke="#bdbdc2"/><text x="60" y="126" text-anchor="middle" font-size="12" fill="#5f5f66">field</text><text x="60" y="142" text-anchor="middle" font-size="12" fill="#5f5f66">settings</text><rect x="116" y="40" width="250" height="196" fill="#e6e6ea" stroke="#18181b" stroke-width="2"/><path d="M157.7 40v196M199.3 40v196M241 40v196M282.7 40v196M324.3 40v196M116 72.7h250M116 105.3h250M116 138h250M116 170.7h250M116 203.3h250" stroke="#c9c9cf" stroke-width="1"/><path d="M241 40v196" stroke="#5f5f66" stroke-dasharray="5 4"/><rect x="200" y="108" width="34" height="34" rx="3" fill="#f6c700" stroke="#18181b" stroke-width="2" transform="rotate(-20 217 125)"/><path d="M217 112v-14" stroke="#A60012" stroke-width="3" transform="rotate(-20 217 125)"/><text x="241" y="229" text-anchor="middle" font-size="12.5" font-weight="700" fill="#18181b">the BIOBUZZ field</text><rect x="378" y="44" width="166" height="26" rx="5" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="388" y="62" font-size="12.5">Mecanum Bot</text><path d="M528 54l5 6 5-6" fill="none" stroke="#18181b" stroke-width="1.5"/><rect x="378" y="78" width="166" height="26" rx="5" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="388" y="96" font-size="12.5">mecanum bot demo</text><path d="M528 88l5 6 5-6" fill="none" stroke="#18181b" stroke-width="1.5"/><rect x="420" y="112" width="82" height="26" rx="5" fill="#A60012"/><text x="461" y="130" text-anchor="middle" font-size="13" font-weight="800" fill="#fff">INIT</text><rect x="378" y="146" width="166" height="90" rx="5" fill="#fff" stroke="#bdbdc2"/><text x="388" y="166" font-size="12" font-family="monospace" fill="#5f5f66">Heading: 36.5</text><text x="388" y="184" font-size="12" font-family="monospace" fill="#5f5f66">Pose: x= -24 ...</text><rect x="116" y="248" width="56" height="56" rx="4" fill="#3a3a3f"/><circle cx="144" cy="276" r="7" fill="#e0312b"/><rect x="182" y="248" width="56" height="56" rx="4" fill="#3a3a3f"/><circle cx="210" cy="276" r="7" fill="#2e7d32"/><circle cx="276" cy="262" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="296" cy="282" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="256" cy="282" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="276" cy="300" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><g font-size="12.5" fill="#1f5fd1" font-weight="800"><text x="384" y="270">1. pick the robot</text><text x="384" y="288">2. pick the program</text><text x="384" y="306">3. INIT, then START</text></g><text x="320" y="320" text-anchor="end" font-size="12" fill="#5f5f66">on-screen gamepad</text></svg><figcaption>A simplified drawing of the simulator window. The real one has more settings, but these are the parts you use.</figcaption></figure>

## The steps at a glance

<div class="hub-grid">
<div class="hub-card"><b><span class="hub-pill">1</span>Get the simulator</b>Clone it in Android Studio</div>
<div class="hub-card"><b><span class="hub-pill">2</span>Get the right Java</b>The gamepad needs Liberica Full 17, exactly</div>
<div class="hub-card"><b><span class="hub-pill">3</span>Pick the Java</b>One setting in Project Structure</div>
<div class="hub-card"><b><span class="hub-pill">4</span>Set up the gamepad</b>Or skip it and use the on-screen one</div>
<div class="hub-card"><b><span class="hub-pill">5</span>Run and drive</b>The green arrow, then INIT and START</div>
</div>

## 1. Get the simulator

1. In Android Studio: **File > New > Project from Version Control**.
2. URL: `https://github.com/svhsrobotics/virtual_robot.git`
3. Directory: on Windows, `C:\FTC\virtual_robot`.
4. Click **Clone**, then **Trust Project**.

<p class="hub-why">Clone, don't download a ZIP, so you can get updates later with one click. On Windows, <code>C:\FTC\</code> is the same short folder your team's repo uses, which keeps OneDrive and long folder names out of the way (see <a href="#/coding/laptop-setup">Setting up your laptop</a>).</p>

This is the Saucon Valley program's own copy of the simulator. You can read it but not change it on GitHub, on purpose: everyone gets the same working version.

Android Studio may complain about a missing Java when the project opens. That's expected until you finish step 3.

## 2. Get the right Java

<div class="hub-trap" style="border:2px solid #A60012;background:#fbecee;font-size:17px"><b style="font-size:20px;color:#A60012">The gamepad will NOT work without this exact Java</b>On a Mac, a real gamepad only works with <b>Liberica Full JDK 17, x86</b>. All three of these must be true:<ol style="margin:6px 0 0;padding-left:22px"><li><b style="display:inline">Downloaded</b> from BellSoft's website, exactly as below. Not Android Studio's Download JDK.</li><li><b style="display:inline">Installed</b> from the DMG.</li><li><b style="display:inline">Picked</b> in Android Studio, in step 3.</li></ol></div>

The simulator needs a special Java: **Liberica JDK, the "Full" version, 17**. The simulator's author recommends it, and it's the one that worked on a student's MacBook with a real gamepad.

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 200"><rect x="8" y="10" width="200" height="140" rx="12" fill="#fbecee" stroke="#A60012" stroke-width="2.5"/><text x="108" y="38" text-anchor="middle" font-size="16" font-weight="800">Liberica Standard</text><rect x="38" y="54" width="140" height="34" rx="6" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="108" y="76" text-anchor="middle" font-size="14" font-weight="700">Java</text><text x="108" y="112" text-anchor="middle" font-size="14" fill="#5f5f66">no JavaFX</text><text x="108" y="136" text-anchor="middle" font-size="15" font-weight="800" fill="#A60012">won't build</text><rect x="232" y="10" width="200" height="140" rx="12" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2.5"/><text x="332" y="38" text-anchor="middle" font-size="16" font-weight="800">Liberica Full</text><rect x="262" y="54" width="140" height="34" rx="6" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="332" y="76" text-anchor="middle" font-size="14" font-weight="700">Java</text><rect x="262" y="94" width="140" height="30" rx="6" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="332" y="114" text-anchor="middle" font-size="14" font-weight="700" fill="#1f5fd1">+ JavaFX</text><text x="332" y="142" text-anchor="middle" font-size="15" font-weight="800" fill="#2e7d32">works</text><text x="220" y="184" text-anchor="middle" font-size="13.5" fill="#5f5f66">JavaFX is the library that draws the simulator's window.</text></svg><figcaption>Only the "Full" package has JavaFX. BellSoft's website starts on the Standard one, so watch out.</figcaption></figure>

### On a Mac

Always do this, even if you think you already have a Liberica. One you got another way may be the wrong one.

1. Go to **bell-sw.com** > Download > **JDK 17 LTS** tab.
2. In the **macOS** row, pick **x86**.
3. Change **Package** from Standard JDK to **Full JDK**.
4. Check the title. It must read **"Liberica Full JDK 17.0.21 ... x86 64 for macOS"**.
5. Download the **DMG** and install it.

<p class="hub-why">The simulator's gamepad part for Mac is built for Intel chips, and x86 is the version that worked with a real gamepad. Don't use Android Studio's Download JDK on a Mac: on a student's MacBook it installed Liberica Full 27, which crashes the simulator at start.</p>

### On Windows

Check first: with the simulator project open, go to **File > Project Structure > Project > SDK** and open the list. If it has a **Liberica Full 17 or 25** that is not marked `[Invalid]`, skip to step 3. If not, install one of these ways:

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(270px,1fr))">
<div class="hub-card" style="border-top:5px solid #8a6d00"><b>Inside Android Studio</b>In that same SDK list: <b>Download JDK</b>, vendor <b>BellSoft Liberica</b>, pick the <b>Full</b> (JavaFX) one, version <b>17 or 25</b>, then <b>Download</b>. Android Studio may offer a newer version first (like 27): don't pick it.<br><br>It saves into <code>C:\Users\&lt;you&gt;\.jdks</code> and needs no administrator rights.</div>
<div class="hub-card"><b>From the BellSoft website</b>Go to <b>bell-sw.com</b> &gt; Download &gt; <b>JDK 17 LTS</b>. Under <b>Windows, x86</b>, set <b>Package: Full JDK</b> and download the <b>MSI</b>.<br><br>In the installer you can untick "Add to PATH", "Setup JAVA_HOME", "Associate .jar files" and "JavaSoft registry". On a school laptop the MSI may need administrator rights, so ask a mentor.</div>
</div>

<p class="hub-why">Liberica Full 25 has also worked on Windows. Nothing newer works: the author couldn't get 21 working on Windows, and 27 built but crashed at start on a student's MacBook.</p>

## 3. Pick the Java

1. **File > Project Structure > Project**, and open the **SDK** list.
2. On a fresh clone it shows `<No Project SDK>` and `liberica-17 [Invalid]`. That's normal: `liberica-17` is only the name the project asks for, not a Java you have.
3. **SDK:** choose your Liberica Full 17 (or 25, if that's what you have on Windows). Not these: a newer Liberica like 27, `ms-17`, `jbr-...` or the Android API entries.
4. **On a Mac, if it isn't in the list:** **Add SDK > JDK**, then pick the Liberica 17 Full folder the installer made.
5. **Language level:** 17.
6. **Apply**, then **OK**.

<p class="hub-why">With the Standard Java picked, the build fails with errors that mention <code>javafx</code>. With a newer one like 27, it builds but crashes at start.</p>

<div class="hub-tip"><b>Your robot code is not affected</b>Android Studio keeps using its own built-in Java for your team's robot project. This setting belongs only to the simulator project. Don't change anything in the robot project.</div>

## 4. Set up the gamepad

No gamepad? Skip this step. The simulator then shows an on-screen gamepad.

1. Open `Controller/src/virtual_robot/config/Config.java` and set `USE_VIRTUAL_GAMEPAD = false`.
2. **Build > Rebuild Project**. If the simulator is open, close it first.
3. Set the switch on the back of the Logitech game controller:
   - **Mac: D.** In X, a Mac doesn't see the gamepad at all.
   - Windows: X. Device Manager then shows it as "Xbox 360 Controller for Windows", a quick way to see that the laptop found it.
   - The MODE light should be off.
4. Plug it in with a data cable (some cables only charge), **before** you start the simulator.

<p class="hub-why">Use Rebuild, not a quick build. Java copies a <code>final</code> setting into every file that uses it, and a quick build can leave old copies behind.</p>

If you clone the simulator again, the new copy has `USE_VIRTUAL_GAMEPAD = true`, so set it to `false` again.

## 5. Run and drive

1. At the top of Android Studio, pick **Main** and click the green **Run** arrow.
2. In the simulator window: configuration **Mecanum Bot**, OpMode **mecanum bot demo**.
3. Click the field to place the robot. Right-click to aim it.
4. With a real gamepad: press **START + A** on it.
5. Press **INIT**, then **START**, and drive.

<p class="hub-why">The buttons work just like the Driver Station: pick a program, INIT, START. So practice here feels the same as on the real robot.</p>

## Getting updates

When a mentor says the simulator was updated: open the simulator project and click **Git > Pull**.

## If something goes wrong

| You see | Likely cause | Fix |
|---|---|---|
| The SDK list shows `<No Project SDK>` and `liberica-17 [Invalid]` | Normal on a fresh clone: the project asks for a Java with that exact name | Pick your Liberica Full 17 or 25 entry (step 3), or install it (step 2) |
| Crash at start, with `LoadException` or `FXMLLoader` in the red text | A Java newer than 25 is picked (for example 27) | Pick Liberica Full 17 (or 25) in step 3, set the language level to 17, then Rebuild |
| Build errors mentioning `javafx` | The Standard Java is picked, not Full | Steps 2 and 3 |
| No green arrow next to **Main** | The project didn't open as the simulator | Reopen the `virtual_robot` folder |
| The window is too big for the screen | Small laptop screen | In `Config.java` set `FIELD_WIDTH = 576` and the picture to `biobuzz576.bmp`, then Rebuild |
| The gamepad does nothing | On a Mac, a Java other than Liberica Full 17 x86 is picked. Or the switch is on X. Or the simulator wasn't closed and rebuilt after changing the setting. Or START + A wasn't pressed | Steps 2 to 4. Press START + A |
