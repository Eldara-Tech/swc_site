swarmcli site — Run locally
=============================

Quick instructions for viewing this static site on your machine.

Prerequisites
-
- Python 3 (recommended) or Docker or Node (optional).

Quick — serve the current directory (no build)
- Change into the site folder and run a simple HTTP server:

```bash
cd /opt/mosonyi/swarmcli/swc_site
python3 -m http.server 8000
# Open http://localhost:8000
```

This works because this repository already contains pre-rendered HTML (for example [index.html](index.html)).

Option: Node (quick)
- Use `npx` to start a lightweight static server:

```bash
cd /opt/mosonyi/swarmcli/swc_site
npx http-server -p 8000
# or: npx serve -l 5000
```

Option: Docker (serve with nginx)
- Run an nginx container serving the repository root:

```bash
cd /opt/mosonyi/swarmcli/swc_site
docker run --rm -p 8080:80 -v "$PWD":/usr/share/nginx/html:ro nginx:alpine
# Open http://localhost:8080
```

Option: Jekyll (if you want template rebuilding)
- This repository uses Jekyll-style folders (`_layouts`, `_includes`). To rebuild from source you'll need Ruby + Jekyll:

```bash
# install Ruby and then:
gem install bundler jekyll
# from repo root (if you add a Gemfile or use defaults):
jekyll serve --watch --livereload --port 4000
# Open http://localhost:4000
```

Notes
- Editing the `.html` files (for example [index.html](index.html)) will be visible immediately when using a static server.
- Editing `.md` files (for example [index.md](index.md)) may require a Jekyll build to produce updated HTML, depending on your workflow.
- If you want, I can add a small `Dockerfile`, `Makefile`, or `package.json` with a dev script.

Files to inspect
- [index.md](index.md)
- [_layouts/default.html](_layouts/default.html)
- [index.html](index.html)
