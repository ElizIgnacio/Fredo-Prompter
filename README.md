# Fredo-Prompter

A simple teleprompter for **video talks and recordings**: the script stays in the **upper part of the screen** so your gaze stays closer to the **camera** (typical laptop webcam at the top).

Everything runs in **one file** (`index.html`) — no Node, no build step, and no third-party account required.

## Open on the web (GitHub Pages)

Public URL:

**[https://elizignacio.github.io/Fredo-Prompter/](https://elizignacio.github.io/Fredo-Prompter/)**

The first deploy can take **1–2 minutes**. If the page does not load, refresh the browser or check **Settings → Pages** to confirm the build finished without errors.

### Enable GitHub Pages on another repository (step by step)

1. On GitHub, open the repository → **Settings**.
2. In the sidebar, click **Pages**.
3. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
4. Under **Branch**, pick **`main`** (or `master` if that is your default) and folder **`/ (root)`** → **Save**.
5. The site will be at `https://YOUR_USER.github.io/REPO_NAME/` (GitHub shows the exact link on the same Settings → Pages screen).

`index.html` must be at the **root** of the chosen branch (as in this project).

## How to use

1. Open `index.html` in your browser (double-click or drag into Chrome / Safari / Firefox), **or** use the GitHub Pages link above.
2. Paste your script in the text box.
3. Set **scroll speed** (px/s) and **font size** (px) using the number fields.
4. Optional: set **Target time (mm:ss)**. If it is greater than zero, **speed is calculated** on start to try to finish the script in that time.
5. Click **Start Fredo-Prompter**.

### While reading

- **Space**: pause / resume  
- **+** and **-**: increase or decrease speed in steps of 5 px/s  
- **Elapsed** and **Remaining**: footer timers (remaining only shows when a target time is set)  
- **Back to start**: resets scroll and the elapsed timer  
- **Edit script**: returns to the setup screen (your pasted text stays)

## Open via file URL

In the browser, use an address like:

`file:///path/to/your/project/index.html`

## Window layout tip

Keep Fredo-Prompter in **one window** (or the top half of the screen) and your video call in another so reading and camera line up.

## Repository files

| File | Description |
|------|-------------|
| `index.html` | Full app (HTML, CSS, JS) |
| `FREDO-PROMPT_ER-REPLICAR.md` | Prompt to recreate the project elsewhere |
| `.gitignore` | Ignores local macOS files (e.g. `.DS_Store`) |

## License

Internal / presentation helper project. Set a license that matches your org policy if you distribute it more broadly.
