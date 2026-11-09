# Preview your site locally, then publish it

Your site is a Jekyll site. You only need to do the one-time setup once.

## 1. One-time setup (Mac)

macOS ships with an old Ruby that won't work, so install a current one with Homebrew.

```bash
# Install Homebrew if you don't have it (see https://brew.sh)
brew install ruby

# Put Homebrew's Ruby first on your PATH.
# Apple silicon (M1/M2/M3/M4):
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
# Intel Mac instead:
# echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc

# Open a NEW Terminal window, then check:
ruby -v      # should say 3.2 or newer
```

Then install the site's dependencies (run inside this folder):

```bash
cd path/to/lilyheald.github.io
bundle install
```

## 2. Preview

```bash
bundle exec jekyll serve
```

Open **http://localhost:4000** in your browser. The site rebuilds when you save a file.
Just refresh the page (changes to `_config.yml` need a restart: Ctrl+C, then run the command again).
Stop the server with Ctrl+C.

## 3. Publish on GitHub

1. On GitHub, create a new **public**, empty repository named exactly **`lilyheald.github.io`**
   (don't add a README or license; this folder already has them).
2. In Terminal, from this folder:

   ```bash
   git init -b source
   git add -A
   git commit -m "Personal website"
   git remote add origin https://github.com/lilyheald/lilyheald.github.io.git
   git push -u origin source
   ```

   The deploy workflow builds from the **`source`** branch, so push to `source`, not `main`.
3. One time only: in the repo, go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.
4. Go to the **Actions** tab, open **Build and Deploy**, and click **Run workflow** (or just push another commit).
   After a minute or two the site is live at **https://lilyheald.github.io**.

Every later `git push` updates the site automatically.

Your existing project page at https://lilyheald.github.io/PAINT/ keeps working. GitHub serves it from the PAINT repo underneath this site.

## Where things live

| To change...                          | Edit                          |
|---------------------------------------|-------------------------------|
| Name, title, email, links, color      | `_config.yml`                 |
| Home page text                        | `_pages/home.md`              |
| About page (experience, skills, etc.) | `_pages/about.md`             |
| Research cards                        | `_pages/research.md`          |
| Publications                          | `assets/ref.bib`              |
| Presentations                         | `_data/talks.yml`             |
| Awards                                | `_data/awards.yml`            |
| Software                              | `_data/software.yml`          |
| Mentoring & service                   | `_data/teaching.yml`          |
| Headshot                              | `images/headshot_lily.jpg`    |

In `assets/ref.bib`, `status={review}` or `status={prep}` decides which section a paper appears under, and `selected={true}` features it on the home page.
When a paper is published, add a section for it to `_pages/publications.md`, for example `{% bibliography --query @article %}`.

Full template documentation: `TEMPLATE_README.md`.
