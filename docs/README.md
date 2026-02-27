# HiveFabric Public Documentation

This repository contains the public documentation for the HiveFabric project.

## Structure

- `docs/public/` holds public docs.
- `docs/mkdocs.yml` is the MkDocs configuration for this repository.
- Internal/private docs are maintained separately in `hivefabric/.github-private`.

## Local preview

```bash
cd .github/docs
mkdocs serve -f mkdocs.yml
```

## Source of truth

- Public architecture and APIs: this repository.
- Private status, runbooks, and internal planning: `.github-private`.
