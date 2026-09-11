# Skill Pass Academy Website

Official website for Skill Pass Academy - Language & Test Preparation institute in Kathmandu, Nepal.

## Live Site
https://skillpassacad.com

## Tech Stack
- Static HTML/CSS/JS (no build step)
- Hosted on GitHub Pages
- Custom domain via Cloudflare
- EmailJS for contact form submissions

## Setup

### Before deploying, configure EmailJS (contact form)
1. Create a free account at [emailjs.com](https://www.emailjs.com)
2. Add an Email Service connected to skillpassa@gmail.com
3. Create an email template with these fields: `from_name`, `from_email`, `from_phone`, `course_interest`, `message`
4. In `index.html`, replace:
   - `YOUR_PUBLIC_KEY` (top of the script) with your EmailJS public key
   - `YOUR_SERVICE_ID` and `YOUR_TEMPLATE_ID` with your credentials

### Deploy to GitHub Pages
1. Create a new repository on GitHub named `skillpass-academy` (or anything you prefer)
2. Push or upload these files to the repository
3. Go to Settings > Pages and set Source to `Deploy from a branch` > `main` > `/ (root)`
4. Add a custom domain of `skillpassacad.com` in the Pages settings
5. Enable "Enforce HTTPS"

### DNS Configuration (Cloudflare)
Add these records in Cloudflare for skillpassacad.com:

| Type  | Name  | Value                                       |
|-------|-------|---------------------------------------------|
| A     | @     | 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 |
| AAAA  | @     | 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153 |
| CNAME | www   | bijay-afk.github.io                         |

> Note: Do NOT enable Cloudflare's orange-cloud proxy for the A/AAAA records if you want the CNAME-based custom domain in GitHub Pages to work properly - set these to DNS only (grey cloud).

## Project Structure
```
├── index.html       # Main landing page
├── 404.html         # Custom 404 page
├── CNAME            # GitHub Pages custom domain
├── robots.txt       # SEO
└── assets/
    └── logo.png     # Academy logo
```

## Contact
- Phone: +977-9801362575
- Email: skillpassa@gmail.com
- Address: Kaikasthan, Kathmandu 29