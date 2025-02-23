# Hugo Mock Landing Page

## 📌 Project Overview

**Hugo Mock Landing Page** is a modern and responsive **rental booking website** built using **Hugo**, a fast and flexible static site generator. The platform is designed to provide users with an intuitive experience for **booking and listing rental properties** efficiently.

This project incorporates **pre-designed UI/UX components** sourced from **CodePen.io** and other modern design inspirations to ensure an elegant and visually appealing layout.

## 🌟 Features

- **Fast & Lightweight** – Powered by Hugo for optimized performance.
- **Pre-made UI/UX Components** – Integrated from CodePen and other modern designs.
- **Secure Booking & Payments** – Provides a seamless rental experience.
- **Responsive Design with Bootstrap 5** – Ensures mobile and desktop compatibility.
- **Three.js Animation** – Adds an interactive **visual animation in the masthead**.
- **Dynamic Content Management** – Easily manage pages, posts, and content with Hugo.
- **SEO-Optimized** – Designed with clean HTML and structured metadata

---

## 🛠️ Installation & Setup

**1⃣ Prerequisites**
Before running the site locally, ensure you have the following installed:

- [Hugo](https://gohugo.io/getting-started/installing/) (Extended version recommended)
- [Git](https://git-scm.com/)
- A modern web browser (Chrome, Firefox, Edge, Safari)

**2⃣ Clone the Repository**
To get started, clone the project from GitHub:
```sh
git clone https://github.com/christianishimwe/hugo-mock-landing-page.git
cd hugo-mock-landing-page
```

**3⃣ Run Hugo Server**
Start a local development server using:

```sh
hugo server
 ``` 

**4⃣ Editing Content**

- All site content is stored inside the `content/` directory.
- You can create new pages using:
```sh
hugo new content/page-name.md
```
- To edit site settings, modify the `config.toml` file.

**5⃣ Building the Site**
To generate static files for deployment, run:
```sh
hugo
```
This will output the generated files in the `public/` folder.

---

** 🎨 UI/UX Design & Inspiration
This project includes **pre-designed** UI elements and inspirations from:
**CodePen.io** – Various creative UI components.
**Bootstrap 5** – For a modern, responsive layout.
**Three.js** – Adds an interactive animation to the landing page.
**Custom CSS & Animations** – Fine-tuned for a polished user experience.

---

**👨‍💻 Contribution Guidelines
Interested in contributing? Follow these steps:

1. **Fork the repository**
2. **Create a new branch** (`git checkout -b feature-new`)
3. **Make your changes**
4. **Commit changes** (`git commit -m "Added new feature"`)
5. **Push to your branch** (`git push origin feature-new`)
6. **Open a Pull Request**

---

**📜 License
This project is licensed under the **MIT License** – feel free to modify and use it as needed.

---

**✨ Credits & Acknowledgments
**UI Components** – Adapted from CodePen.io and other modern designs.
**Built with Hugo** – For fast and efficient website generation.
**Three.js Animation** – Enhancing user interaction with dynamic visuals.

---

**📞 Contact
For inquiries or contributions:
**Email:** christianishimwe2003@gmail.com
**Website:** [lalastays.com](https://lalastays.com)
**GitHub:** [christianishimwe](https://github.com/christianishimwe)

---

🚀 **Enjoy using Hugo Mock Landing Page – The easiest way to create a modern, static landing page!**

#####################################################################################################################

# Hugo Website Deployment Workflow

This repository uses GitHub Actions to automatically build and deploy a Hugo website to GitHub Pages.

## 🔄 Workflow Overview

The workflow (`/.github/workflows/deploy-hugo.yml`) automatically triggers when code is pushed to the `main` branch. It handles the complete process of building and deploying the Hugo website.

## 🛠️ Technical Details

### Prerequisites
- A Hugo website repository
- GitHub Pages enabled for your repository
- Hugo version 0.144.1 (extended version)

### Workflow Steps

1. **Source Code Checkout**
   - Checks out the repository code
   - Includes all submodules (important for Hugo themes)
   - Fetches complete Git history for Hugo's `.GitInfo` and `.Lastmod` features

2. **Hugo Setup**
   - Installs Hugo v0.144.1 (extended version)
   - Configures the Hugo environment

3. **Build Process**
   - Builds the Hugo static files
   - Includes draft content (`-D` flag)
   - Performs garbage collection (`--gc`)
   - Minifies output files for better performance

4. **Deployment**
   - Deploys to the `gh-pages` branch
   - Uses GitHub's automated token system
   - Sets up proper commit attribution

## 🚀 Usage

The workflow runs automatically when you push to the `main` branch. No manual intervention is required.

To modify the workflow:
1. Edit the `.github/workflows/deploy-hugo.yml` file
2. Commit and push your changes to the `main` branch

## ⚙️ Configuration Options

### Hugo Version
```yaml
hugo-version: "0.144.1"
```
Change this value to use a different Hugo version.

### Custom Domain
To use a custom domain, uncomment and modify the following line in the workflow file:
```yaml
## cname: mydomain.com
```

### Draft Content
The `-D` flag in the build command includes draft content. Remove this flag to exclude drafts from the build.

## 📝 Notes

- The workflow uses Ubuntu 22.04 as the running environment
- All actions use specific versions for stability
- The deployment uses GitHub's automated token system for authentication
- Commit messages in the `gh-pages` branch will be attributed to the GitHub Actions bot