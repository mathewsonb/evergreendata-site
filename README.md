# Evergreen Data Architects — Portfolio & Platform

Official source code for [evergreendata.me](https://evergreendata.me), the professional consulting portfolio for **Evergreen Data Architects**. Built with **Hugo Extended**, styled using custom Bootstrap/CSS overrides, and deployed automatically via **GitHub Actions**.

---

## Purpose & Features

* **Data Engineering Focus:** Highlights capabilities across End-to-End ETL/ELT pipelines, Data Warehousing, Modeling, BI Dashboards, and Enterprise Data Architecture.
* **Interactive Contact Inquiries:** Custom serverless modal powered by Web3Forms for direct lead acquisition, featuring client-side form validation and honeypot spam protection.
* **Resume Delivery:** Integrated direct-download resume hosted locally and version-controlled.
* **Mobile-First Responsive Layout:** Clean typography with custom padding, tight hero section spacing, and removed theme clutter.

---

## Architecture & Tech Stack

| Layer | Technology / Service |
| :--- | :--- |
| **Static Site Generator** | [Hugo (Extended Edition)](https://gohugo.io/) `v0.120+` |
| **Base Theme** | [Hugo Profile](https://github.com/gohugo-theme-profile/hugo-profile) (Git Submodule) |
| **Frontend Framework** | Bootstrap 5, Custom CSS (`assets/css/custom.css`) |
| **Contact Backend** | Web3Forms Serverless API |
| **Hosting & CI/CD** | GitHub Pages & GitHub Actions Workflow |

---

## Repository Structure

Custom layout overrides are stored in the project root `layouts/` directory to preserve the theme submodule integrity and ensure seamless deployment pipelines.

```text
evergreendata-site/
├── .github/
│   └── workflows/
│       └── deploy.yaml     # GitHub Actions deployment pipeline
├── assets/
│   └── css/
│       └── custom.css      # Layout overrides & hero section spacing fixes
├── layouts/
│   └── partials/
│       └── sections/
|           └── contact.html        # Custom Web3Forms inquiry modal override
├── public/
|   └── bootstrap-5/
|   |   └── css/
|   |   |   └── boostrap.min.css
|   |   |   └── boostrap.min.css.map
|   |   └── js/
|   |       └── boostrap.bundle.js
|   |       └── boostrap.bundle.js.map
|   |       └── boostrap.bundle.min.js
|   |       └── boostrap.bundle.min.js.map
|   └── categories/
|   |   └── page/
|   |   |   └── 1/
|   |   |       └── index.html
|   |   └── index.html
|   |   └── index.xml
|   └── css/
|   |   └── about.css
|   |   └── font.css
|   |   └── footer.css
|   |   └── gallery.css
|   |   └── header.css
|   |   └── index.css
|   |   └── language-switcher.css
|   |   └── list.css
|   |   └── projects.css
|   |   └── single.css
|   |   └── theme.css
|   └── docs/
|   |   └── Ben_Mathewson_Resume.pdf
|   └── fontawesome-6/
|   |   └── svgs/
|   |   |   └── brands/
|   |   |   |   └── ...
|   |   |   └── regular/
|   |   |   |   └── ...
|   |   |   └── solid/
|   |   |       └── ...
|   |   └── all-6.4.2.js
|   └── images/
|   |   └── projects/
|   |       └── ...
|   └── js/
|   |   └── contact.js
|   |   └── readingTime.js
|   |   └── scrollProgressBar.js
|   |   └── search.js
|   └── tags/
|   |   └── page/
|   |   |   └── 1/
|   |   |       └── index.html
|   |   └── index.html
|   |   └── index.xml
|   └── viewer/
|   |   └── viewer.min.css
|   |   └── viewer.min.js
|   └── 404.html
|   └── 404.png
|   └── fav.png
|   └── index.html
|   └── index.xml
|   └── sitemap.xml
├── themes/
│   └── hugo-profile/       # Unmodified Git submodule theme (not to update)
└── hugo.yaml       # Primary site configuration