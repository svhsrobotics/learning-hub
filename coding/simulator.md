# Try the Simulator

<p class="hub-lead">Drive a robot on the BIOBUZZ field on your laptop screen, with no robot needed. <b>Virtual Robot</b> is a free simulator made by FTC team 8397. It runs real FTC Java code.</p>

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(250px,1fr))">
<div class="hub-card" style="border-top:5px solid #2e7d32"><b>Good for</b>Practicing driving code, gamepad buttons, and autonomous steps like drive, turn and stop at a wall.</div>
<div class="hub-card" style="border-top:5px solid #A60012"><b>Not in it</b>No HIVE, no balls and no camera. For launching and aiming you still need the real robot.</div>
</div>

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 560 330"><rect x="4" y="4" width="552" height="322" rx="10" fill="#fff" stroke="#18181b" stroke-width="2"/><rect x="4" y="4" width="552" height="26" rx="10" fill="#f6f4f4" stroke="#18181b" stroke-width="2"/><text x="16" y="22" font-size="13" font-weight="700">Virtual Robot</text><rect x="14" y="44" width="92" height="186" rx="6" fill="#f6f4f4" stroke="#bdbdc2"/><text x="60" y="126" text-anchor="middle" font-size="12" fill="#5f5f66">field</text><text x="60" y="142" text-anchor="middle" font-size="12" fill="#5f5f66">settings</text><rect x="116" y="40" width="250" height="196" fill="#e6e6ea" stroke="#18181b" stroke-width="2"/><path d="M157.7 40v196M199.3 40v196M241 40v196M282.7 40v196M324.3 40v196M116 72.7h250M116 105.3h250M116 138h250M116 170.7h250M116 203.3h250" stroke="#c9c9cf" stroke-width="1"/><path d="M241 40v196" stroke="#5f5f66" stroke-dasharray="5 4"/><rect x="200" y="108" width="34" height="34" rx="3" fill="#f6c700" stroke="#18181b" stroke-width="2" transform="rotate(-20 217 125)"/><path d="M217 112v-14" stroke="#A60012" stroke-width="3" transform="rotate(-20 217 125)"/><text x="241" y="229" text-anchor="middle" font-size="12.5" font-weight="700" fill="#18181b">the BIOBUZZ field</text><rect x="378" y="44" width="166" height="26" rx="5" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="388" y="62" font-size="12.5">Mecanum Bot</text><path d="M528 54l5 6 5-6" fill="none" stroke="#18181b" stroke-width="1.5"/><rect x="378" y="78" width="166" height="26" rx="5" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="388" y="96" font-size="12.5">mecanum bot demo</text><path d="M528 88l5 6 5-6" fill="none" stroke="#18181b" stroke-width="1.5"/><rect x="420" y="112" width="82" height="26" rx="5" fill="#A60012"/><text x="461" y="130" text-anchor="middle" font-size="13" font-weight="800" fill="#fff">INIT</text><rect x="378" y="146" width="166" height="90" rx="5" fill="#fff" stroke="#bdbdc2"/><text x="388" y="166" font-size="12" font-family="monospace" fill="#5f5f66">Heading: 36.5</text><text x="388" y="184" font-size="12" font-family="monospace" fill="#5f5f66">Pose: x= -24 ...</text><rect x="116" y="248" width="56" height="56" rx="4" fill="#3a3a3f"/><circle cx="144" cy="276" r="7" fill="#e0312b"/><rect x="182" y="248" width="56" height="56" rx="4" fill="#3a3a3f"/><circle cx="210" cy="276" r="7" fill="#2e7d32"/><circle cx="276" cy="262" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="296" cy="282" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="256" cy="282" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><circle cx="276" cy="300" r="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><g font-size="12.5" fill="#1f5fd1" font-weight="800"><text x="384" y="270">1. pick the robot</text><text x="384" y="288">2. pick the program</text><text x="384" y="306">3. INIT, then START</text></g><text x="320" y="320" text-anchor="end" font-size="12" fill="#5f5f66">on-screen gamepad</text></svg><figcaption>A simplified drawing of the simulator window. The real one has more settings, but these are the parts you use.</figcaption></figure>

## The steps at a glance

<div class="hub-grid">
<div class="hub-card"><b><span class="hub-pill">1</span>Get the simulator</b>Clone it into <code>C:\FTC\</code></div>
<div class="hub-card"><b><span class="hub-pill">2</span>Check your Java</b>It needs Liberica Full 17 or 25</div>
<div class="hub-card"><b><span class="hub-pill">3</span>Install it if missing</b>Two ways to get it</div>
<div class="hub-card"><b><span class="hub-pill">4</span>Pick the Java</b>One setting in Project Structure</div>
<div class="hub-card"><b><span class="hub-pill">5</span>Run and drive</b>The green arrow, then INIT and START</div>
<div class="hub-card"><b><span class="hub-pill">6</span>Real gamepad</b>Optional</div>
</div>

## 1. Get the simulator

1. In Android Studio: **File > New > Project from Version Control**.
2. URL: `https://github.com/svhsrobotics/virtual_robot.git`
3. Directory: `C:\FTC\virtual_robot`
4. Click **Clone**, then **Trust Project**.

<p class="hub-why">Clone, don't download a ZIP, so you can get updates later with one click. <code>C:\FTC\</code> is the same short folder your team's repo uses, which keeps OneDrive and long folder names out of the way (see <a href="#/coding/laptop-setup">Setting up your laptop</a>).</p>

This is the Saucon Valley program's own copy of the simulator. You can read it but not change it on GitHub, on purpose: everyone gets the same working version.

Android Studio may complain about a missing Java when the project opens. That's expected until you finish step 4.

## 2. Check your Java

The simulator needs a special Java: **Liberica JDK, the "Full" version, 17 or 25**. The simulator's author recommends Liberica Full 17. Liberica Full 25 has also worked on a mentor's laptop.

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 200"><rect x="8" y="10" width="200" height="140" rx="12" fill="#fbecee" stroke="#A60012" stroke-width="2.5"/><text x="108" y="38" text-anchor="middle" font-size="16" font-weight="800">Liberica Standard</text><rect x="38" y="54" width="140" height="34" rx="6" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="108" y="76" text-anchor="middle" font-size="14" font-weight="700">Java</text><text x="108" y="112" text-anchor="middle" font-size="14" fill="#5f5f66">no JavaFX</text><text x="108" y="136" text-anchor="middle" font-size="15" font-weight="800" fill="#A60012">won't build</text><rect x="232" y="10" width="200" height="140" rx="12" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2.5"/><text x="332" y="38" text-anchor="middle" font-size="16" font-weight="800">Liberica Full</text><rect x="262" y="54" width="140" height="34" rx="6" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="332" y="76" text-anchor="middle" font-size="14" font-weight="700">Java</text><rect x="262" y="94" width="140" height="30" rx="6" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="1.5"/><text x="332" y="114" text-anchor="middle" font-size="14" font-weight="700" fill="#1f5fd1">+ JavaFX</text><text x="332" y="142" text-anchor="middle" font-size="15" font-weight="800" fill="#2e7d32">works</text><text x="220" y="184" text-anchor="middle" font-size="13.5" fill="#5f5f66">JavaFX is the library that draws the simulator's window.</text></svg><figcaption>Only the "Full" package has JavaFX. The Standard one is the big download button on BellSoft's website, so watch out.</figcaption></figure>

**How to check:** with the simulator project open, go to **File > Project Structure > Project > SDK** and open the list.
- **Good:** a BellSoft Liberica Full entry that is not marked `[Invalid]`: `liberica-full-...` if Android Studio downloaded it, or the `LibericaJDK-17-Full` folder if you installed it from the website. Skip to step 4.
- **Normal on a fresh clone:** `<No Project SDK>` and `liberica-17 [Invalid]`. `liberica-17` is only the name the project asks for, not a Java you have.
- **Not these:** `ms-17`, `jbr-...` or the Android API entries. They have no JavaFX.
- **Not there:** do step 3.

You can also look on disk: `C:\Program Files\BellSoft\LibericaJDK-17-Full`, or a `liberica-full-...` folder in `C:\Users\<you>\.jdks`.

<p class="hub-why">With the wrong Java picked, the build fails with errors that mention <code>javafx</code>.</p>

<div class="hub-tip"><b>Your robot code is not affected</b>Android Studio keeps using its own built-in Java for your team's robot project. This setting belongs only to the simulator project. Don't change anything in the robot project.</div>

## 3. Install it if missing

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(270px,1fr))">
<div class="hub-card" style="border-top:5px solid #8a6d00"><b>A. Inside Android Studio (try this first)</b>In the same SDK list from step 2: <b>Download JDK</b>, vendor <b>BellSoft Liberica</b>, pick the <b>Full</b> (JavaFX) one, version <b>17 or 25</b>, then <b>Download</b>.<br><br>It saves into <code>C:\Users\&lt;you&gt;\.jdks</code> and needs no administrator rights. This is how a mentor's laptop got its Liberica Full 25.</div>
<div class="hub-card"><b>B. From the BellSoft website</b>Go to <b>bell-sw.com</b> &gt; Download &gt; <b>JDK 17 LTS</b>. Under <b>Windows, x86</b>, set <b>Package: Full JDK</b> and download the <b>MSI</b>.<br><br><b>Don't click the big black button:</b> that's the Standard package, without JavaFX.<br><br>In the installer you can untick "Add to PATH", "Setup JAVA_HOME", "Associate .jar files" and "JavaSoft registry". On a school laptop the MSI may need administrator rights, so ask a mentor.</div>
</div>

<p class="hub-why">The author recommends Liberica Full 17, and 25 has worked twice on a mentor's laptop. Pick one of those two: the author couldn't get version 21 working on Windows.</p>

## 4. Pick the Java

1. **File > Project Structure > Project**.
2. **SDK:** choose the Liberica one.
3. **Language level:** leave whatever Android Studio picks. 17 and 25 both work.
4. **Apply**, then **OK**.

## 5. Run and drive

1. At the top of Android Studio, pick **Main** and click the green **Run** arrow.
2. In the simulator window: configuration **Mecanum Bot**, OpMode **mecanum bot demo**.
3. Click the field to place the robot. Right-click to aim it.
4. Press **INIT**, then **START**, and drive with the on-screen gamepad.

<p class="hub-why">The buttons work just like the Driver Station: pick a program, INIT, START. So practice here feels the same as on the real robot.</p>

## 6. Real gamepad (optional)

1. Open `Controller/src/virtual_robot/config/Config.java` and set `USE_VIRTUAL_GAMEPAD = false`.
2. Close the simulator, then **Build > Rebuild Project**.
3. Run it again and press **START + A** on the gamepad.

<p class="hub-why">Use Rebuild, not a quick build. Java copies a <code>final</code> setting into every file that uses it, and a quick build can leave old copies behind.</p>

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(220px,1fr))">
<div class="hub-card"><b>Logitech</b>Set the switch to <b>X</b> (on the back of an F310, on top of an F710). The MODE light should be off.</div>
<div class="hub-card"><b>PlayStation</b>PS4 controllers should work (OPTIONS + Cross). PS5 may not.</div>
<div class="hub-card"><b>Cable</b>Use a data cable. Some cables only charge.</div>
</div>

## Getting updates

When a mentor says the simulator was updated: open the simulator project and click **Git > Pull**.

## If something goes wrong

| You see | Likely cause | Fix |
|---|---|---|
| The SDK list shows `<No Project SDK>` and `liberica-17 [Invalid]` | Normal on a fresh clone: the project asks for a Java with that exact name | Pick your Liberica Full entry (step 4), or install one (step 3) |
| Build errors mentioning `javafx` | The Standard Java is picked, not Full | Steps 3 and 4 |
| No green arrow next to **Main** | The project didn't open as the simulator | Reopen `C:\FTC\virtual_robot` |
| The window is too big for the screen | Small laptop screen | In `Config.java` set `FIELD_WIDTH = 576` and the picture to `biobuzz576.bmp`, then Rebuild |
| The gamepad does nothing | Simulator not rebuilt, or START + A not pressed | Step 6 |
