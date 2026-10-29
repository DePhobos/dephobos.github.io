# bakhtin.dev

Personal portfolio and resume site for Gleb Bakhtin, DevOps / SRE Engineer. 
Live at **[bakhtin.dev](https://bakhtin.dev)**.

A single static HTML page: no frameworks, no build step, no dependencies. It's hosted on GitHub Pages with a custom domain and deployed by GitHub Actions on every push to `main`.


## Structure

```
.
├── index.html                   # the whole site: markup, styles, scripts
├── og.png                       # 1200×630 link preview image
├── resume-en.pdf                # resume, English
├── resume-ru.pdf                # resume, Russian
├── CNAME                        # custom domain: bakhtin.dev
└── .github/workflows/deploy.yml # deploy to GitHub Pages
```

## 🛠️ Architecture & Stack
- **Frontend:** Vanilla HTML/CSS/JS. No frameworks, no build step. This ensures the site loads instantly and has a zero attack surface.
- **Infrastructure:** GitHub Pages.
- **CI/CD:** GitHub Actions. Deployments are triggered strictly via Pull Requests to the `main` branch (Branch Protection is enabled).
- **Domain & Security:** Custom domain `bakhtin.dev` managed via Porkbun. SSL/TLS is automated by GitHub Pages.

## Deploy

Every push to `main` runs the workflow, which:

1. replaces `__DEPLOY_DATE__` and `__COMMIT_SHA__` in `index.html` with the current date and short commit hash;
2. uploads the repository as a Pages artifact;
3. deploys it to GitHub Pages.

Keep both placeholders in `index.html` exactly as written, or the footer will show them as plain text.



## Contact

[Telegram](https://t.me/AstraProxima) · [LinkedIn](https://www.linkedin.com/in/astraproxima/) · [gleb@bakhtin.dev](mailto:gleb@bakhtin.dev)
