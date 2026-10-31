# Cloud Portfolio — Elijah Davids

[![Astro](https://img.shields.io/badge/Astro-Framework-BC52EE?logo=astro)](https://astro.build/)
[![GitHub](https://img.shields.io/badge/GitHub-Version_Control-181717?logo=github)](https://github.com/Ejahmix/cloud-portfolio)
[![Vercel](https://img.shields.io/badge/Vercel-Deployment-000000?logo=vercel)](https://vercel.com/)

**Live Website:** https://portfolio.elijahdavids.com

**Project Repository:** https://github.com/Ejahmix/cloud-portfolio

## Project Overview

This project is my personal developer portfolio, built to showcase my professional background, technical skills, certifications, and independent projects as I pursue a career in cloud computing and infrastructure engineering.

Beyond serving as an online resume, this project provides hands-on experience with modern web development, Git-based version control, automated deployments, custom-domain configuration, and DNS management.

## Technology Stack

| Technology | Purpose |
|---|---|
| Astro | Static site generation and frontend framework |
| Tailwind CSS | Responsive design and styling |
| HTML / CSS | Page structure and presentation |
| Git | Local version control |
| GitHub | Source code hosting and repository management |
| Vercel | Website hosting and automated deployment |
| Cloudflare | DNS management for the custom domain |
| VS Code | Development environment |

## Architecture

The website uses a Git-based deployment workflow:

```text
Developer (VS Code)
        |
        v
   Git Repository
        |
        | git push
        v
      GitHub
        |
        | Connected repository
        v
      Vercel
        |
        | Build and deploy
        v
   Astro Static Website
        |
        | Custom domain DNS
        v
     Cloudflare
        |
        v
portfolio.elijahdavids.com
```

**Deployment workflow:**

1. Develop and test changes locally using Astro.
2. Track and commit changes using Git.
3. Push committed changes to the GitHub repository.
4. Vercel detects updates to the connected production branch.
5. Vercel builds and deploys the Astro website.
6. Visitors access the deployed website using the custom domain, with DNS managed through Cloudflare.

## Key Features

- Responsive, dark-themed Modern Developer portfolio.
- Professional experience, technical skills, and certifications.
- Dedicated project case-study pages.
- Links to GitHub, LinkedIn, and professional contact information.
- Custom domain configuration.
- Automated deployments from GitHub through Vercel.

## Local Development

### Prerequisites

- Node.js
- npm
- Git

### Installation

Clone the repository:

```bash
git clone https://github.com/Ejahmix/cloud-portfolio.git
```

Navigate into the project:

```bash
cd cloud-portfolio
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open `http://localhost:4321` in your browser.

### Production Build

Generate the production-ready static website:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Deployment

The portfolio is deployed through Vercel using a GitHub-connected deployment workflow.

The repository's `main` branch is used for production deployments.

To publish changes:

```bash
git status
git add .
git commit -m "Describe the changes"
git push origin main
```

Vercel automatically starts a new deployment when changes are pushed to the connected production branch.

### Custom Domain

The portfolio uses the custom domain:

`portfolio.elijahdavids.com`

Cloudflare manages the domain's DNS records, including the CNAME record that directs the portfolio subdomain to Vercel.

Vercel handles hosting and HTTPS for the deployed website.

## Challenges and Lessons Learned

### 1. Git Version Control

**Challenge:** Understanding the difference between committing changes locally and publishing those changes to GitHub.

**Resolution:** Used `git status` to identify when the local branch was ahead of the remote branch, then used `git push origin main` to synchronize the repository.

**Lesson:** A successful Git commit does not automatically update the remote repository or trigger a deployment.

### 2. Astro File-Based Routing

**Challenge:** Troubleshooting a project case-study page that initially displayed a blank screen.

**Resolution:** Verified the route and tested the page with minimal Astro markup before restoring the intended content.

**Lesson:** Isolating routing, markup, and styling issues helps identify problems systematically.

### 3. DNS Configuration

**Challenge:** Connecting a custom portfolio subdomain to a Vercel-hosted application.

**Resolution:** Configured the appropriate DNS record in Cloudflare using the target supplied by Vercel.

**Lesson:** DNS records, domain verification, and hosting configuration must work together to make a custom domain accessible.

## Future Improvements

The following enhancements are planned but are not part of the current deployment:

- Deploy an alternative static hosting environment using Amazon S3 and CloudFront.
- Configure secure AWS deployments using GitHub Actions and IAM OIDC.
- Manage cloud resources using Terraform.
- Explore monitoring and observability with AWS CloudWatch.
- Develop and document additional independent cloud infrastructure projects.

## About Me

**Elijah Davids**

AWS Certified Cloud Practitioner | CompTIA Network+ Certified

Bachelor of Applied Science in Computing Technology & Software Development — Cloud Computing concentration, Valencia College (Expected May 2027).

Interested in cloud infrastructure, networking, cloud operations, and technical problem-solving.

**Portfolio:** https://portfolio.elijahdavids.com

**GitHub:** https://github.com/Ejahmix

**LinkedIn:** https://www.linkedin.com/in/elijahdavids/

**Email:** contact@elijahdavids.com
