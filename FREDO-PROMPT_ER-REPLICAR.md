# Prompt to replicate Fredo-Prompter in Cursor

Copy the block below (everything between the `---` lines) and paste it into a **new Cursor chat** in the project folder where you want the file generated. An empty folder or a new project works.

---

## Prompt (copy from here)

Build a **teleprompter as a static website** in a single `index.html` file (HTML + CSS + JavaScript, no frameworks, no required server — it must open with a double-click in the browser).

### Intended use

- **Video presentations**: the script should appear in the **upper part of the screen** (~22% of the height with a subtle horizontal guide line) so the reader’s gaze stays closer to the **camera** on laptops with a top-center webcam.
- Can live in a **separate browser window** from the rest of your work.

### Setup screen (configuration)

- Title and help text in **English (`lang="en"`)**.
- **Large area to paste the script** (textarea).
- **Scroll speed**: **typed** numeric field (not a slider), label like “Scroll speed (px/s)”, integer values between **5** and **120**, default **40**. Unit: pixels per second.
- **Font size**: **typed** numeric field, between **16** and **56** px, default **28**.
- Button **Start Fredo-Prompter** (only meaningful if there is text; if empty, focus the textarea).
- If the user leaves an invalid or empty number in a field, on leaving the field (**change**), restore the **last valid value**.

### Prompter mode (full page)

- Dark background, light text, text **horizontally centered**, comfortable side margins (e.g. horizontal padding in `vw`).
- **Auto scroll** upward: content moves with `requestAnimationFrame` at **px/s** speed.
- **Read line**: horizontal line at **~22%** of the viewport height (soft color, not distracting).
- **Top padding** on the text block so the **first line** starts aligned with the read-line zone; **large bottom padding** so the end of the script does not cut off abruptly.
- **End-of-scroll clamp**: when the script ends, do not scroll past the end of the content (use `offsetHeight` and window height).
- **Fixed bottom control bar (HUD)**: buttons **Pause / Resume**, **Back to start**, **Edit script** (returns to setup without losing pasted text).
- In the HUD: the **same numeric speed field** (px/s), synced with the setup screen.
- **Keyboard** (while prompter is active): **Space** toggles pause; **+** and **-** adjust speed in steps of **5** (respect min/max).
- **Window resize**: recompute read-line padding and scroll limits without jarring jumps.

### Implementation details

- Single file: `index.html`.
- `lang="en"`, viewport meta, coherent styles (visible focus on fields, prominent primary button).
- Numeric fields: `type="number"` with `inputmode="numeric"`; optional CSS to hide native spinners so fields feel more like plain text boxes.
- Script text: split on newlines (`\n`) into paragraphs; handle blank lines reasonably.

Deliver a complete, working `index.html`.

---

## Prompt (copy up to here)

### How to use on another machine / Cursor window

1. Open a folder in Cursor (new or existing).
2. Paste the prompt above into the agent chat and ask it to create the file (for example: “Implement this by creating `index.html` at the repo root”).
3. Open `index.html` in the browser (double-click or “Open with Live Server” if you use that extension).

Node, npm, and an external service account are **not** required to run the teleprompter.
