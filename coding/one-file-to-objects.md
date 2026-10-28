# Last Season's Code in Parts

<p class="hub-lead">Last season, each of our three teams wrote its whole TeleOp in one big file. Here is each one rewritten in parts: the same robot, the same buttons, the same numbers, but one file per part of the robot.</p>

New to the idea of splitting code into parts? Start with [Sample robot & code](coding/sample-robot-code.md).

## The code maps
There's one map per team: Gamma, Psi and Robotica. Each shows that team's real TeleOp from last season (DECODE). You can switch teams at the top of the map.

<p>
<a href="coding/code-map.html#gamma" style="display:inline-block;background:#A60012;color:#fff;font-weight:700;padding:10px 18px;border-radius:6px;text-decoration:none;margin:0 8px 8px 0">Gamma's code map</a>
<a href="coding/code-map.html#psi" style="display:inline-block;background:#A60012;color:#fff;font-weight:700;padding:10px 18px;border-radius:6px;text-decoration:none;margin:0 8px 8px 0">Psi's code map</a>
<a href="coding/code-map.html#robotica" style="display:inline-block;background:#A60012;color:#fff;font-weight:700;padding:10px 18px;border-radius:6px;text-decoration:none;margin:0 8px 8px 0">Robotica's code map</a>
</p>

| Team | File | What the robot had |
|---|---|---|
| Gamma | `BobComp.java`, 321 lines | Mecanum drive, two flywheels, pusher servos, camera aiming |
| Psi | `FINALTELEOPREFACTOR.java`, 365 lines | Tank drive, two flywheels, a gate, a silo, LED lights, a camera |
| Robotica | `DecodeTestTeleOp.java`, 361 lines | Mecanum drive, a small and a big flywheel, two trigger servos, a camera that can center on a tag |

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
- Last season's AprilTag numbers (20 and 24) don't apply this season. BIOBUZZ uses tags 30 to 45. See "AprilTags on the HIVE" on the [BIOBUZZ 2026-27 Overview](/) page.

## Your turn
Talk these over with your team. There's no single right answer.
- BIOBUZZ lets a robot control **at most 4 game pieces** at once (rule G407). If your robot counts the balls it's holding, which object should do the counting? What methods would it need?
- Your robot might not have a camera. Which box would disappear, and what would TeleOp do instead?
- Pick one part of **your** robot. What would its box say under "Has" and "Can do"?
