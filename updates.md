# Latest Updates

<!--
  HOW TO ADD AN UPDATE (this note is hidden on the website)

  1. Put your update BELOW this note, above the newest update. Anything typed
     inside this note never shows on the hub.
  2. Start with a heading: two # signs, a space, today's date written out,
     a colon, and a title. Example:   ## November 3, 2026: Sample Title Article
  3. Leave one empty line, then write a few sentences: Starting now, you need to add a Pull Request, here is how or why...

  Write the date like the example (month name, day, comma, year). The menu
  reads it to show the newest date, and the red star moves to the top update
  by itself.
-->

<p class="hub-lead">News and announcements for everyone in Saucon Valley Robotics. Newest first.</p>

## November 9, 2026: New Simulator Robot and Two Coding Pages

The Virtual Robot simulator has a new robot: the **Mecanum Odometry Bot**. It has mecanum wheels, 3 odometry pods and an intake, so you can practice driving and autonomous code on your laptop before your team's robot is ready. Any team can use it.

**To get it:** open the Virtual Robot project in Android Studio and click **Git > Pull**. Then pick **Mecanum Odometry Bot** in the Configuration list (steps: <a href="#/coding/simulator?id=try-the-mecanum-odometry-bot">Try the Mecanum Odometry Bot</a>). New to the simulator? Start with <a href="#/coding/simulator">Try the Virtual Robot</a>.

It comes with five example programs, in the `odometrybot` folder in TeamCode:

- **Manual Drive:** drive with the gamepad. It's laid out like FIRST's `BasicOmniOpMode_Linear` sample.
- **Pedro: TeleOp:** drive through Pedro Pathing, plus the intake.
- **Pod Test:** shows each odometry pod's count next to the robot's position.
- **Pedro: Auto Leave + Park:** Autonomous Level 1.
- **Pedro: Auto Launch + Park:** Autonomous Level 2. It curves to a launch spot facing the HIVE, with a pretend launch.

Two new pages under **Driving the robot** walk through that code step by step:

- <a href="coding/drive-explainer.html">TeleOp: drive with the gamepad</a>: how a TeleOp turns two joysticks into four mecanum wheel powers.
- <a href="coding/pedro-explainer.html">Autonomous with Pedro Pathing</a>: the two autonomous programs, for red and blue.

**Want to use the code on your team's robot?** Everything that depends on the robot is in two files: `RobotHardware.java` (motor names) and `pedro/Constants.java` (Pedro's settings).

## November 2, 2026: Game Controller Works on the Mac

The Virtual Robot simulator now runs on a MacBook with a real Logitech game controller. It was tested on a student's MacBook Air.

The key is one exact Java download: **Liberica Full JDK 17, x86**, from BellSoft's website. Without it, the controller won't work. The <a href="#/coding/simulator">Try the Virtual Robot</a> page has the updated steps:

- <a href="#/coding/simulator?id=_2-get-the-right-java">Get the right Java</a>: the exact download for a Mac, and how to pick it in Android Studio.
- <a href="#/coding/simulator?id=_4-set-up-the-gamepad">Set up the gamepad</a>: the one setting to change, and the switch on the back of the controller goes to **D**.

## October 28, 2026: Learning Hub Launch

Welcome to the Saucon Valley Robotics Learning Hub. It's our program's reference site for the BIOBUZZ season: the game, the field and the rules, coding, and the tools you'll use. Everything here comes from the official Competition Manual and FTC's own guides.

This page is where we'll post updates and announcements for all team members, newest first. Check back here when you want to know what's new.
