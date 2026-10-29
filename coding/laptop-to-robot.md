# From Laptop to Robot

<p class="hub-lead">Your team's code lives in one folder, <code>TeamCode</code>. Android Studio builds it together with FIRST's code into one app, installs that app on the robot's <b>Control Hub</b>, and the <b>Driver Station</b> tells it when to run.</p>

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 460 312" role="img" aria-label="The laptop builds FtcRobotController and TeamCode into one app, installs it on the Control Hub, which runs motors and sensors and talks to the Driver Station over Wi-Fi"><defs><marker id="trip-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M0 0L10 5L0 10z" fill="#5f5f66"/></marker></defs><rect x="4" y="30" width="136" height="176" rx="12" fill="#fff" stroke="#18181b" stroke-width="2"/><text x="72" y="22" text-anchor="middle" font-size="14" font-weight="800">Your laptop</text><rect x="12" y="44" width="120" height="52" rx="8" fill="#f6f4f4" stroke="#5f5f66" stroke-width="1.5"/><text x="72" y="66" text-anchor="middle" font-size="11.5" font-weight="800">FtcRobotController</text><text x="72" y="84" text-anchor="middle" font-size="12" fill="#5f5f66">FIRST's: don't edit</text><rect x="12" y="104" width="120" height="52" rx="8" fill="#fbecee" stroke="#A60012" stroke-width="2"/><text x="72" y="126" text-anchor="middle" font-size="13" font-weight="800">TeamCode</text><text x="72" y="144" text-anchor="middle" font-size="12" fill="#A60012" font-weight="700">yours: work here</text><text x="72" y="176" text-anchor="middle" font-size="12" fill="#5f5f66">Build: both become</text><text x="72" y="192" text-anchor="middle" font-size="12" fill="#5f5f66">one app</text><path d="M142 118h34" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#trip-arrow)"/><text x="159" y="108" text-anchor="middle" font-size="12" font-weight="700">Run</text><rect x="180" y="30" width="112" height="176" rx="12" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2"/><text x="236" y="22" text-anchor="middle" font-size="14" font-weight="800">Control Hub</text><text x="236" y="80" text-anchor="middle" font-size="13" font-weight="800" fill="#2e7d32">runs your</text><text x="236" y="98" text-anchor="middle" font-size="13" font-weight="800" fill="#2e7d32">code</text><text x="236" y="132" text-anchor="middle" font-size="12" fill="#5f5f66">finds hardware</text><text x="236" y="148" text-anchor="middle" font-size="12" fill="#5f5f66">by its</text><text x="236" y="164" text-anchor="middle" font-size="12" fill="#5f5f66">configuration</text><text x="236" y="180" text-anchor="middle" font-size="12" fill="#5f5f66">names</text><path d="M296 118h34" stroke="#5f5f66" stroke-width="1.5" marker-start="url(#trip-arrow)" marker-end="url(#trip-arrow)"/><text x="313" y="108" text-anchor="middle" font-size="12" font-weight="700">Wi-Fi</text><rect x="334" y="30" width="122" height="176" rx="12" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><text x="395" y="22" text-anchor="middle" font-size="14" font-weight="800">Driver Station</text><text x="395" y="62" text-anchor="middle" font-size="12">picks the OpMode</text><text x="395" y="82" text-anchor="middle" font-size="12">INIT, START, STOP</text><text x="395" y="102" text-anchor="middle" font-size="12">gamepads plug in</text><text x="395" y="122" text-anchor="middle" font-size="12">shows telemetry</text><text x="395" y="164" text-anchor="middle" font-size="12" font-weight="800" fill="#1f5fd1">a remote control:</text><text x="395" y="182" text-anchor="middle" font-size="12" font-weight="800" fill="#1f5fd1">no code runs here</text><path d="M236 206v28" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#trip-arrow)"/><rect x="146" y="238" width="180" height="40" rx="10" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="236" y="263" text-anchor="middle" font-size="13" font-weight="700">motors, servos, sensors</text><text x="230" y="304" text-anchor="middle" font-size="12" fill="#5f5f66">After installing, you can close the laptop. The robot keeps your code.</text></svg><figcaption>The whole trip, from the laptop to the robot.</figcaption></figure>

## The two folders that matter

The robot project has a lot of folders. Almost all of them are FIRST's. Only two matter to you:

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
<div class="hub-card" style="border-top:5px solid #5f5f66"><b>FtcRobotController: don't edit</b>FIRST's code that talks to motors, gamepads and the Driver Station. It also holds more than 60 example programs (the samples).</div>
<div class="hub-card" style="border-top:5px solid #A60012"><b>TeamCode: work here</b>Your team's OpModes and its one shared hardware class. Java files go in <code>TeamCode/src/main/java/org/firstinspires/ftc/teamcode/</code>.</div>
</div>

<p class="hub-why">FIRST sends updates during the season. If its folder is untouched, an update drops in cleanly. If your team changed FIRST's files, you'd get merge conflicts, maybe the night before a competition.</p>

**That path is long** because it's the Java **package** name (`org.firstinspires.ftc.teamcode`) written as folders. A package is like a full mailing address, so two files called `RobotHardware.java` can't get mixed up. In Android Studio's "Android" view it collapses into one line.

**The other files** (`build.gradle` and friends) are the build recipe. Leave them alone. The one exception: the lead programmer adds extra libraries, like Road Runner, in `TeamCode/build.gradle`. And never accept Android Studio's offer to upgrade the "Android Gradle Plugin" (see [laptop setup](coding/laptop-setup.md#step-7-first-gradle-sync-and-never-accept-the-agp-upgrade)).

### What's in TeamCode at the start

Only a readme from FIRST. We don't add files of our own: your team starts by copying one of FIRST's samples, the way FIRST's readme in that folder says to.

<p class="hub-why">FIRST updates its samples with every new SDK, and they're what you'll find in FTC Docs, videos and other teams' code. So what you learn matches the help you find.</p>

### Use FIRST's samples

<div class="hub-tip"><b>Copy, rename, change the copy</b>Copy a sample into <code>TeamCode</code>, rename it, and remove the <code>@Disabled</code> line so it shows up on the Driver Station. Never edit the original.</div>

| You want to | Start from |
|---|---|
| Drive a mecanum robot with a gamepad (day one) | `BasicOmniOpMode_Linear.java` |
| Drive a robot with one motor per side (tank) | `RobotTeleopPOV_Linear.java` or `RobotTeleopTank_Iterative.java` |
| See the bare skeleton of an OpMode | `BasicOpMode_Linear.java` |
| Do something once per button press | `ConceptGamepadEdgeDetection.java` |
| Drive a set distance in AUTO, with a timeout on every move | `RobotAutoDriveByEncoder_Linear.java` |
| Drive until a sensor sees something | `RobotAutoDriveToLine_Linear.java` |
| Set up every motor in one shared hardware class | `externalhardware/RobotHardware.java`, used by `ConceptExternalHardwareClass.java` |
| See AprilTags with a camera | `ConceptAprilTagEasy.java` |

They're in `FtcRobotController > java > org.firstinspires.ftc.robotcontroller > external.samples` in the "Android" view.

<p class="hub-why">When your team starts writing autonomous, move the motor setup into one shared hardware class. Then motor names and directions live in exactly one file: fix it once and every OpMode gets the fix. See it on <a href="#/coding/sample-robot-code">Sample robot &amp; code</a>.</p>

<div class="hub-trap"><b>Watch out: FIRST's hardware class moves servos at INIT</b>Its <code>init()</code> sets the hand servos to a starting position. In your copy, move those lines out of <code>init()</code> and set servos after START. If INIT moves anything, your drivers can't press INIT during the 8 second pause before TELEOP; they must wait until TELEOP begins (G403).</div>

## The trip, step by step

<div class="hub-grid">
<div class="hub-card"><b><span class="hub-pill">1</span>Edit</b>Change <code>.java</code> files in <code>TeamCode</code>.</div>
<div class="hub-card"><b><span class="hub-pill">2</span>Build</b>Gradle turns FIRST's code and yours into one app. A typo stops the build and names the line.</div>
<div class="hub-card"><b><span class="hub-pill">3</span>Install</b>The green <b>Run</b> arrow sends the app to the Control Hub over Wi-Fi or USB.</div>
<div class="hub-card"><b><span class="hub-pill">4</span>Configure</b>The Control Hub's saved list of what's plugged in where, with names.</div>
<div class="hub-card"><b><span class="hub-pill">5</span>Run</b>On the Driver Station: pick an OpMode, INIT, then START.</div>
</div>

<p class="hub-why">The build catches typos before they reach the robot. It can't catch a wrong number, which is why you still test.</p>

## Names, not ports

Code never says "the motor on port 0". It asks for a name, and the configuration on the Control Hub says where that name is plugged in. Like a seating chart.

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 130"><rect x="4" y="30" width="130" height="56" rx="10" fill="#fbecee" stroke="#A60012" stroke-width="2"/><text x="69" y="52" text-anchor="middle" font-size="12.5" font-weight="800">Your code asks for</text><text x="69" y="72" text-anchor="middle" font-size="12" font-family="monospace">front_left_motor</text><path d="M134 58h22" stroke="#5f5f66" stroke-width="1.5"/><path d="M150 52l8 6-8 6" fill="none" stroke="#5f5f66" stroke-width="1.5"/><rect x="160" y="30" width="130" height="56" rx="10" fill="#fff7d6" stroke="#8a6d00" stroke-width="2"/><text x="225" y="52" text-anchor="middle" font-size="12.5" font-weight="800">Configuration</text><text x="225" y="72" text-anchor="middle" font-size="12">says: motor port 0</text><path d="M290 58h22" stroke="#5f5f66" stroke-width="1.5"/><path d="M306 52l8 6-8 6" fill="none" stroke="#5f5f66" stroke-width="1.5"/><rect x="316" y="30" width="120" height="56" rx="10" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2"/><text x="376" y="52" text-anchor="middle" font-size="12.5" font-weight="800">Control Hub</text><text x="376" y="72" text-anchor="middle" font-size="12">port 0: the motor</text><text x="220" y="118" text-anchor="middle" font-size="12.5" fill="#5f5f66">Move a wire? Change one line in the configuration, not the code.</text></svg><figcaption>The configuration is made on the Driver Station and saved on the Control Hub.</figcaption></figure>

<div class="hub-trap"><b>Watch out: names must match exactly</b>Capital letters and underscores count. If the code asks for <code>front_left_motor</code> and the configuration says <code>frontLeft</code>, the OpMode stops at INIT with an error naming the missing device. FIRST's samples use their own names (like <code>front_left_drive</code>), so change them in your copy.</div>

Your team picks its device names once, uses the same spelling in the configuration and in the code, and writes the list down. Ask your code captain for it.

## The Driver Station buttons

| Button | What the code does |
|---|---|
| Pick an OpMode | Nothing yet. You've chosen which program |
| **INIT** | The code starts: it finds hardware and gets ready. **Nothing may move** (G304) |
| **START** | The main loop runs: read gamepad and sensors, decide, set motors, many times per second |
| **STOP** | The loop ends and the robot stops |

In a match, a 30 second timer ends AUTO on its own, and TELEOP lasts 2:00. Between them is an 8 second pause where nothing may move (G403).

<div class="hub-trap"><b>Watch out: "I changed it but nothing happened"</b>The robot still has the old code until you press <b>Run</b> and the install finishes. Then pick the OpMode again.</div>

<div class="hub-trap"><b>Watch out: "My OpMode doesn't show up"</b>Check, in this order: did the install finish after you pressed Run? Is it marked <code>@Disabled</code>? Is the <code>@TeleOp</code> or <code>@Autonomous</code> label there? Is its name unique? Are you looking in the right list (TeleOp or Autonomous)?</div>

## Telemetry: the robot talking back

Your code can show text on the Driver Station screen. It's your window into what the robot is "thinking".

```java
telemetry.addData("Battery", "%.2f V", robot.getBatteryVoltage());
telemetry.update();   // nothing shows until you call update()
```

In matches, the Driver Station screen is the **only** allowed place for this. FTC Dashboard and other tools that stream over Wi-Fi are banned during matches (R704.D).
