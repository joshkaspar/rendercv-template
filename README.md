A GitHub template repository for rendering a professional PDF résumé from a YAML file — no local installation required.

---

> [!NOTE]
> This is a thin workflow wrapper around [RenderCV](https://rendercv.com), which is the tool actually doing the work. The schema, the renderer, the output quality — all theirs. If this template is useful to you, the underlying project is what made it possible.

## Quickstart

### 1. Use this template

Click **"Use this template"** (the green button at the top of this page on GitHub) and create your own repository.

### 2. Edit `resume.yaml`

Open `resume.yaml` in the GitHub file editor (or clone the repo). Replace the example content with your own information. The file is fully annotated with commented-out options for
customising the layout, fonts, and colours.

Detailed yaml documentation can be found at https://docs.rendercv.com

### 3. Trigger the workflow

Go to the **Actions** tab → **Render Resume** → **Run workflow** → **Run workflow**.

### 4. Download your PDF

When the run finishes, go to the **Releases** page. A new release named after today's date will contain your rendered PDF.

> [!IMPORTANT]
> If the render fails, open the failed run in Actions and read the **job summary** — the exact error from RenderCV is print

## Autocomplete in VSCode

`.vscode/settings.json` is included and automatically wires up the RenderCV JSON schema for YAML autocompletion. Field names, types, and valid values will suggest inline as you type.

If you use a different editor, the `# yaml-language-server` comment at the top of `resume.yaml` points compatible language servers at the same schema.

## Why this project exists

On my first visit to [RenderCV.com](https://rendercv.com) I used my one PDF export as I was testing the tool out, not realizing that subsequent PDF downloads were paywalled. The tool is fully open source and available as a Python package, so I installed it locally and tweaked the output until I got it how I wanted it. But along the way, I noticed that 1.2k+ people had forked the original project, with the vast majority of those projects containing 0 code changes. 
I think a lot of those users were hoping they would be able to generate some résumés once they forked the repository - maybe even from github itself. Or maybe some of them are like me, and they want to own the process in some way. So I made this template to make the process easier.

## Why you should consider using rendercv.com instead

The web app offers things this template cannot:

- **Live preview** — make a change and it appears in the preview window instantly. 
- **PDF Import** - drop your old résumé in, a slick modern version comes out.
- **Browser-native autocomplete** — schema validation and field suggestions without any editor setup
- **AI agent** — describe your experience in plain language and it structures the YAML for you
- **No GitHub account required** — works entirely in the browser
	
