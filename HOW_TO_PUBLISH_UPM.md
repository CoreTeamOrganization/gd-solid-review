# How to Publish as a UPM Package via GitHub

## Step 1 — Push to GitHub

Create a new GitHub repository (e.g. `gd-solid-review`), then:

```bash
cd gd-solid-review/
git init
git add .
git commit -m "Initial release v1.0.0"
git branch -M main
git remote add origin https://github.com/YOUR_ORG/gd-solid-review.git
git push -u origin main
```

Tag the release for versioning:
```bash
git tag v1.0.0
git push origin v1.0.0
```

## Step 2 — Install in any Unity project

Window → Package Manager → + → Add package from git URL:

```
https://github.com/YOUR_ORG/gd-solid-review.git
```

To install a specific version:
```
https://github.com/YOUR_ORG/gd-solid-review.git#v1.0.0
```

## Step 3 — Update the package

```bash
git add .
git commit -m "v1.0.1 - fix xyz"
git tag v1.0.1
git push origin main --tags
```

Then in Unity: Package Manager → SOLID Review → Update

## Notes
- The repo root must contain `package.json` (already set up)
- No subfolder nesting — the package root IS the repo root
- Unity caches packages in `Library/PackageCache/` — never edit there
- To force Unity to re-fetch: delete `Library/PackageCache/com.gamedistrict.solid-review@*`
