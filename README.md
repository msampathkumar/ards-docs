# ARD documentation site

Source for the **Agentic Resource Discovery** documentation site —
[agenticresourcediscovery.org](https://agenticresourcediscovery.org).

Built with [MkDocs](https://www.mkdocs.org/) + Material and deployed to GitHub
Pages automatically by
[`.github/workflows/publish-docs.yaml`](.github/workflows/publish-docs.yaml) on
every push to `main`. Nothing needs to run locally.

## Editing

- Pages live in [`docs/`](docs/) as Markdown; the navigation is defined in
  [`mkdocs.yml`](mkdocs.yml).
- The **specification** page is *not* edited here — it's generated at build time
  from the canonical [`ards-project/ard-spec`](https://github.com/ards-project/ard-spec)
  repo by [`hooks/spec_from_canonical.py`](hooks/spec_from_canonical.py). Edit the
  spec there.

## Preview locally (optional)

```bash
python -m venv .venv-docs
.venv-docs/bin/pip install -r requirements-docs.txt
.venv-docs/bin/mkdocs serve
```

Changes land via pull request, reviewed per [`.github/CODEOWNERS`](.github/CODEOWNERS).
