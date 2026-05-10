A GitHub template repository for rendering a professional PDF résumé from a YAML file — no local installation required.

---

> [!NOTE]
> This is a thin workflow wrapper around [rendercv](https://github.com/rendercv/rendercv), which is the tool actually doing the work. The schema, renderer, and output quality are all the work of [Sina Atalay](https://github.com/sinaatalay) and the other contributors to that project. If this template is useful to you, the underlying project is what made it possible.

## Quickstart

### 1. Use this template

[**Use this template**](https://github.com/joshkaspar/rendercv-template/generate) (the green button at the top-right when you're logged in) to create your own repository.

> [!WARNING]
> Don't forget to **make it private** — your resume.yaml will contain your phone number and email address, which you probably don't want out in the open and indexed by search engines.

### 2. Edit `resume.yaml`

Open `resume.yaml` in the GitHub file editor (or the editor of your choice after cloning it locally). Replace the example content with your own information. The file is fully annotated with commented-out options for customising the layout, fonts, and colours.

Detailed yaml documentation can be found at https://docs.rendercv.com

> [!TIP]
> Every time you edit the yaml file, or make any other change to the repo, and indicator at the top of the page will tell you if the changes you made were valid: 🟠=processing | 🟢=valid | ❌=error.  
> A workflow (`lint.yml`) does a dry-run render to catch YAML errors early — if anything is wrong, the exact error output from RenderCV appears in the job summary in the **Actions** tab.

### 3. Trigger the workflow

Go to the **Actions** tab → **Render Resume** → **Run workflow** → **Run workflow**.

### 4. Download your PDF

When the run finishes, go to the **Releases** page. A new release named after today's date will contain your rendered PDF.

> [!IMPORTANT]
> If the render fails, open the failed run in Actions and read the **job summary** — the exact error from RenderCV is printed in the summary.

## Autocomplete in VSCode

`.vscode/settings.json` is included and automatically wires up the RenderCV JSON schema for YAML autocompletion. Field names, types, and valid values will suggest inline as you type.

If you use a different editor, the `# yaml-language-server` comment at the top of `resume.yaml` points compatible language servers at the same schema.

## Why this project exists

I noticed that 1.2k+ people had forked [rendercv](https://github.com/rendercv/rendercv) - most with zero code changes. I think they were looking for a way to render a résumé in the cloud, only to find the main repository is a software library. This template is a missing link for those users.

## Why you should consider using rendercv.com instead

The web app offers things this template cannot:

- **Live preview** — make a change and it appears in the preview window instantly. 
- **PDF Import** - drop your old résumé in, a slick modern version comes out.
- **Browser-native autocomplete** — schema validation and field suggestions without any editor setup
- **AI agent** — describe your experience in plain language and it structures the YAML for you	
