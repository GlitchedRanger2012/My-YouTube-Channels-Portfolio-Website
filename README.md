# Christopher's YouTube Portfolio — GitHub Pages Package

This folder contains the **built static website** for Christopher's YouTube Portfolio. It is ready to upload to a GitHub repository and serve with GitHub Pages. The package includes the generated HTML, CSS, JavaScript, fallback page, and visual assets; no Node.js build step is required after extraction.

## Quick setup

1. Create a new GitHub repository, or open the repository that will host the website.
2. Extract this ZIP file on your computer.
3. Upload the **contents of `christopher-portfolio-github-pages/`** to the repository's root directory. The repository root should contain `index.html`, `404.html`, the `assets/` directory, and the `manus-storage/` directory.
4. Commit the files to the repository's default branch.
5. In GitHub, open **Settings → Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select the branch containing the uploaded files and choose **`/ (root)`** as the folder, then click **Save**.
8. Wait for GitHub Pages to finish deploying. GitHub will display the live site URL in the Pages settings panel.

The included `.nojekyll` file tells GitHub Pages to serve the generated asset folders as-is. The included `404.html` mirrors the application entry page as a safe fallback if a visitor lands on an unknown path. Navigation uses hash-based routes (`#/archive` and `#/requests`), so the app works without server-side rewrite rules.

## Important upload detail

Upload the contents of the package folder, not the outer folder itself. A correct repository root will look like this:

```text
index.html
404.html
.nojekyll
README.md
assets/
manus-storage/
```

## Optional command-line upload

If Christopher prefers Git instead of the browser upload, from the extracted package directory run:

```bash
git init
git add .
git commit -m "Add Christopher portfolio for GitHub Pages"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

Replace `USERNAME/REPOSITORY` with the actual repository path. Then enable Pages using the Settings steps above.

## Routing and repository paths

This build uses hash-based client-side routing for GitHub Pages compatibility. The Home page is available at the repository URL, while the Archive and Requests pages can be reached through the site's navigation and use hash routes that do not require server-side rewrites.

## Included files

The deployable output includes the minified JavaScript bundle, compiled stylesheet, `index.html`, `404.html`, `.nojekyll`, and the five visual assets used by the site. The Archive page also loads YouTube thumbnails at runtime from YouTube's image service, so those dynamic thumbnails are not bundled.

## Rebuilding from source

This ZIP contains only the deployable static output. To rebuild the site from source, use the separate source package, install dependencies with `pnpm install`, and run the GitHub Pages build configured for relative asset paths.

## License and asset ownership

Confirm ownership and licensing of any creator-provided or third-party content before redistributing the site publicly. The original project manifest declares the MIT license for the project code.
