# Rashmika Samaranayaka — Portfolio

A personal portfolio website showcasing my full-stack & cloud development projects, technical skills, certifications, and contact details. Built as a single-page, static site with a dark/light theme toggle and fully responsive layout.

**Live Site:** [rashmika-portfolio.s3-website.ap-south-1.amazonaws.com](http://rashmika-portfolio.s3-website.ap-south-1.amazonaws.com)

## Tech Stack

- **HTML5** — semantic page structure
- **CSS3** — custom properties (CSS variables) for theming, CSS Grid & Flexbox for layout, no framework/library used
- **Vanilla JavaScript** — theme toggle, mobile nav, scroll behavior, CV download
- **Google Fonts** — Space Grotesk (display) & Inter (body)

No build tools, bundlers, or package managers are involved — it's a plain static site, so it runs directly in the browser.

## Cloud Concepts Demonstrated

This project is hosted using **AWS S3 Static Website Hosting**:

- The site's static assets (HTML, images, CV) are uploaded to an S3 bucket
- The bucket is configured for **static website hosting**, serving `index.html` as the index document and `404.html` as the custom error document
- Public read access is granted via a bucket policy so the site is reachable over HTTP
- Demonstrates core cloud concepts: object storage (S3), static hosting without a server, and serving content via a regional S3 website endpoint (`ap-south-1`)

## Project Structure

```
Portfolio/
├── index.html      # Main page (all sections + inline styles/scripts)
├── 404.html        # Custom error page for S3 hosting
└── images/         # Photos, project screenshots, CV
```

## Setup / Run Locally

1. Clone the repository
   ```bash
   git clone https://github.com/Rashmika-Sa/portfolio.git
   cd portfolio
   ```
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   npx serve .
   ```

## Deploying to AWS S3

1. Create an S3 bucket (e.g. `rashmika-portfolio`)
2. Enable **Static website hosting** under bucket properties
   - Index document: `index.html`
   - Error document: `404.html`
3. Upload `index.html`, `404.html`, and the `images/` folder to the bucket
4. Attach a bucket policy allowing public `s3:GetObject` access
5. Access the site via the S3 website endpoint shown in the bucket's properties

## Contact

- Email: rurashmika@gmail.com
- GitHub: [github.com/Rashmika-Sa](https://github.com/Rashmika-Sa)
- LinkedIn: [in/ruwan-rashmika](https://www.linkedin.com/in/ruwan-rashmika-2814511b3)
