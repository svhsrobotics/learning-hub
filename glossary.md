# Glossary

Words you'll hear on the team, from Java to the competition rules, in plain English. Skim it now and come back when a word confuses you. Words are grouped by topic, not in A to Z order.

## Java words

| Word | What it means |
|---|---|
| **Java** | The programming language we write robot code in. It's strict about spelling and punctuation, which is annoying at first but catches lots of mistakes before the robot ever moves. |
| **Code** | Exact instructions the robot follows, in order, very fast. The robot does what you *wrote*, not what you *meant*. |
| **Variable** | A labeled box that holds one value, like `speed = 0.5`. You can change what's in the box later. |
| **Type** | What kind of thing a box can hold: `int` (whole numbers), `double` (decimals), `boolean` (true or false), `String` (text). |
| **Class** | A blueprint. It describes what a thing remembers and what it can do. Like the LEGO instructions for a set. |
| **Object** | One real thing built from a class. Many objects can come from one class, like many identical LEGO cars built from the same instructions. |
| **Subsystem** | The class for one part of the robot, like the launcher or the intake. Each one owns its motors and sensors and has simple methods like `turnOn()`. See [Sample robot & code](coding/sample-robot-code.md). |
| **Method** | An action an object can do, like `drive()` or `stopDrive()`. Think of it as a button on a vending machine. |
| **Field** | A variable that belongs to an object and stays as long as the object exists. It's the object's memory. |
| **public / private** | Who may use something. `public` is the vending machine's buttons (anyone can press them). `private` is the machinery inside (only the machine itself touches it). |
| **Constant** | A value that never changes, written `static final` and in ALL_CAPS, like `SLOW_MODE_SCALE`. These are the "tuning knobs" you'll change most. |
| **Compile / compiler** | Turning the Java you wrote into something a computer can run. The compiler refuses to finish if there are spelling or type mistakes, and points to the line. |
| **Bug / debugging** | A bug is code that doesn't do what you meant. Debugging is finding out why and fixing it. |
| **null** | "Nothing is in this box yet." Using a null object crashes the program with a NullPointerException. |

## Tools on your laptop

| Word | What it means |
|---|---|
| **Android Studio** | The program we write code in. It's like a word processor for code, plus buttons to build and install the robot app. |
| **Gradle** | The build tool inside Android Studio. It follows the recipe in the `build.gradle` files to turn our code plus FIRST's code into one app. |
| **Gradle sync** | Android Studio reading the recipe and downloading what it needs. Do it after opening the project or pulling new code. |
| **Build** | Turning all the code into an app. If the build fails, nothing can go on the robot. |
| **Deploy (install)** | Sending the built app from the laptop to the Control Hub, with Android Studio's green Run arrow. Until you deploy, the robot keeps running the old code. |
| **APK** | The finished Android app file that gets installed on the Control Hub. You rarely see it directly. |
| **SDK (Software Development Kit)** | FIRST's ready-made code that knows how to talk to motors, sensors, gamepads and the Driver Station. This season's version is **12.0**. We build on top of it instead of starting from scratch. |
| **FtcRobotController** | The folder that holds FIRST's part of the project. We don't edit it. |
| **TeamCode** | The folder that holds *your team's* code. This is where you work. |
| **AGP Upgrade Assistant** | A pop-up in Android Studio that offers to upgrade the build tools. **Always say no** on FTC projects. FIRST sets those versions on purpose, and the upgrade rewrites their files. |

## Robot hardware

| Word | What it means |
|---|---|
| **Control Hub** | The robot's brain, made by REV. Our code runs here. Motors, servos and sensors plug into it. |
| **Expansion Hub** | An add-on box that gives the Control Hub more ports for motors and servos. We may use at most one (rule R701). |
| **Driver Station / Driver Hub** | The handheld screen the drive team holds, with the gamepads plugged in. It's a remote control with a screen: it picks the program, sends gamepad input, and shows messages. It does **not** run our code. |
| **Motor** | Spins things (wheels, intakes, launchers). The robot may have at most 8 (rule R501 to R503). |
| **Servo** | A small motor that moves to a position you choose, like an arm that goes to "open" or "closed". At most 8. |
| **Encoder** | A sensor on a motor that counts how far it has turned. |
| **Sensor** | Anything that measures the world: distance, color, angle, and more. |
| **IMU** | A sensor inside the Control Hub that knows which way the robot is facing, like the compass in your phone. |

## Robot software

| Word | What it means |
|---|---|
| **OpMode** | One program that shows up in the Driver Station's list. You pick one, press INIT, then START. |
| **TeleOp** | An OpMode the drivers control with gamepads. Used in the 2:00 driver-controlled part of the match. |
| **Autonomous (AUTO)** | An OpMode that drives the robot by itself, with no gamepads, during the first 30 seconds of a match. |
| **LinearOpMode** | The style of OpMode we use. It reads top to bottom like a recipe: set up, wait for START, then loop until STOP. |
| **Hardware configuration** | A list saved on the robot that says what is plugged into which port and gives each device a name, like "front_left_motor is on motor port 0". Made on the Driver Station. |
| **hardwareMap** | How code finds a device by its configuration name. The name in code must match the configuration *exactly*, or the program stops at INIT with an error. |
| **Telemetry** | Text messages the robot sends to the Driver Station screen. It's the robot's voice, and your best debugging tool. |
| **Gamepad** | The game controller. In code it's `gamepad1` (driver 1) and `gamepad2` (driver 2). |
| **Hardware class** | One shared file that sets up every motor and sensor (FIRST's sample `RobotHardware.java` shows how to start one). Every OpMode uses it, so motor names live in one place. |

## Driving and position

| Word | What it means |
|---|---|
| **Mecanum wheels** | Wheels with angled rollers that let the robot slide sideways (strafe) as well as drive and turn. |
| **Odometry** | Figuring out where the robot is on the field by measuring how far its wheels have rolled and which way it turned. Like counting your steps with your eyes closed. |
| **Dead wheels (odometry pods)** | Small extra wheels that aren't powered. They just roll along the floor so encoders can measure movement accurately. |
| **Pinpoint** | A small goBILDA board that reads the odometry pods and a built-in angle sensor and tells the code the robot's position (x, y and heading). |
| **AprilTag** | A square black-and-white code (like a QR code) that a camera can recognize. This season they're under the HIVE's cells, facing down. They move when the HIVE tips, so we use them to **aim**, not to find our position on the field. |
| **Road Runner** | A free add-on library that helps a robot follow smooth paths in autonomous. It needs tuning for each robot. Optional for us, and it is not part of FIRST's SDK. |

## Git and GitHub

| Word | What it means |
|---|---|
| **Git** | A tool on your laptop that saves snapshots of the code and remembers every version. Like save points in a video game, but for code. |
| **GitHub** | A website that stores a copy of our Git projects online so the whole team can share them. Git is the tool; GitHub is the meeting place. |
| **Repo (repository)** | One project folder plus its whole history. Each team has its own repo (names on the [Git page](coding/git-and-github.md)). |
| **Clone** | Download a repo from GitHub to your laptop, with its full history. You do it once per laptop. |
| **Commit** | Save a snapshot of your changes on your laptop, with a short message saying what changed. |
| **Push** | Upload your commits to GitHub so teammates can get them. |
| **Pull** | Download teammates' new commits from GitHub and combine them with your copy. |
| **Branch** | A separate line of work. `master` is the official code on the robot. Other branches let you experiment without breaking `master`. |
| **Merge** | Combine two lines of work into one. Git does it automatically unless two people changed the same lines. |
| **Merge conflict** | When two people changed the same lines and Git asks a human to decide which version is right. Normal and fixable. |
| **Tag** | A permanent label on one exact version, like a bookmark that never moves. We tag the code before every event. |
| **Remote** | A nickname for a GitHub address, like `origin` (your team's repo). |
| **Fork** | A copy of a repo on GitHub that keeps the full history and remembers where it came from. Our starter repo is a fork of FIRST's, and each team repo is a fork of the starter. |
| **Sync fork** | The GitHub button that brings new work from a fork's parent into the fork. It's how SDK updates and shared fixes reach each team. |
| **Pull request** | A request to bring changes from one branch or repo into another. GitHub shows exactly what would change before anyone clicks Merge. |
| **Code captain** | The student on each team who keeps `master` building, brings in shared updates, and tags the code before each event. |
| **Force push** | Replacing the history on GitHub with yours. It can erase teammates' work. **We never do it.** |

## Competition rules words

| Word | What it means |
|---|---|
| **Competition Manual** | FIRST's official rule book for the season. It wins over anything on this site. |
| **Team Update** | An official change to the manual. The latest one we've checked is TU03 (October 1, 2026). |
| **FTC Dashboard / Panels** | Web tools that show live graphs and let you change numbers while the robot runs. Great for tuning at practice. **Banned during matches** (rule R704.D), because event Wi-Fi is shared by every robot and the rules keep extra data off the air. Telemetry on the Driver Station is the only allowed way to show data in a match, so Dashboard must never be in our competition code. |
| **Inspection** | The check at an event where volunteers make sure the robot follows the rules before it can play. |
