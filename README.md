# mapzen-docs-generator

Mapzen documentation pipeline.

**Current documentation generator:** [MkDocs](http://www.mkdocs.org/)

### Rapid bootstrapping

```shell
# Clone repository
git clone https://github.com/mapzen/mapzen-docs-generator.git
cd mapzen-docs-generator

# Get all the sources
make get

# Build all the documentations
make all

# Local preview
python -m SimpleHTTPServer 8000
```

**NOTE:** `Make` automatically downloads and installs local Python dependencies into the `./env/` directory.

## Making MkDocs happy

### You must always:

- Include an `index.md` file at the root folder of your documentation.
- Include all local documentation assets, such as images, inside this root folder (or link to an external source).
- Start each page with a top-level heading.

### You will sometimes:

- Think carefully about the choices you made in life.

### Markdown formatting tweaks for compatibility with GitHub

- Good luck!