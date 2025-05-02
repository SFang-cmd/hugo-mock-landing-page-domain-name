# Cristofori: AI Assistant Landing Page

Welcome to the repository for **Cristofori**, a modern, emotionally intelligent AI assistant landing page. Built with [Hugo](https://gohugo.io/) and the [Hugo Bootstrap Theme](https://github.com/filipecarneiro/hugo-bootstrap-theme), this project emphasizes speed, SEO, and elegant design.

**Live Site:** [seanfang.click](https://seanfang.click)

---

## 🚦 Automated Deployment Workflow

This repository now features **automatic deployment to GitHub Pages** via a custom shell script and GitHub Actions workflow.

### How it works

1. **Push to `main` branch**  
   When you push changes to the `main` branch, GitHub Actions triggers a workflow that:
   - Builds the Hugo static site (`hugo` command).
   - Runs `publish_to_gh_pages.sh` to synchronize the built site (`public/` folder) with the `gh-pages` branch.
   - Publishes the latest content to the live site at GitHub Pages.

2. **Deployment Script**  
   See [`publish_to_gh_pages.sh`](./publish_to_gh_pages.sh) for the deployment logic.  
   - It checks for build artifacts, clones or initializes the `gh-pages` branch, syncs files, and force pushes only if there are changes.
   - The script includes robust checks for empty folders, handles orphan branches, and cleans up temporary files.

3. **GitHub Actions Workflow**  
   The workflow YAML (see `.github/workflows/`) automates the above steps.  
   - You can easily adapt or extend it for custom build steps.
   - No manual intervention is needed for routine content or style updates.

#### Example: Excerpt of conversation with Claude

> *Q: How do I automate Hugo deployment to GitHub Pages?*  
> *A: Use a shell script to push the `public/` folder to `gh-pages` and wire it up with GitHub Actions. I can help generate the script and workflow YAML.*

Feel free to ask Claude or ChatGPT for help customizing workflows or scripts!

---

## 🛠️ Tech Stack

- **Framework:** [Hugo](https://gohugo.io/)
- **Theme:** [Hugo Bootstrap Theme](https://github.com/filipecarneiro/hugo-bootstrap-theme)
- **Languages:** Go (Hugo), HTML, Markdown, SCSS
- **Deployment:** GitHub Pages (automated)

---

## ✨ Features

- Modern, responsive landing page
- User stories & product vision for Cristofori
- Automated deployment to GitHub Pages
- Contact & privacy policy pages
- Easily customizable via `config.toml`
- No cookies or personal data collected

---

## 📄 User Stories

See [`USER-STORIES.md`](./USER-STORIES.md) for the product backlog, including:
- Real-time voice response & meeting notes
- Multilingual conversation translation
- Emotional intelligence & sentiment analysis
- Custom knowledge base & autonomous scheduling

---

## 📁 Project Structure

- `content/` — Markdown content (about, contact, privacy, etc.)
- `layouts/` — Custom HTML templates
- `themes/` — Hugo Bootstrap Theme
- `static/` — Static assets (images, favicon, etc.)
- `config.toml` — Site configuration
- `publish_to_gh_pages.sh` — Deployment script

---

## 🏁 Getting Started

1. **Clone the repo:**
   ```bash
   git clone https://github.com/SFang-cmd/hugo-mock-landing-page.git
   cd hugo-mock-landing-page
   ```
2. **Install Hugo:**  
   [Installation guide](https://gohugo.io/getting-started/installing/)
3. **Start the local server:**
   ```bash
   hugo server
   ```
   Then visit [http://localhost:1313](http://localhost:1313).

4. **Deploy:**  
   Push to `main`. GitHub Actions handles the rest!

---

## 📝 Customization

- Edit `config.toml` for site metadata, navigation, and theme options.
- Update content in `content/`.
- Customize templates in `layouts/`.
- See `themes/hugo-bootstrap-theme/README.md` for theme documentation.

---

## 👤 Contact

- **Developer:** Sean Fang
- **Email:** [sefang@seas.upenn.edu](mailto:sefang@seas.upenn.edu)
- **GitHub:** [sfang-cmd](https://github.com/sfang-cmd)
- **LinkedIn:** [sefang](https://www.linkedin.com/in/sefang/)

---

## 🔒 Privacy

See [`content/privacy-policy.md`](./content/privacy-policy.md):  
No cookies, no personal data collected.

---

## 📜 License

This website and its content are © 2025 Sean Fang.  
The Hugo Bootstrap Theme is MIT licensed.

---

*Made with ❤️ using Hugo, Bootstrap, and the help of Claude and ChatGPT.*
