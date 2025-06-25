# GitHub Pages Deployment

This repository includes two GitHub Actions workflows for deploying to GitHub Pages:

## 1. Primary Workflow (`deploy.yml`)
This uses GitHub's official Pages deployment actions. To use this:

1. Go to your repository Settings → Pages
2. Under "Build and deployment", select "GitHub Actions" as the source
3. The workflow will run automatically on push to main/master branch

## 2. Alternative Workflow (`deploy-alternative.yml`)
This uses the popular `peaceiris/actions-gh-pages` action. To use this:

1. Go to your repository Settings → Pages
2. Under "Build and deployment", select "Deploy from a branch"
3. Select "gh-pages" branch as the source
4. The workflow will create and push to the gh-pages branch automatically

## Manual Deployment
You can also trigger either workflow manually:
1. Go to Actions tab in your repository
2. Select the workflow you want to run
3. Click "Run workflow"

## Notes
- Both workflows preserve your custom domain (aanshshah.com)
- They run on pushes to main/master branches
- They handle the static files (HTML, CSS, JS, PDFs) in your repository

## Choosing a Workflow
- Use the primary workflow (`deploy.yml`) if you want to use GitHub's newer deployment method
- Use the alternative workflow (`deploy-alternative.yml`) if you prefer the traditional gh-pages branch method

To disable a workflow, simply delete or rename its `.yml` file.