# 🍅 Pomodoro

A minimal, lo-fi Pomodoro timer built with pure HTML, CSS, and JavaScript. No frameworks, no build steps — just drop it in a repo and deploy.

## Features

- **Configurable sessions** — set your own work time, rest time, and number of cycles. Click directly on any number to edit it inline.
- **Auto-start** — the timer begins as soon as you hit *Comenzar*.
- **Inline time editing** — tap the big clock during a session to type a new time directly.
- **Quick adjust** — buttons to add or remove 1 or 5 minutes on the fly.
- **Progress bar** — a thin line below the clock that shrinks from both outer ends toward the center.
- **Cycle indicators** — dots below the controls show your progress. Click any dot to jump to that cycle.
- **Sound notifications** — soft chimes play when a work or rest session ends.
- **8 lo-fi themes** — Papel, Lluvia, Musgo, Noche, Durazno, Blanco, Negro, Rojo. Your choice is saved in localStorage.
- **New session shortcut** — a button in the bottom bar lets you restart without finishing the current session.
- **Responsive** — works on desktop and mobile.

## File structure

```
/
├── index.html
├── sounds/
│   ├── work-end.wav    ← plays when a work session ends
│   └── rest-end.wav    ← plays when a rest session ends
└── README.md
```

## Deploy to Cloudflare Pages (free plan)

1. Push this repository to GitHub or GitLab.
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/) → **Create a project** → **Connect to Git**.
3. Select your repository.
4. Leave **Build command** empty and set **Build output directory** to `/` (or the folder where `index.html` lives).
5. Click **Save and Deploy**.

That's it. No build step needed — Cloudflare serves the static files directly.

## Sounds

The two WAV files in `/sounds/` are simple chimes generated with Python's `wave` module — no external libraries required. You can replace them with any audio files you prefer (WAV or MP3), just keep the same filenames.

| File | When it plays |
|------|---------------|
| `work-end.wav` | End of every work session |
| `rest-end.wav` | End of every rest session |

## Themes

Hover over the **tema** label in the bottom bar to reveal the theme picker. On mobile, tap it to toggle. Your selected theme persists across visits via `localStorage`.

| Theme | Description |
|-------|-------------|
| Papel | Warm parchment |
| Lluvia | Rainy blue-grey |
| Musgo | Deep forest green |
| Noche | Soft purple-dark |
| Durazno | Warm terracotta |
| Blanco | Clean white |
| Negro | Dark grey |
| Rojo | Warm red |

## License

Do whatever you want with it.
