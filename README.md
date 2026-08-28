# Curriculum Vitae

A personal CV built with HTML, CSS, and vanilla JavaScript. It uses no framework and requires no build step.

## How it works

The CV content is stored in `data.json`. `index.html` fetches the JSON file and generates the sections dynamically, so most content updates only require editing `data.json`.

`preview.html` is a standalone, static preview containing sample content. It does not load `data.json` and can be used as a visual reference or opened independently.

```text
portfolio/
├── index.html    # Data-driven CV page
├── preview.html  # Standalone sample preview
├── style.css     # Shared visual styles for index.html
├── data.json     # CV content
└── README.md
```

## Quick start

1. Clone or download the repository.
2. Edit `data.json` with your own information.
3. Start a local web server from the project folder:

	```bash
	npx serve .
	```

	Alternatively, install the Live Server extension in VS Code and choose **Open with Live Server** from the context menu for `index.html`.
4. Open the local URL shown by the server.

> A local server is required for `index.html` because the page loads `data.json` with `fetch()`. Opening `index.html` directly as a `file://` URL may prevent the JSON from loading.

## Customisation

### Content (`data.json`)

The main sections use these keys:

| Key | Contents |
| --- | --- |
| `meta` | Page language and document title |
| `persona` | Name, initials, role, and biography |
| `contacts` | Location, phone number, email, and links |
| `technicalSkills` | Skills and proficiency levels from 1 to 5 |
| `languages` | Languages and proficiency labels |
| `interests` | List of interest tags |
| `education` | Degrees, institutions, periods, and notes |
| `experience` | Roles, organisations, periods, locations, and descriptions or bullet points |
| `publications` | Titles, venues, years, and optional links |
| `certifications` | Certification titles, issuers, and years |
| `otherActivities` | Additional activities, details, and periods |

Keep the existing property names and data types when replacing the sample content. The `icon` field in `contacts` must match one of the keys defined in the `ICONS` object in `index.html`.

### Styling (`style.css`)

The CSS custom properties are defined in `:root`. Edit them to change the colour palette, typography-related dimensions, or sidebar width.

`preview.html` contains its own copy of the styles and sample markup. If you change the design in `style.css`, update `preview.html` separately if you want both pages to remain visually identical.

## Previewing in VS Code

With Live Server installed, right-click `index.html` and select **Open with Live Server**. The browser preview will refresh when you save changes. To view it inside VS Code, open the same local URL with **Simple Browser: Show** from the Command Palette.

## Publishing with GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Select the `main` branch and the `/ (root)` folder.
4. GitHub Pages will provide a URL such as `https://your-username.github.io/repository-name/`.

## Printing / PDF

Use `Ctrl+P` (or `Cmd+P` on macOS) in the browser. Print styles are included for a clean result.

## Licence

Personal project. Feel free to use and adapt it.
