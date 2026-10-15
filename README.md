[README.md](https://github.com/user-attachments/files/33509418/README.md)
<div align="center">

<h1>Linux CMD</h1>
<h3>Master the terminal. Own your potential.</h3>

<p>A browser-based Linux practice studio that turns your first commands into an adventure.</p>

<p>
  <img alt="Built with HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&amp;logo=html5&amp;logoColor=white">
  <img alt="Styled with CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&amp;logo=css&amp;logoColor=white">
  <img alt="Powered by JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&amp;logo=javascript&amp;logoColor=black">
  <img alt="No account required" src="https://img.shields.io/badge/No_login-required-14b8a6?style=flat-square">
</p>

<p>
  <a href="#the-idea">The idea</a> &nbsp;·&nbsp;
  <a href="#inside-the-studio">Features</a> &nbsp;·&nbsp;
  <a href="#start-practising">Get started</a> &nbsp;·&nbsp;
  <a href="#how-it-works">How it works</a>
</p>

</div>

---

## The idea

Learning Linux can feel intimidating when the first thing you see is an empty terminal. **Linux CMD** gives beginners a place to explore, make mistakes, and try again—with command explanations, guided practice, and games that make progress visible.

The project combines a cybersecurity-inspired interface with practical exercises. Start with `pwd`, `ls`, and `cd`, then build confidence with files, text processing, and more.

**Explore → Practise → Complete missions → Test your skills.**

## Why it matters

- **A smaller first step:** open a browser and begin, without installing Linux or setting up a virtual machine.
- **Learning through action:** run commands and see how they change a simulated filesystem.
- **A reason to keep going:** missions, XP, badges, and personal best scores give learners clear milestones.
- **Space to experiment:** commands affect the website's simulated environment rather than the computer's real files.
- **Progress at your pace:** locally saved practice and game progress let you return to the same browser and continue.

Designed for Linux beginners, students, and people taking their first steps into cybersecurity. It is a foundation for later practice on a real Linux system.

## Inside the studio

<table>
  <tr>
    <td><strong>Interactive terminal</strong><br>Glass-style terminal, Linux penguin header, command history, quick command buttons, and Run or Enter controls.</td>
    <td><strong>Command reference</strong><br>Browse command descriptions, syntax, examples, categories, and difficulty levels.</td>
  </tr>
  <tr>
    <td><strong>Guided practice</strong><br>Five missions covering navigation, file management, text processing, system administration, and users.</td>
    <td><strong>Skill challenges</strong><br>Twelve challenges with objectives, difficulty levels, and completion rewards.</td>
  </tr>
  <tr>
    <td><strong>Progress dashboard</strong><br>Track XP, levels, badges, completed activities, and recent command history.</td>
    <td><strong>Your visual atmosphere</strong><br>Light and dark themes, three selectable backgrounds, responsive layouts, and subtle motion.</td>
  </tr>
</table>

### Adventure exams

| Game | The experience |
| --- | --- |
| **Compass Quest** | Help Pip restore the compass through ten command checkpoints. Explore the map, collect three fragments, use hints when needed, and work toward a better score and star rating. |
| **Cyber Spook Quest** | Answer 25 shuffled multiple-choice questions. Earn up to 250 points, review your results, and replay to improve your personal best. |

The games support saved progress and repeat attempts. Completion XP is awarded once per game reward, so replays do not repeatedly grant the same completion bonus.

### Three scenes. Two moods each.

| Background | Dark version | Light version |
| --- | --- | --- |
| **Haunted Lab** | Shadowy server cathedral, cyan glow, and mist | Silver architecture, daylight, and luminous server racks |
| **Dragon Core** | Circuit-inspired dragon vault and a glowing server core | Bright cyber architecture and an icy, atmospheric vault |
| **Ghost Protocol** | Rainy hacking workstation and midnight city views | Daylit workstation and a pale futuristic skyline |

Use the **image button beside the theme switch** to cycle through `1/3 → 2/3 → 3/3`. Switching themes automatically displays the matching artwork for the selected scene. Both preferences are saved locally.

## Start practising

### Open the website

Download this repository and open **`index.html`** in a modern browser. The application code, styling, and background images are included in that file; no package installation or build command is needed.

For more consistent browser storage behavior, serve the folder locally. If Python is installed, run:

```bash
python -m http.server 8000
```

Then open **http://localhost:8000**. On Windows, `py -m http.server 8000` is an alternative if the `python` command is unavailable.

### Try your first commands

Click **Start Practising**, then enter these commands one at a time:

```bash
pwd
ls
mkdir my-lab
cd my-lab
echo "Hello Linux" > notes.txt
cat notes.txt
```

The terminal starts in a simulated home directory. These commands show your location, list its contents, create a folder, move into it, write a file, and read it back.

### Continue your journey

1. Select a command in **Command Reference** to see its syntax and example.
2. Open **Practice** and choose a guided mission.
3. Complete objectives in **Challenges**.
4. Visit **Progress** to review your milestones.
5. Choose **Explore Adventure** or **Adventure Exam** to play the games.

## How it works

**Everything runs in the browser.** JavaScript parses a submitted command, routes it to the simulator, renders the result, checks active objectives, and saves updated state when browser storage is available.

| Part | Responsibility |
| --- | --- |
| HTML | Page structure, terminal controls, navigation, reference panels, and game screens |
| CSS | Responsive layouts, glass styling, theme colors, focus states, and motion |
| JavaScript | Command parsing, virtual files, missions, rewards, game logic, and UI updates |
| `localStorage` | Progress, simulated files, history, visual preferences, and game saves |
| Embedded WebP images | Background artwork included directly in the HTML file |

### A simulator with clear limits

File and navigation commands such as `mkdir`, `touch`, `cd`, `cp`, `mv`, `rm`, and `cat` operate on a **virtual filesystem**. Text commands support a selected set of options.

Some system, networking, and administration commands return educational simulated responses. The terminal is not Bash, does not run arbitrary shell scripts, and does not provide real network scanning or remote machine access. Its supported syntax is a subset of Linux command behavior.

## Saving and privacy

- No login, Firebase configuration, database, or backend is required for this version.
- The application saves data in the current browser for the current website origin.
- Progress does not automatically sync between browsers, devices, or different website addresses.
- Clearing site data can remove saved progress. Private browsing or blocked storage may prevent saves from lasting.
- The application code does not use IP addresses to identify learners or include analytics tracking. A hosting provider may maintain its own request logs.

<details>
<summary><strong>Developer reference: storage keys</strong></summary>

| Key | Saved data |
| --- | --- |
| `linuxcmd-state-v2` | Main practice state, XP, badges, command history, virtual files, theme, and background selection |
| `linuxcmd-adventure-v1` | Compass Quest progress and results |
| `linuxcmd-cyber-quiz-v1` | Cyber Spook Quest session, personal best, and recent attempts |

Keep these keys stable when updating the application if existing saves should remain accessible. A different domain or origin has separate browser storage.

</details>

## Project structure

| File | Purpose |
| --- | --- |
| [`index.html`](./index.html) | Complete website: HTML, CSS, JavaScript, and embedded background artwork |
| [`README.md`](./README.md) | Project overview and usage documentation |

This README describes the standalone HTML version. It does not require Next.js, TypeScript, Node.js, or Firebase.

## Put it online

Upload `index.html` and `README.md` to the root of your GitHub repository. Deploy the folder using a static website host such as GitHub Pages or Vercel. The website entry point is `index.html`; this version needs no server code, database credentials, or application build step.

The README badges use external image URLs; they are documentation decoration and are not required by the application.

## Contributing

Improvements to beginner explanations, command behavior, accessibility, and practice activities are welcome.

When reporting an issue, include the command or action, what you expected, what happened, and your browser and screen size. Avoid sharing private browser data.

Before proposing a change, check terminal execution, saved progress after a reload, both themes, background switching, mobile navigation, and both games.

## Author

Created by **Muhammed Faheem A.P.** to make Linux practice more approachable, engaging, and memorable.

[View the GitHub repository](https://github.com/faheemapofficial/Linux-cmd/)

---

<div align="center">
  <strong>Learn by exploring. Build confidence one command at a time.</strong>
</div>
