# Your First OpMode

<p class="hub-lead">An <b>OpMode</b> is one robot program. Every one has the same shape: <b>get ready</b>, <b>wait for START</b>, then <b>loop</b> until STOP. New to words like "variable" and "if"? Read <a href="#/coding/java-basics">Java basics</a> first.</p>

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 460 250" role="img" aria-label="An OpMode's life: INIT gets ready without moving, waits for START, loops sense think act many times a second, and stops the motors after STOP"><defs><marker id="op-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto"><path d="M0 0L10 5L0 10z" fill="#5f5f66"/></marker></defs><rect x="4" y="40" width="96" height="92" rx="12" fill="#fff7d6" stroke="#8a6d00" stroke-width="2"/><text x="52" y="30" text-anchor="middle" font-size="14" font-weight="800">INIT</text><text x="52" y="66" text-anchor="middle" font-size="12">set up the</text><text x="52" y="82" text-anchor="middle" font-size="12">motors</text><text x="52" y="108" text-anchor="middle" font-size="12" font-weight="800" fill="#A60012">nothing</text><text x="52" y="124" text-anchor="middle" font-size="12" font-weight="800" fill="#A60012">moves!</text><path d="M100 86h16" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#op-arrow)"/><rect x="120" y="58" width="62" height="56" rx="10" fill="#f6f4f4" stroke="#5f5f66" stroke-width="1.5"/><text x="151" y="82" text-anchor="middle" font-size="12" font-weight="700">wait for</text><text x="151" y="98" text-anchor="middle" font-size="12" font-weight="700">START</text><path d="M182 86h14" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#op-arrow)"/><circle cx="270" cy="86" r="70" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><text x="270" y="10" text-anchor="middle" font-size="14" font-weight="800">LOOP</text><circle cx="270" cy="38" r="22" fill="#fff" stroke="#1f5fd1" stroke-width="2"/><text x="270" y="42" text-anchor="middle" font-size="12" font-weight="800">sense</text><circle cx="312" cy="112" r="22" fill="#fff" stroke="#1f5fd1" stroke-width="2"/><text x="312" y="116" text-anchor="middle" font-size="12" font-weight="800">think</text><circle cx="228" cy="112" r="22" fill="#fff" stroke="#1f5fd1" stroke-width="2"/><text x="228" y="116" text-anchor="middle" font-size="12" font-weight="800">act</text><path d="M290 50 Q312 70 314 88" fill="none" stroke="#1f5fd1" stroke-width="2" marker-end="url(#op-arrow)"/><path d="M290 122 Q270 136 252 122" fill="none" stroke="#1f5fd1" stroke-width="2" marker-end="url(#op-arrow)"/><path d="M226 88 Q228 68 250 50" fill="none" stroke="#1f5fd1" stroke-width="2" marker-end="url(#op-arrow)"/><text x="270" y="175" text-anchor="middle" font-size="12" font-weight="700" fill="#1f5fd1">many times a second</text><path d="M340 86h24" stroke="#5f5f66" stroke-width="1.5" marker-end="url(#op-arrow)"/><text x="353" y="104" text-anchor="middle" font-size="11" font-weight="700" fill="#5f5f66">STOP</text><rect x="368" y="40" width="88" height="92" rx="12" fill="#fbecee" stroke="#A60012" stroke-width="2"/><text x="412" y="30" text-anchor="middle" font-size="14" font-weight="800">AFTER</text><text x="412" y="80" text-anchor="middle" font-size="12">stop the</text><text x="412" y="96" text-anchor="middle" font-size="12">motors</text><rect x="20" y="198" width="420" height="44" rx="10" fill="#fff" stroke="#bdbdc2"/><text x="230" y="216" text-anchor="middle" font-size="12.5"><tspan font-weight="800">sense:</tspan> read the gamepad and sensors.  <tspan font-weight="800">think:</tspan> decide.</text><text x="230" y="234" text-anchor="middle" font-size="12.5"><tspan font-weight="800">act:</tspan> set the motors. Then do it all again.</text></svg><figcaption>Like riding a bike: look, decide, steer, over and over. You don't plan the whole ride with your eyes closed.</figcaption></figure>

## The program

This example drives forward and back with the left stick, and goes half speed while A is held. It would go in `TeamCode/src/main/java/org/firstinspires/ftc/teamcode/opmodes/MyFirstTeleOp.java` and uses a shared hardware class called `RobotHardware` that your team writes, with a `drive()` and a `stopDrive()` method. FIRST's sample `externalhardware/RobotHardware.java` shows how to start one (see [From laptop to robot](coding/laptop-to-robot.md)).

```java
package org.firstinspires.ftc.teamcode.opmodes;   // which folder this file lives in

import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;   // FIRST's OpMode blueprint
import com.qualcomm.robotcore.eventloop.opmode.TeleOp;         // the @TeleOp label

import org.firstinspires.ftc.teamcode.RobotHardware;           // your team's shared hardware class

// This label puts the program in the Driver Station's TeleOp list.
// The name must be different from every other OpMode's name.
@TeleOp(name = "My First TeleOp", group = "Practice")
public class MyFirstTeleOp extends LinearOpMode {

    // A tuning number. Change it here, and only here.
    static final double HALF_SPEED = 0.5;

    @Override
    public void runOpMode() {
        // ----- INIT: set up, but DON'T MOVE ANYTHING (rule G304) -----
        RobotHardware robot = new RobotHardware(this);   // build your team's robot object
        robot.init();                                    // find all the motors by name

        telemetry.addData("Status", "Ready. Press START.");
        telemetry.update();                              // actually send the message

        // ----- WAIT here until the driver presses START -----
        waitForStart();

        // ----- LOOP: runs many times per second until STOP -----
        while (opModeIsActive()) {

            // SENSE: read the left stick. Pushing UP gives a NEGATIVE number,
            // so we flip the sign to make "up" mean "forward".
            double forward = -gamepad1.left_stick_y;

            // THINK: if A is held, slow down.
            if (gamepad1.a) {
                forward = forward * HALF_SPEED;
            }

            // ACT: drive forward or back, no sliding sideways, no turning.
            robot.drive(forward, 0, 0);

            // SHOW: what the robot is "thinking", on the Driver Station screen.
            telemetry.addData("Forward power", forward);
            telemetry.addData("Half speed?", gamepad1.a);
            telemetry.update();
        }

        // ----- AFTER STOP: make sure everything stops -----
        robot.stopDrive();
    }
}
```

### The lines that matter most

| Line | What it does | Why |
|---|---|---|
| `@TeleOp(name = "...")` | Puts the program in the Driver Station's TeleOp list | Without it, the program doesn't show up. Use `@Autonomous` for auto programs |
| `extends LinearOpMode` | "My program is a LinearOpMode, plus my own part" | FIRST's blueprint already knows how to talk to the Driver Station |
| `new RobotHardware(this)` then `robot.init()` | Builds the robot object and finds every motor by name | A wrong name shows up here, not halfway through a match |
| `telemetry.update()` | Sends the messages to the Driver Station | Nothing appears until you call it |
| `waitForStart();` | Pauses until START | INIT and START are separate moments in a match |
| `while (opModeIsActive())` | Loops until STOP or the match timer ends | This is the sense, think, act loop |
| `robot.drive(...)` | Asks the hardware class to drive | The OpMode decides **what** to do; the hardware class knows **how** |
| `robot.stopDrive();` | Stops the motors after the loop | Nothing may move after the match ends (G404) |

### Why the minus sign on the stick?

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 150" role="img" aria-label="Pushing the stick up reads minus one, pulling it down reads plus one, so the code flips the sign"><circle cx="80" cy="75" r="56" fill="#f6f4f4" stroke="#18181b" stroke-width="2"/><circle cx="80" cy="37" r="20" fill="#3a3a3f"/><path d="M80 75V45" stroke="#3a3a3f" stroke-width="6"/><path d="M146 70V30M139 38l7-8 7 8" fill="none" stroke="#2e7d32" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/><text x="80" y="146" text-anchor="middle" font-size="12" fill="#5f5f66">pushed up</text><text x="190" y="62" text-anchor="middle" font-size="13" fill="#5f5f66">FTC reads</text><text x="190" y="90" text-anchor="middle" font-size="24" font-weight="800" fill="#A60012">-1.0</text><path d="M232 78h40M264 70l8 8-8 8" fill="none" stroke="#18181b" stroke-width="2"/><text x="252" y="64" text-anchor="middle" font-size="12" font-family="monospace">-y</text><text x="350" y="62" text-anchor="middle" font-size="13" fill="#5f5f66">your code uses</text><text x="350" y="90" text-anchor="middle" font-size="24" font-weight="800" fill="#2e7d32">+1.0</text><text x="350" y="112" text-anchor="middle" font-size="12.5" font-weight="700">= forward</text></svg><figcaption>FTC gamepads report "up" as a negative number. Everyone trips on this once.</figcaption></figure>

## Try it (predict first!)

<div class="hub-trap"><b>Safety first, every time you run new code</b>Put the robot on a stand so its wheels are off the floor the first time, tell people nearby, and keep a finger near STOP. New code does surprising things.</div>

1. Change `HALF_SPEED` to `0.2`. **Predict** what holding A will feel like, then try it.
2. Add a telemetry line that shows `gamepad1.left_stick_x`. Predict what it shows when you push the stick right.
3. Make the B button go at full speed even when A is held. Which `if` has to come last? Why?

<div class="hub-tip"><b>Starting from one of FIRST's samples?</b>Copy it into <code>TeamCode</code> and rename the copy (for example <code>MyNameTeleOp</code>). Then check four things or it won't work: the <code>package</code> line at the top says <code>org.firstinspires.ftc.teamcode</code> (plus a folder name if you put it in one, like <code>.opmodes</code>), the class name matches the file name, the name in <code>@TeleOp(name = "...")</code> is different from every other OpMode, and the <code>@Disabled</code> line is gone.</div>

<div class="hub-tip"><b>Using code you found online?</b>Learn from it, but understand every line before it goes on your team's robot (the "explain it back" rule), check that it works with Java 8, and never add FTC Dashboard to competition code. If you copy a file, add a comment saying where it came from.</div>

## Two rules for every robot program

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
<div class="hub-card" style="border-top:5px solid #1f5fd1"><b>1. Every loop checks <code>opModeIsActive()</code></b>It turns false when someone presses STOP or the match timer runs out. Without it, the robot keeps going and STOP doesn't work: a safety problem and a rules problem.</div>
<div class="hub-card" style="border-top:5px solid #A60012"><b>2. Don't <code>sleep()</code> when a sensor can tell you</b>A sleep freezes the program: no gamepad, no sensors, no STOP. A sleep <b>guesses</b> how long something takes; a sensor <b>knows</b>.</div>
</div>

So instead of "drive for 2 seconds and hope you're at the wall", say "drive until the distance sensor says 12 inches". And because sensors can fail, add a **timeout** too. Every autonomous loop checks all three:

<div class="hub-grid">
<div class="hub-card"><b><span class="hub-pill">1</span>Still running?</b><code>opModeIsActive()</code>, so STOP works</div>
<div class="hub-card"><b><span class="hub-pill">2</span>Not too long?</b>Under 5 seconds, so a broken sensor can't drive forever</div>
<div class="hub-card"><b><span class="hub-pill">3</span>Not there yet?</b>The wall is more than 12 inches away</div>
</div>

```java
// Same idea as FIRST's sample RobotAutoDriveToLine_Linear.java, which drives until a
// color sensor sees a line. Real code first checks that robot.frontDistance isn't null
// (see "null" in Java basics).
ElapsedTime timer = new ElapsedTime();   // a stopwatch that starts now

while (opModeIsActive()                                   // 1. STOP still works
        && timer.seconds() < 5.0                          // 2. give up after 5 seconds
        && robot.frontDistance.getDistance(DistanceUnit.INCH) > 12.0) {   // 3. not at the wall yet
    robot.drive(0.4, 0, 0);   // forward, slowly
}
robot.stopDrive();
```

<div class="hub-trap"><b>Watch out: a loop missing one of the three</b>It's an easy mistake, and the robot can keep driving for the whole autonomous period.</div>

## Check yourself

<div class="hub-quiz">
<details><summary>What are the three parts of every OpMode?</summary><div>Get ready (INIT, nothing moves), wait for START, then loop until STOP. After the loop, stop the motors.</div></details>
<details><summary>Why is -gamepad1.left_stick_y negative?</summary><div>FTC gamepads report pushing the stick up as a negative number. The minus sign flips it so "up" means forward.</div></details>
<details><summary>What happens if you forget telemetry.update()?</summary><div>Nothing shows on the Driver Station. The messages are only sent when you call <code>update()</code>.</div></details>
<details><summary>Name the three things every autonomous loop checks.</summary><div><code>opModeIsActive()</code>, a timeout, and the real condition you're waiting for (like the distance to the wall).</div></details>
<details><summary>Why is a sensor better than sleep()?</summary><div>A sleep guesses how long something takes and freezes the program while it waits. A sensor knows when you're there, and the loop keeps checking STOP the whole time.</div></details>
</div>
