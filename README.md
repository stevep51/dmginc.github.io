# GitHub Pages (Jekyll)

This repository is configured as a GitHub Pages site using Jekyll.

## Local preview

1. Install Ruby 3.x and Bundler.
   - macOS (recommended with `rbenv`):

   ```bash
   brew install rbenv ruby-build
   rbenv install 3.2.2
   rbenv local 3.2.2
   gem install bundler
   ```

   If your shell does not already initialize `rbenv`, add this and restart shell:

   ```bash
   echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
   ```

2. Install dependencies:

   ```bash
   bundle install
   ```

3. Run the site:

   ```bash
   bundle exec jekyll serve
   ```

4. Open `http://127.0.0.1:4000`.

If you see an error like `ffi-1.17.3... requires ruby version >= 3.0`, your shell is still using system Ruby (`2.6.x`). Run `ruby -v` and make sure it reports `3.x`.

## Publish on GitHub Pages

1. Commit and push this repository to GitHub (`main` branch).
2. In the repository settings, open **Pages**.
3. Under **Build and deployment**, set:
   - **Source**: GitHub Actions
4. Save.
5. Open the **Actions** tab and watch the workflow `Deploy Jekyll site to Pages`.
6. After it finishes, open the Pages URL shown in Settings > Pages.

The site will be available at the repository Pages URL shown in Settings > Pages.
