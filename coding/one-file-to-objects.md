# Last Season's Code, Rebuilt in Parts

<p class="hub-lead">We took each team's real TeleOp from last season and rebuilt it in modules: one Java file for each part of the robot, plus one TeleOp that tells the parts what to do. Same robot, same buttons, same numbers. Only where the code lives changed, and that makes it easier to read, fix and reuse.</p>

**Pick your team** to see last season's file next to the rebuilt one:

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(250px,1fr))">
<a class="hub-card" href="coding/code-map.html#gamma" style="border-top:5px solid #A60012"><svg viewBox="0 0 120 70" width="120" height="70" style="display:block;margin:2px 0 8px" aria-hidden="true"><rect x="2" y="4" width="22" height="62" rx="3" fill="#f6f4f4" stroke="#5f5f66"/><rect x="5" y="8" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="15" width="16" height="4" fill="#c99700"/><rect x="5" y="21" width="16" height="6" fill="#7a4fc0"/><rect x="5" y="29" width="16" height="4" fill="#c99700"/><rect x="5" y="35" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="42" width="16" height="7" fill="#c99700"/><rect x="5" y="51" width="16" height="4" fill="#7a4fc0"/><rect x="5" y="57" width="16" height="5" fill="#1f5fd1"/><path d="M26 20 C50 20 50 12 70 12 M26 35 C50 35 50 35 70 35 M26 50 C50 50 50 58 70 58" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><rect x="72" y="4" width="44" height="16" rx="3" fill="#e9f0fc" stroke="#1f5fd1"/><rect x="72" y="27" width="44" height="16" rx="3" fill="#fff7d6" stroke="#c99700"/><rect x="72" y="50" width="44" height="16" rx="3" fill="#ece4fa" stroke="#7a4fc0"/></svg><b>Gamma</b><code>BobComp.java</code>: 321 lines in one file, rebuilt as <b>6 files</b>: BobRobot, Drivetrain, Launcher, Intake, Aimer and BobTeleOp.</a>
<a class="hub-card" href="coding/code-map.html#psi" style="border-top:5px solid #A60012"><svg viewBox="0 0 120 70" width="120" height="70" style="display:block;margin:2px 0 8px" aria-hidden="true"><rect x="2" y="4" width="22" height="62" rx="3" fill="#f6f4f4" stroke="#5f5f66"/><rect x="5" y="8" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="15" width="16" height="4" fill="#c99700"/><rect x="5" y="21" width="16" height="6" fill="#7a4fc0"/><rect x="5" y="29" width="16" height="4" fill="#c99700"/><rect x="5" y="35" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="42" width="16" height="7" fill="#c99700"/><rect x="5" y="51" width="16" height="4" fill="#7a4fc0"/><rect x="5" y="57" width="16" height="5" fill="#1f5fd1"/><path d="M26 20 C50 20 50 12 70 12 M26 35 C50 35 50 35 70 35 M26 50 C50 50 50 58 70 58" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><rect x="72" y="4" width="44" height="16" rx="3" fill="#e9f0fc" stroke="#1f5fd1"/><rect x="72" y="27" width="44" height="16" rx="3" fill="#fff7d6" stroke="#c99700"/><rect x="72" y="50" width="44" height="16" rx="3" fill="#ece4fa" stroke="#7a4fc0"/></svg><b>Psi</b><code>FINALTELEOPREFACTOR.java</code>: 365 lines in one file, rebuilt as <b>9 files</b>: PsiRobot, Drivetrain, Launcher, Intake, Feeder, Lights, Camera, PsiTeleOp and a button helper.</a>
<a class="hub-card" href="coding/code-map.html#robotica" style="border-top:5px solid #A60012"><svg viewBox="0 0 120 70" width="120" height="70" style="display:block;margin:2px 0 8px" aria-hidden="true"><rect x="2" y="4" width="22" height="62" rx="3" fill="#f6f4f4" stroke="#5f5f66"/><rect x="5" y="8" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="15" width="16" height="4" fill="#c99700"/><rect x="5" y="21" width="16" height="6" fill="#7a4fc0"/><rect x="5" y="29" width="16" height="4" fill="#c99700"/><rect x="5" y="35" width="16" height="5" fill="#1f5fd1"/><rect x="5" y="42" width="16" height="7" fill="#c99700"/><rect x="5" y="51" width="16" height="4" fill="#7a4fc0"/><rect x="5" y="57" width="16" height="5" fill="#1f5fd1"/><path d="M26 20 C50 20 50 12 70 12 M26 35 C50 35 50 35 70 35 M26 50 C50 50 50 58 70 58" fill="none" stroke="#bdbdc2" stroke-width="1.5"/><rect x="72" y="4" width="44" height="16" rx="3" fill="#e9f0fc" stroke="#1f5fd1"/><rect x="72" y="27" width="44" height="16" rx="3" fill="#fff7d6" stroke="#c99700"/><rect x="72" y="50" width="44" height="16" rx="3" fill="#ece4fa" stroke="#7a4fc0"/></svg><b>Robotica</b><code>DecodeTestTeleOp.java</code>: 361 lines in one file, rebuilt as <b>6 files</b>: RoboticaRobot, Drivetrain, Launcher, Intake, Aimer and RoboticaTeleOp.</a>
</div>

<p class="hub-why">One big file mixes every part of the robot together, so fixing the launcher means hunting through 300+ lines. With one file per part, each fix happens in one place, and an autonomous program can reuse the same parts instead of copying the code.</p>

New to the idea of splitting code into parts? Start with [Sample robot & code](coding/sample-robot-code.md).

## How the map works

The map fills the whole window. To come back here, click **Robotics Learning Hub** at its top left, or use your browser's Back button.

**It opens in a simple view.** On the **left**, the team's whole TeleOp is one tall bar: each colored stripe is a chunk of code, colored by the part of the robot it controls. On the **right**, one box per new file, showing only its main methods. Lines join each stripe to the box its code moved to.

| To do this | Do this |
|---|---|
| See a method's old and new code | Click it in a box. A panel shows the old lines next to the new code. |
| See one chunk of the old file | Click a stripe |
| See which stripes went into a box | Point at the box |
| Switch teams | Click **Gamma**, **Psi** or **Robotica** at the top |
| See every line and every method | Click **Show every line**. You can drag, zoom, rearrange the boxes and highlight one part. **Back to the simple view** returns. |

## Try these
Each one takes a minute or two. Say your answer out loud before you check.

1. **Predict, then check.** Before you look closely: how many separate places in the big file do you think touch the launcher? Now count the yellow stripes in the bar.
2. **Follow one method.**
   - *Gamma:* click `isAtSpeed()` in the Launcher box. Which lines did it come from? Why would an autonomous program want to use this method instead of waiting a fixed number of seconds?
   - *Psi:* click `shoot()` in the PsiRobot box, then look at lines 286 and 287 in the old file. Which flywheel motor gets set twice, and which one never gets set? Now open `turnOnFull()` in the Launcher box: the same mistake is there, on purpose. What one-word change fixes it, and why is it easier to fix now that it lives in one method?
   - *Robotica:* click `toggleCamera()` in the Aimer box and trace lines 254 to 259 one step at a time. What really happens when you press D-pad up?
3. **Find the code nobody used.** Click **Not carried over**. Why is it safe to delete code that nothing calls? (Hint: what does Git keep?)
4. **Read the TeleOp box.** Click its button map. Notice that TeleOp still decides which button does what, but it no longer knows *how* the launcher spins up. Why is that a good split?
5. **Compare the teams.** Switch between the three teams. Why does Psi end up with Feeder and Lights boxes when Gamma and Robotica don't? And why do Gamma's pushers and Robotica's triggers both live in the Launcher box? What decides which boxes a robot needs?

## Things to know about the examples
- All three files are real code from last season's robots, used here with thanks. A real file teaches more than a made-up one.
- The boxes show **real code**: for each team, files that compile and do what last season's TeleOp did, but they haven't been run on a robot yet. Each team's oddities are kept on purpose and marked, so you can find them (the "look closely" questions point at them). Psi's background timer and Robotica's centering loop, which could freeze or crash the program, were fixed. Treat the code as a pattern to follow, not something to copy and paste.
- Psi saved several versions of its TeleOp last season. The map uses the newest one. Keeping one file and using Git to remember old versions is easier than keeping copies with "FINAL" in the name. See [Git and GitHub](coding/git-and-github.md).
- Last season's AprilTag numbers (20 and 24) don't apply this season. BIOBUZZ uses tags 30 to 45. See "AprilTags on the HIVE" on the [Overview: Field and Rules](overview.md) page.

## Your turn
Talk these over with your team. There's no single right answer.
- BIOBUZZ lets a robot control **at most 4 game pieces** at once (rule G407). If your robot counts the balls it's holding, which object should do the counting? What methods would it need?
- Your robot might not have a camera. Which box would disappear, and what would TeleOp do instead?
- Pick one part of **your** robot. What would its box say under "Has" and "Can do"?
