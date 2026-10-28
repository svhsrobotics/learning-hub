# Sample Robot & Code

**The short version:** most teams start by writing the whole robot in one big TeleOp file. That works. But as the robot grows, one file gets hard to fix and hard to share. The next step is to split the code into **objects**: one file per part of the robot (drivetrain, launcher, intake, camera), each with its own variables and methods. FTC teams call each of those part classes a **subsystem**.

> **When to read this:** when your team's TeleOp is getting long, or when you're about to copy your motor setup into an autonomous program. You don't need any of this to drive a robot on day one.

## Start with a pretend robot

<a class="hub-card" href="coding/sample-robot.html" style="display:flex;gap:14px;align-items:center;border-left:5px solid #A60012;max-width:640px"><svg viewBox="0 0 60 60" width="60" height="60" style="flex:0 0 60px"><rect x="12" y="10" width="36" height="40" rx="6" fill="#f6f4f4" stroke="#5f5f66" stroke-width="2"/><rect x="4" y="14" width="8" height="12" rx="2" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><rect x="48" y="14" width="8" height="12" rx="2" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><rect x="4" y="34" width="8" height="12" rx="2" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><rect x="48" y="34" width="8" height="12" rx="2" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><rect x="16" y="5" width="28" height="7" rx="3.5" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2"/><circle cx="30" cy="38" r="7" fill="#fbecee" stroke="#A60012" stroke-width="2"/></svg><span><b style="display:block;font-size:17px;margin-bottom:2px">Open the sample robot</b>A pretend robot, seen from above. Tap a part (drive, intake, launcher, camera) to see its Java file, then open the TeleOp to see one program use them all.</span></a>

<p class="hub-why">One class per part means each file is short, each part can be tested and fixed on its own, and two students can work on different parts at the same time.</p>

<div class="hub-tip"><b>Then see it with real code</b><a href="#/coding/one-file-to-objects">Last season's code in parts</a> takes each team's real TeleOp from last season and splits it into parts like these.</div>

## The words

These are the same ideas as [Classes and objects](coding/java-basics.md) in Java basics, with robot parts.

| Word | What it means | Example |
|---|---|---|
| **Class** | A blueprint, written once in its own file | `Launcher.java` |
| **Object** | One real thing built from the blueprint with `new` | `new Launcher()` inside the robot's own class |
| **Variables ("has")** | What the object owns and remembers | its motors, its target speed, whether it's on |
| **Methods ("can do")** | What you can ask the object to do | `turnOn()`, `turnOff()`, `isAtSpeed()` |
| **Subsystem** | The class for one part of the robot | `Launcher`, `Intake`, `Drivetrain` |

Think of a sports team. The TeleOp is the **coach** calling plays: "shoot!" The launcher is the **player** who knows how to shoot. The coach doesn't explain how to hold the ball every time. If the shots are off, you work with the shooter, not the whole team.

**Moves that use several parts** (like "load a ball", which runs the intake and then a feeder in order, or "center on the tag", which uses the camera and the drivetrain) go one level up, in the robot's own class. Each part still only knows its own job.

## Why split the code up?
- **One place to look.** A launcher problem means opening the launcher file, about 50 lines, instead of searching a 300-line file.
- **Autonomous reuses it.** AUTO calls the same `turnOn()` and `isAtSpeed()` that TeleOp uses. Without objects, that code gets copied into every program, and the copies slowly stop matching.
- **Students can split the work.** One student owns the launcher file, another owns the drivetrain, and they don't edit the same lines at the same time. That also means fewer Git conflicts.
- **The names explain the code.** `robot.feeder.openGate()` says what it does. `gateServo.setPosition(servoshootpos)` makes you go look.

**Why not start this way?** Splitting code up only makes sense once you've felt the problem it fixes. Writing one file first teaches you what the robot needs. Then you'll know which parts deserve their own files.
