
Run this project in docker:
```
docker-compose up
```

If you're running Material for MkDocs from within Docker, use:
```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```
Point your browser to localhost:8000/sdet

When you're finished editing, you can build a static site from your Markdown files with:
```bash
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
```

```bash
docker run -d \
  --name cv-sdet \
  -p 8000:8000 \
  -v $(pwd):/docs \
  --restart unless-stopped \
  squidfunk/mkdocs-material
```