# Java Basics for FTC

<p class="hub-lead">Robot code is built from five building blocks. Learn these and you can read most of our robot code. Tap one to jump to it.</p>

<div class="hub-tip"><b>Never coded before?</b>That's normal here. Lots of students start with zero experience, and robot code is built from a handful of ideas you'll practice on a real robot.</div>

<div class="hub-grid">
<a class="hub-card" href="#/coding/java-basics?id=variables-labeled-boxes"><span class="hub-pic"><svg viewBox="0 0 120 80"><path d="M22 28l-10-12M98 28l10-12" stroke="#A60012" stroke-width="3" stroke-linecap="round"/><rect x="22" y="28" width="76" height="46" rx="4" fill="#fbecee" stroke="#A60012" stroke-width="3"/><rect x="30" y="35" width="60" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="46.5" text-anchor="middle" font-size="11" font-family="monospace">speed</text><text x="60" y="68" text-anchor="middle" font-size="15" font-weight="800">0.7</text></svg></span><b>Variables</b>Labeled boxes that hold a value</a>
<a class="hub-card" href="#/coding/java-basics?id=if-else-decisions"><span class="hub-pic"><svg viewBox="0 0 120 80" fill="none" stroke-linecap="round" stroke-linejoin="round"><path d="M60 76V44" stroke="#18181b" stroke-width="4"/><path d="M60 44L28 14M60 44l32-30" stroke="#18181b" stroke-width="4"/><path d="M28 14l2 10M28 14l10 1" stroke="#2e7d32" stroke-width="4"/><path d="M92 14l-2 10M92 14l-10 1" stroke="#A60012" stroke-width="4"/><text x="18" y="44" font-size="13" font-weight="800" fill="#2e7d32" stroke="none">yes</text><text x="86" y="44" font-size="13" font-weight="800" fill="#A60012" stroke="none">no</text></svg></span><b>if / else</b>Make a decision</a>
<a class="hub-card" href="#/coding/java-basics?id=loops-repeat"><span class="hub-pic"><svg viewBox="0 0 120 80" fill="none" stroke-linecap="round"><path d="M86 40a26 26 0 1 1-8-19" stroke="#1f5fd1" stroke-width="5"/><path d="M80 8l-1 14-14-2" stroke="#1f5fd1" stroke-width="5" stroke-linejoin="round"/><text x="60" y="46" text-anchor="middle" font-size="14" font-weight="800" fill="#1f5fd1" stroke="none">again</text></svg></span><b>Loops</b>Do it again and again</a>
<a class="hub-card" href="#/coding/java-basics?id=methods-named-actions"><span class="hub-pic"><svg viewBox="0 0 120 80"><rect x="14" y="20" width="92" height="40" rx="20" fill="#f6c700" stroke="#8a6d00" stroke-width="3"/><text x="60" y="45" text-anchor="middle" font-size="13" font-weight="800" font-family="monospace">drive()</text></svg></span><b>Methods</b>A named action you can reuse</a>
<a class="hub-card" href="#/coding/java-basics?id=objects-vending-machines"><span class="hub-pic"><svg viewBox="0 0 120 80"><rect x="34" y="6" width="52" height="70" rx="5" fill="#fff" stroke="#18181b" stroke-width="3"/><rect x="40" y="12" width="28" height="36" rx="2" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2"/><circle cx="54" cy="30" r="9" fill="none" stroke="#1f5fd1" stroke-width="2.5"/><circle cx="77" cy="18" r="4" fill="#A60012"/><circle cx="77" cy="30" r="4" fill="#A60012"/><circle cx="77" cy="42" r="4" fill="#A60012"/><rect x="42" y="58" width="36" height="10" rx="2" fill="#f6f4f4" stroke="#18181b" stroke-width="1.5"/></svg></span><b>Objects</b>Machines with buttons, built from a blueprint</a>
</div>

## Code is exact instructions

The robot does exactly what you wrote, not what you meant. Say "drive forward" without "stop" and it won't stop. Java is also picky:

<div class="hub-grid">
<div class="hub-card"><b style="font-size:28px;font-family:var(--mono);color:#A60012">;</b>Every statement ends with a semicolon.</div>
<div class="hub-card"><b style="font-size:28px;font-family:var(--mono);color:#A60012">{ }</b>Curly braces are the covers of a block, like a book.</div>
<div class="hub-card"><b style="font-size:28px;color:#A60012">Aa</b><code>Robot</code> and <code>robot</code> are different names.</div>
<div class="hub-card"><b style="font-size:28px;font-family:var(--mono);color:#A60012">//</b>Starts a comment: a note for humans. The computer skips it.</div>
</div>

## Variables: labeled boxes

A variable is a box with a label. It holds one value at a time. The first word (the **type**) says what can go in the box.

<div class="hub-grid">
<div class="hub-card"><span class="hub-pic"><svg viewBox="0 0 120 80"><path d="M22 28l-10-12M98 28l10-12" stroke="#1f5fd1" stroke-width="3" stroke-linecap="round"/><rect x="22" y="28" width="76" height="46" rx="4" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="3"/><rect x="28" y="35" width="64" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="46.5" text-anchor="middle" font-size="10.5" font-family="monospace">ballsHeld</text><text x="60" y="68" text-anchor="middle" font-size="16" font-weight="800">2</text></svg></span><b>int</b>Whole numbers<br><code>int ballsHeld = 2;</code></div>
<div class="hub-card"><span class="hub-pic"><svg viewBox="0 0 120 80"><path d="M22 28l-10-12M98 28l10-12" stroke="#A60012" stroke-width="3" stroke-linecap="round"/><rect x="22" y="28" width="76" height="46" rx="4" fill="#fbecee" stroke="#A60012" stroke-width="3"/><rect x="28" y="35" width="64" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="46.5" text-anchor="middle" font-size="10.5" font-family="monospace">speed</text><text x="60" y="68" text-anchor="middle" font-size="16" font-weight="800">0.7</text></svg></span><b>double</b>Decimals<br><code>double speed = 0.7;</code></div>
<div class="hub-card"><span class="hub-pic"><svg viewBox="0 0 120 80"><path d="M22 28l-10-12M98 28l10-12" stroke="#2e7d32" stroke-width="3" stroke-linecap="round"/><rect x="22" y="28" width="76" height="46" rx="4" fill="#e8f5e9" stroke="#2e7d32" stroke-width="3"/><rect x="28" y="35" width="64" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="46.5" text-anchor="middle" font-size="10.5" font-family="monospace">slowMode</text><text x="60" y="68" text-anchor="middle" font-size="15" font-weight="800">false</text></svg></span><b>boolean</b>Only <code>true</code> or <code>false</code><br><code>boolean slowMode = false;</code></div>
<div class="hub-card"><span class="hub-pic"><svg viewBox="0 0 120 80"><path d="M22 28l-10-12M98 28l10-12" stroke="#8a6d00" stroke-width="3" stroke-linecap="round"/><rect x="22" y="28" width="76" height="46" rx="4" fill="#fff7d6" stroke="#8a6d00" stroke-width="3"/><rect x="28" y="35" width="64" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="46.5" text-anchor="middle" font-size="10.5" font-family="monospace">alliance</text><text x="60" y="68" text-anchor="middle" font-size="15" font-weight="800">"red"</text></svg></span><b>String</b>Text, in double quotes<br><code>String alliance = "red";</code></div>
<div class="hub-card"><span class="hub-pic"><svg viewBox="0 0 120 80"><rect x="22" y="22" width="76" height="52" rx="4" fill="#ececee" stroke="#5f5f66" stroke-width="3"/><path d="M22 34h76" stroke="#5f5f66" stroke-width="3"/><rect x="24" y="40" width="72" height="14" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="60" y="50" text-anchor="middle" font-size="7.4" font-family="monospace">SLOW_MODE_SCALE</text><text x="60" y="68" text-anchor="middle" font-size="14" font-weight="800">0.4</text><rect x="51" y="6" width="18" height="14" rx="2" fill="#5f5f66"/><path d="M54 6V2a6 6 0 0 1 12 0v4" fill="none" stroke="#5f5f66" stroke-width="2.5"/></svg></span><b>Constant</b>A sealed box: can't change<br><code>static final double SLOW_MODE_SCALE = 0.4;</code></div>
</div>

```java
double speed = 0.7;     // make a box called "speed" and put 0.7 in it
speed = 0.4;            // put a new value in the same box
```

<p class="hub-why">Constants give a tuning number one home and a name. <code>0.4</code> alone means nothing; <code>SLOW_MODE_SCALE</code> explains itself.</p>

<div class="hub-trap"><b>Watch out: whole number division</b>Dividing two whole numbers throws the fraction away. <code>300 / 537</code> gives <b>0</b>, not 0.56, and the motor doesn't move. Write a <code>.0</code> on one number: <code>300.0 / 537</code>.</div>

## Putting in vs. asking

One equal sign **puts** a value in a box. Two equal signs **ask** a question. Mixing them up is the most common beginner bug.

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
<div class="hub-card"><span class="hub-pic" style="height:110px"><svg viewBox="0 0 200 110"><rect x="62" y="56" width="76" height="46" rx="4" fill="#fbecee" stroke="#A60012" stroke-width="3"/><rect x="70" y="63" width="60" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="100" y="74.5" text-anchor="middle" font-size="11" font-family="monospace">speed</text><circle cx="100" cy="18" r="14" fill="#f6c700" stroke="#8a6d00" stroke-width="2"/><text x="100" y="23" text-anchor="middle" font-size="12" font-weight="800">0.5</text><path d="M100 34v16M93 44l7 7 7-7" fill="none" stroke="#18181b" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/></svg></span><b><code>speed = 0.5;</code></b>Puts 0.5 in the box.</div>
<div class="hub-card"><span class="hub-pic" style="height:110px"><svg viewBox="0 0 200 110"><rect x="20" y="40" width="76" height="46" rx="4" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="3"/><rect x="26" y="47" width="64" height="15" rx="3" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="58" y="58.5" text-anchor="middle" font-size="10.5" font-family="monospace">ballsHeld</text><text x="58" y="80" text-anchor="middle" font-size="16" font-weight="800">2</text><text x="122" y="70" text-anchor="middle" font-size="22" font-weight="800">=</text><text x="122" y="56" text-anchor="middle" font-size="22" font-weight="800">=</text><text x="160" y="72" text-anchor="middle" font-size="26" font-weight="800">4</text><text x="122" y="28" text-anchor="middle" font-size="26" font-weight="800" fill="#A60012">?</text><text x="160" y="102" text-anchor="middle" font-size="14" font-weight="800" fill="#A60012">false</text></svg></span><b><code>ballsHeld == 4</code></b>Asks "is it 4?" The answer is true or false.</div>
</div>

| Symbol | Means | Example |
|---|---|---|
| `+ - * /` | Add, subtract, multiply, divide | `forward * 0.5` |
| `!=` | Not equal | `ballsHeld != 0` |
| `> < >= <=` | Bigger, smaller, and so on | `distance < 12` |
| `&&` | AND: both must be true | `a && b` |
| `\|\|` | OR: at least one is true | `a \|\| b` |
| `!` | NOT: flips true and false | `!slowMode` |

<div class="hub-trap"><b>Watch out: mixing && and ||</b>Java does <code>&&</code> first, which surprises people. Use parentheses to say what you mean: <code>if ((gamepad1.a || gamepad1.b) && !intakeFull)</code></div>

## if / else: decisions

"If it's raining, take an umbrella, else wear sunglasses." The robot checks a question and takes one path.

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 210"><rect x="140" y="6" width="160" height="34" rx="8" fill="#f6f4f4" stroke="#18181b" stroke-width="2"/><text x="220" y="28" text-anchor="middle" font-size="15" font-weight="700">every loop</text><path d="M220 40v14" stroke="#18181b" stroke-width="2.5"/><path d="M220 54l80 34-80 34-80-34z" fill="#fff7d6" stroke="#8a6d00" stroke-width="2.5"/><text x="220" y="85" text-anchor="middle" font-size="14.5" font-weight="800">right bumper</text><text x="220" y="102" text-anchor="middle" font-size="14.5" font-weight="800">held?</text><path d="M140 88H70v58" fill="none" stroke="#2e7d32" stroke-width="3"/><path d="M63 138l7 10 7-10" fill="none" stroke="#2e7d32" stroke-width="3" stroke-linejoin="round"/><text x="100" y="80" text-anchor="middle" font-size="15" font-weight="800" fill="#2e7d32">yes</text><path d="M300 88h70v58" fill="none" stroke="#A60012" stroke-width="3"/><path d="M363 138l7 10 7-10" fill="none" stroke="#A60012" stroke-width="3" stroke-linejoin="round"/><text x="340" y="80" text-anchor="middle" font-size="15" font-weight="800" fill="#A60012">no</text><rect x="6" y="152" width="128" height="50" rx="10" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2.5"/><text x="70" y="174" text-anchor="middle" font-size="14" font-family="monospace" font-weight="700">speed = 0.3</text><text x="70" y="193" text-anchor="middle" font-size="13.5" fill="#5f5f66">slow, careful</text><rect x="306" y="152" width="128" height="50" rx="10" fill="#fbecee" stroke="#A60012" stroke-width="2.5"/><text x="370" y="174" text-anchor="middle" font-size="14" font-family="monospace" font-weight="700">speed = 1.0</text><text x="370" y="193" text-anchor="middle" font-size="13.5" fill="#5f5f66">full speed</text></svg><figcaption>Slow mode: hold the right bumper to drive slowly.</figcaption></figure>

```java
if (gamepad1.right_bumper) {
    speed = 0.3;          // bumper held: slow
} else {
    speed = 1.0;          // otherwise: full speed
}
```

**More than two choices?** Chain them with `else if`. Java checks from the top and runs **only the first** one that's true.

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 520 150"><rect x="8" y="30" width="14" height="80" fill="#5f5f66"/><text x="15" y="130" text-anchor="middle" font-size="13" fill="#5f5f66">wall</text><rect x="22" y="56" width="90" height="28" fill="#fbecee" stroke="#A60012" stroke-width="2"/><rect x="112" y="56" width="90" height="28" fill="#fff7d6" stroke="#8a6d00" stroke-width="2"/><rect x="202" y="56" width="230" height="28" fill="#e8f5e9" stroke="#2e7d32" stroke-width="2"/><text x="67" y="75" text-anchor="middle" font-size="14" font-weight="800" fill="#A60012">stop</text><text x="157" y="75" text-anchor="middle" font-size="14" font-weight="800" fill="#8a6d00">creep</text><text x="317" y="75" text-anchor="middle" font-size="14" font-weight="800" fill="#2e7d32">normal speed</text><text x="30" y="104" text-anchor="middle" font-size="13">0</text><text x="112" y="104" text-anchor="middle" font-size="13">6 in</text><text x="202" y="104" text-anchor="middle" font-size="13">12 in</text><text x="67" y="44" text-anchor="middle" font-size="12.5" font-family="monospace">distance &lt; 6</text><text x="157" y="44" text-anchor="middle" font-size="12.5" font-family="monospace">&lt; 12</text><text x="317" y="44" text-anchor="middle" font-size="12.5" font-family="monospace">else</text><rect x="446" y="46" width="60" height="48" rx="6" fill="#fff" stroke="#18181b" stroke-width="2.5"/><circle cx="458" cy="98" r="7" fill="#18181b"/><circle cx="494" cy="98" r="7" fill="#18181b"/><path d="M440 70h-24M424 62l-8 8 8 8" fill="none" stroke="#18181b" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/><text x="476" y="74" text-anchor="middle" font-size="12" font-weight="700">robot</text></svg><figcaption>Driving toward a wall: the closer it gets, the slower it goes.</figcaption></figure>

```java
if (distance < 6) {
    robot.stopDrive();            // too close: stop
} else if (distance < 12) {
    robot.drive(0.2, 0, 0);       // getting close: creep
} else {
    robot.drive(0.5, 0, 0);       // far away: normal speed
}
```

<p class="hub-why">When two separate <code>if</code>s set the same box, the last one wins. So the order of your <code>if</code>s is a design decision.</p>

## Loops: repeat

A `while` loop repeats as long as its question is true, like a song on repeat until someone presses Stop. A TeleOp runs its loop many times every second.

<figure class="hub-fig"><svg class="hub-svg narrow" viewBox="0 0 440 290"><rect x="100" y="6" width="240" height="52" rx="10" fill="#f6f4f4" stroke="#18181b" stroke-width="2"/><text x="220" y="27" text-anchor="middle" font-size="14.5" font-weight="800">Before the loop: runs once</text><text x="220" y="47" text-anchor="middle" font-size="13.5" font-family="monospace">int loopCount = 0;</text><path d="M220 58v20M213 70l7 8 7-8" fill="none" stroke="#18181b" stroke-width="2.5" stroke-linejoin="round"/><circle cx="220" cy="158" r="74" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="3"/><path d="M280 114a74 74 0 0 1 14 34" fill="none" stroke="#1f5fd1" stroke-width="6" stroke-linecap="round"/><path d="M286 146l8 12 8-13" fill="none" stroke="#1f5fd1" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/><text x="220" y="132" text-anchor="middle" font-size="14.5" font-weight="800" fill="#1f5fd1">Inside: runs again</text><text x="220" y="150" text-anchor="middle" font-size="14.5" font-weight="800" fill="#1f5fd1">and again</text><text x="220" y="176" text-anchor="middle" font-size="13" font-family="monospace">loopCount =</text><text x="220" y="194" text-anchor="middle" font-size="13" font-family="monospace">loopCount + 1;</text><path d="M294 158h60" stroke="#A60012" stroke-width="2.5"/><text x="390" y="150" text-anchor="middle" font-size="13.5" font-weight="800" fill="#A60012">Stop</text><text x="390" y="167" text-anchor="middle" font-size="13.5" font-weight="800" fill="#A60012">pressed?</text><text x="390" y="184" text-anchor="middle" font-size="12.5" fill="#5f5f66">leave the loop</text><text x="60" y="140" text-anchor="middle" font-size="13" fill="#5f5f66">counts</text><text x="60" y="160" text-anchor="middle" font-size="18" font-weight="800">1, 2, 3...</text><path d="M220 232v12" stroke="#1f5fd1" stroke-width="2.5"/><text x="328" y="262" font-size="12.5" fill="#5f5f66">asked before</text><text x="328" y="278" font-size="12.5" fill="#5f5f66">every round</text><rect x="120" y="244" width="200" height="40" rx="10" fill="#fff" stroke="#18181b" stroke-width="2"/><text x="220" y="269" text-anchor="middle" font-size="13.5" font-family="monospace">while (opModeIsActive())</text></svg><figcaption>The box at the top runs once. Everything inside the circle runs every loop.</figcaption></figure>

```java
int loopCount = 0;                  // before: made once
while (opModeIsActive()) {
    loopCount = loopCount + 1;      // inside: goes up every loop
}
```

<div class="hub-trap"><b>Watch out: the counter that never counts</b>Put <code>int loopCount = 0;</code> <i>inside</i> the loop and it's emptied back to 0 every time, so it never gets past 1. Real teams make this bug.</div>

<div class="hub-trap"><b>Watch out: a stray semicolon</b><code>while (opModeIsActive());</code> with a <code>;</code> at the end is an empty loop. The robot ignores everything after it until someone presses Stop.</div>

## Methods: named actions

A method is a named set of steps you can use again and again, like a recipe card called "make toast". Some methods just **do** something. Others **hand back an answer**.

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
<div class="hub-card"><span class="hub-pic" style="height:96px"><svg viewBox="0 0 220 96"><rect x="6" y="28" width="104" height="40" rx="20" fill="#f6c700" stroke="#8a6d00" stroke-width="2.5"/><text x="58" y="53" text-anchor="middle" font-size="12" font-weight="800" font-family="monospace">driveSlowly()</text><path d="M116 48h28M136 40l8 8-8 8" fill="none" stroke="#18181b" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/><rect x="152" y="24" width="56" height="44" rx="6" fill="#fff" stroke="#18181b" stroke-width="2.5"/><circle cx="164" cy="72" r="7" fill="#18181b"/><circle cx="196" cy="72" r="7" fill="#18181b"/><path d="M160 16h40" stroke="#2e7d32" stroke-width="3" stroke-dasharray="6 5"/></svg></span><b>Does something: <code>void</code></b>Press it and the robot acts. Nothing comes back.</div>
<div class="hub-card"><span class="hub-pic" style="height:96px"><svg viewBox="0 0 220 96"><rect x="6" y="28" width="116" height="40" rx="20" fill="#f6c700" stroke="#8a6d00" stroke-width="2.5"/><text x="64" y="53" text-anchor="middle" font-size="12" font-weight="800" font-family="monospace">inchesToWall()</text><path d="M128 40h40M160 32l8 8-8 8" fill="none" stroke="#18181b" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/><path d="M168 60h-40M136 52l-8 8 8 8" fill="none" stroke="#1f5fd1" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/><rect x="172" y="30" width="40" height="36" rx="6" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2.5"/><text x="192" y="53" text-anchor="middle" font-size="13" font-weight="800" fill="#1f5fd1">14.2</text></svg></span><b>Hands back an answer: <code>double</code></b>Ask it, and a value comes back to use.</div>
</div>

```java
robot.drive(0.5, 0, 0);                     // call "drive" with three numbers
double volts = robot.getBatteryVoltage();   // this one hands back an answer

public void driveSlowly() {                 // "void": does something, hands back nothing
    drive(0.2, 0, 0);
}

public double inchesToWall() {              // "double": hands back a decimal
    return frontDistance.getDistance(DistanceUnit.INCH);
}
```

## Objects: vending machines

A **class** is a blueprint. An **object** is one real thing built from it, with `new`. Think of each robot part (the launcher, the intake) as a **vending machine**.

<figure class="hub-fig"><svg class="hub-svg" viewBox="0 0 560 300"><rect x="10" y="60" width="120" height="150" rx="4" fill="#e9f0fc" stroke="#1f5fd1" stroke-width="2.5"/><path d="M22 84h96M22 104h70M22 124h86M22 144h60" stroke="#1f5fd1" stroke-width="2" stroke-dasharray="5 4"/><rect x="40" y="160" width="60" height="38" rx="3" fill="none" stroke="#1f5fd1" stroke-width="2"/><text x="70" y="44" text-anchor="middle" font-size="15" font-weight="800" fill="#1f5fd1">class Launcher</text><text x="70" y="232" text-anchor="middle" font-size="13.5" fill="#5f5f66">the blueprint</text><path d="M140 135h56M186 125l10 10-10 10" fill="none" stroke="#18181b" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/><text x="166" y="122" text-anchor="middle" font-size="15" font-weight="800" font-family="monospace">new</text><rect x="210" y="20" width="230" height="270" rx="12" fill="#fff" stroke="#18181b" stroke-width="3"/><text x="325" y="12" text-anchor="middle" font-size="14" font-weight="800">one launcher object</text><rect x="224" y="36" width="130" height="170" rx="6" fill="#f6f4f4" stroke="#5f5f66" stroke-width="2"/><text x="289" y="56" text-anchor="middle" font-size="12.5" font-weight="800" fill="#5f5f66">PRIVATE: inside</text><circle cx="289" cy="104" r="30" fill="#fff" stroke="#18181b" stroke-width="3"/><circle cx="289" cy="104" r="6" fill="#18181b"/><path d="M289 74v60M259 104h60" stroke="#18181b" stroke-width="1.5"/><text x="289" y="152" text-anchor="middle" font-size="12" font-family="monospace">flywheel</text><rect x="240" y="164" width="98" height="30" rx="4" fill="#fff" stroke="#18181b" stroke-width="1.5"/><text x="289" y="184" text-anchor="middle" font-size="11.5" font-family="monospace">targetSpeed</text><rect x="279" y="214" width="20" height="15" rx="2" fill="#5f5f66"/><path d="M283 214v-5a6 6 0 0 1 12 0v5" fill="none" stroke="#5f5f66" stroke-width="2.5"/><text x="397" y="50" text-anchor="middle" font-size="12.5" font-weight="800" fill="#A60012">PUBLIC:</text><text x="397" y="65" text-anchor="middle" font-size="12.5" font-weight="800" fill="#A60012">buttons</text><rect x="366" y="72" width="62" height="32" rx="16" fill="#A60012"/><text x="397" y="93" text-anchor="middle" font-size="11.5" font-weight="800" fill="#fff" font-family="monospace">spinUp</text><rect x="366" y="116" width="62" height="32" rx="16" fill="#A60012"/><text x="397" y="137" text-anchor="middle" font-size="11.5" font-weight="800" fill="#fff" font-family="monospace">isReady</text><rect x="366" y="160" width="62" height="32" rx="16" fill="#A60012"/><text x="397" y="181" text-anchor="middle" font-size="11.5" font-weight="800" fill="#fff" font-family="monospace">stop</text><rect x="236" y="246" width="178" height="26" rx="4" fill="#f6f4f4" stroke="#18181b" stroke-width="1.5"/><path d="M548 135h-96M462 125l-10 10 10 10" fill="none" stroke="#A60012" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/><text x="500" y="118" text-anchor="middle" font-size="13.5" font-weight="800">TeleOp</text><text x="500" y="160" text-anchor="middle" font-size="12.5" fill="#5f5f66">presses</text><text x="500" y="176" text-anchor="middle" font-size="12.5" fill="#5f5f66">buttons only</text></svg><figcaption>Public methods are the buttons anyone can press. Private fields are the machinery only the machine itself touches.</figcaption></figure>

```java
public class Launcher {
    private DcMotorEx flywheel;          // machinery: hidden inside
    private double targetSpeed = 0;      // machinery: hidden inside

    public void spinUp(double speed) {   // a button: anyone can press it
        targetSpeed = speed;
        flywheel.setVelocity(targetSpeed);
    }
}

```

```java
RobotHardware robot = new RobotHardware(this);   // "new" builds one object from the blueprint
robot.init();                                    // press one of its buttons
```

This is a cut-down example. A real launcher file has more buttons, such as "is it up to speed yet?"

<p class="hub-why">If the launcher's insides change (a new motor, a new way to spin up), the buttons stay the same, so nobody else's code breaks. Two pairs of students can work at once: one builds the insides, the other writes the TeleOp that presses the buttons.</p>

<div class="hub-tip"><b>See it with real robot code</b><a href="#/coding/sample-robot-code">Sample robot &amp; code</a> has a pretend robot to explore, and <a href="#/coding/one-file-to-objects">Last season's code, rebuilt</a> takes each team's TeleOp from last season apart into machines like this one.</div>

## Two more traps

<div class="hub-grid" style="grid-template-columns:repeat(auto-fill,minmax(260px,1fr))">
<div class="hub-card"><span class="hub-pic" style="height:96px"><svg viewBox="0 0 220 96"><rect x="20" y="30" width="70" height="44" rx="4" fill="#fff7d6" stroke="#8a6d00" stroke-width="2.5"/><text x="55" y="58" text-anchor="middle" font-size="14" font-weight="800">"red"</text><rect x="130" y="30" width="70" height="44" rx="4" fill="#fff7d6" stroke="#8a6d00" stroke-width="2.5"/><text x="165" y="58" text-anchor="middle" font-size="14" font-weight="800">"red"</text><text x="110" y="20" text-anchor="middle" font-size="12.5" font-weight="800" fill="#2e7d32">same letters</text><text x="110" y="92" text-anchor="middle" font-size="12.5" font-weight="800" fill="#A60012">two different boxes</text></svg></span><b>Text: use <code>.equals()</code>, not <code>==</code></b><code>alliance.equals("red")</code> compares the letters. <code>==</code> asks "is it the same box?" and can say false even when both say "red".</div>
<div class="hub-card"><span class="hub-pic" style="height:96px"><svg viewBox="0 0 220 96"><path d="M40 34l-10-12M110 34l10-12" stroke="#5f5f66" stroke-width="2.5" stroke-linecap="round"/><rect x="40" y="34" width="70" height="44" rx="4" fill="#fff" stroke="#5f5f66" stroke-width="2.5" stroke-dasharray="6 4"/><text x="75" y="61" text-anchor="middle" font-size="13" font-weight="800" fill="#5f5f66">null</text><path d="M150 30l8 14 14-6-6 14 14 8-16 2 2 16-12-10-10 12-2-16-16-2 14-8-6-14 14 6z" fill="#fbecee" stroke="#A60012" stroke-width="2.5" stroke-linejoin="round"/></svg></span><b><code>null</code>: the empty box</b>Using an object that's still empty crashes with a <b>NullPointerException</b>. Most common cause: forgetting <code>robot.init()</code>. The error names the file and line. Read it!</div>
</div>

**Good to know:** robot code uses an older Java (Java 8). Code from the internet that uses newer features, like `var x = ...`, won't build.

## Check yourself

Tap a question to see the answer.

<div class="hub-quiz">
<details><summary>What's the difference between int and double? What does 7 / 2 give?</summary><div><code>int</code> holds whole numbers, <code>double</code> holds decimals. <code>7 / 2</code> is two whole numbers, so Java throws the fraction away and gives <b>3</b>. Write <code>7.0 / 2</code> to get 3.5.</div></details>
<details><summary>What's the difference between = and ==?</summary><div>One <code>=</code> puts a value in a box. Two <code>==</code> ask "are these equal?" and give true or false.</div></details>
<details><summary>Where does a counter go: before the loop or inside it?</summary><div>Before. Anything made inside the loop is made again every time, so the counter would keep going back to 0.</div></details>
<details><summary>In the vending machine, what are the buttons and what's the machinery?</summary><div>Buttons are the public methods anyone can call, like <code>spinUp()</code>. Machinery is the private fields only the machine itself touches, like the flywheel motor.</div></details>
<details><summary>How do you check if a String says "blue"?</summary><div><code>alliance.equals("blue")</code>. Not <code>==</code>.</div></details>
</div>
