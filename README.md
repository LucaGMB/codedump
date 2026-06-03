# CodeDump

Consolidate any repository into a single downloadable file, directly in your browser.

## What it does

CodeDump lets you take a GitHub repository or a local ZIP archive and merge all the selected source files into one `.txt` or `.md` file. Useful for feeding codebases into LLMs, doing code reviews offline, or archiving projects.

## Features

**Two input sources:**
- GitHub repositories (public without auth, private with a Personal Access Token)
- Local `.zip` files, extracted entirely in the browser via JSZip

**Interactive file tree:**
- Checkbox per file and folder with cascading selection
- Indeterminate state on partially selected folders
- Filter by extension in real time (e.g. `.js, .ts, .jsx`)
- Exclude by glob patterns (e.g. `node_modules, *.test.js, dist`)

**Format options:**
- Add a customizable header before each file (`{filename}`, `{filepath}`, `{extension}`)
- Strip blank lines
- Strip comments (`//`, `#`, `/* */`, `<!-- -->`) based on file type
- Strip indentation
- Collapse all line breaks into a single line

**Output:**
- `.txt` plain text
- `.md` with fenced code blocks and inferred language per file

Everything runs client-side. No backend, no data leaves your browser.

## Usage

Open `index.html` in any modern browser. No build step required.

Or use GitHub Pages if you deploy this repo.

## Stack

- React 18 (via CDN, no build step)
- JSZip for ZIP extraction
- Vanilla JS for file generation and download

## License

MIT
