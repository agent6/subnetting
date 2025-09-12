# Subnetting Explainer – Interactive

An interactive, single‑file IPv4 subnetting tool. Edit any field (IP, CIDR, or mask) and everything stays in sync. Network vs Host bits are color‑coded in binary visualizations. No dependencies; just open the page.

## Features
- Live sync: IP, CIDR, and subnet mask update each other in real time.
- Binary viz: 32‑bit views with color‑coded Network and Host bits.
- Smart masks: Accepts decimal masks and snaps non‑contiguous masks to the nearest valid contiguous mask.
- Calculations: Network, Broadcast, First/Last usable host, total addresses, and usable hosts (handles /31 and /32).
- Shortcuts: Classful prefix button, Next/Previous subnet jumpers, and Randomize.
- Zero deps: Pure HTML/CSS/JS in a single `index.html`.

## Quick Start
- Open `index.html` in any modern browser.
- Type an IPv4 address (e.g., `192.168.1.10`) and a CIDR (e.g., `24`).
- Or edit the subnet mask; it normalizes to a valid mask and updates CIDR.

## GitHub Pages
Host it directly from this repo with GitHub Pages:
- Push this repository to GitHub.
- In your repo, go to: Settings → Pages.
- Build and deployment → Source: “Deploy from a branch”.
- Branch: `main` (or your default), Folder: `/` (root).
- Save. Your site will be available at:
  `https://<your-username>.github.io/<your-repo>/`

## Usage Notes
- IPv4 only. CIDR range is `0–32`.
- Mask edits are validated; non‑contiguous masks are snapped to the closest valid contiguous mask.
- For `/31` and `/32`, usable host count is `0` by design; fields and counts reflect these special cases.
- Read‑only fields (Network, Broadcast, Range) update automatically.

## Tech
- Single page: `index.html` (HTML, CSS, vanilla JS).
- No build step, no external libraries.

## Development
- Open `index.html` and modify styles or logic as needed.
- Key functions: IPv4 parsing/formatting, CIDR↔mask conversion, binary visualization, and subnet math are implemented inline.

## Screenshot (optional)
Add a screenshot (e.g., `/screenshot.png`) and embed it here:

```md
![Subnetting Explainer](screenshot.png)
```

## License
Specify your preferred license (e.g., MIT) by adding a `LICENSE` file.

