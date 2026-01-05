# Art by Jennefer Ann - Portfolio Website

A modern, responsive portfolio website showcasing the artistic work of Jennefer Ann. This portfolio features a beautiful gallery interface, admin dashboard for content management, and seamless deployment to Netlify.

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Setup Instructions](#setup-instructions)
- [Development](#development)
- [Admin Dashboard](#admin-dashboard)
- [Deployment Guide](#deployment-guide)
- [Environment Variables](#environment-variables)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)

## 🎨 About

Art by Jennefer Ann is a professional portfolio website designed to showcase artistic work in an elegant and user-friendly manner. The site features:

- **Portfolio Gallery**: Display of artwork with detailed descriptions
- **Admin Dashboard**: Easy management of portfolio content without coding knowledge
- **Responsive Design**: Optimized for mobile, tablet, and desktop viewing
- **Fast Performance**: Optimized for speed and SEO
- **Content Management**: Simple interface to add, edit, and delete artwork

## ✨ Features

- 🖼️ **Dynamic Gallery**: Beautiful image gallery with lightbox functionality
- 👤 **Admin Dashboard**: Intuitive content management system
- 📱 **Responsive Design**: Mobile-first approach
- 🔍 **SEO Optimized**: Built-in SEO best practices
- ⚡ **Fast Loading**: Optimized images and lazy loading
- 🎯 **Category Management**: Organize artwork by categories
- 💬 **Contact Integration**: Integrated contact form
- 📊 **Analytics Ready**: Built for Google Analytics integration

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **Static Site Generator**: [Your SSG - e.g., Hugo, Jekyll, 11ty]
- **Hosting**: Netlify
- **CMS**: Netlify CMS / Decap CMS
- **Package Manager**: npm
- **Build Tool**: [e.g., Webpack, Parcel, Vite]

## 📁 Folder Structure

```
artbyjennefer/
├── README.md                 # This file
├── package.json             # Project dependencies and scripts
├── package-lock.json        # Locked dependency versions
├── netlify.toml             # Netlify configuration
├── .env.example             # Example environment variables
├── .gitignore               # Git ignore rules
│
├── src/                     # Source files
│   ├── index.html          # Homepage
│   ├── portfolio.html      # Portfolio/gallery page
│   ├── about.html          # About page
│   ├── contact.html        # Contact page
│   │
│   ├── css/                # Stylesheets
│   │   ├── style.css       # Main stylesheet
│   │   ├── responsive.css  # Responsive design styles
│   │   └── variables.css   # CSS custom properties
│   │
│   ├── js/                 # JavaScript files
│   │   ├── main.js         # Main application logic
│   │   ├── gallery.js      # Gallery functionality
│   │   ├── lightbox.js     # Lightbox/modal logic
│   │   └── admin-api.js    # Admin API interactions
│   │
│   ├── images/             # Static images
│   │   ├── logo.svg        # Logo
│   │   ├── icons/          # Icon files
│   │   └── placeholder/    # Placeholder images
│   │
│   └── assets/             # Other assets
│       └── fonts/          # Custom fonts
│
├── admin/                  # Admin dashboard
│   ├── index.html         # Admin dashboard main page
│   ├── config.yml         # CMS configuration (if using Netlify CMS)
│   ├── css/               # Admin styles
│   └── js/                # Admin scripts
│
├── content/               # Dynamic content
│   ├── portfolio/         # Portfolio items/artwork
│   │   ├── piece-1.md
│   │   ├── piece-2.md
│   │   └── ...
│   ├── categories.json    # Category definitions
│   └── settings.json      # Global settings
│
├── functions/             # Netlify Functions (serverless)
│   ├── contact.js        # Contact form handler
│   └── portfolio.js      # Portfolio data API
│
├── public/               # Build output (generated)
│   └── ...
│
└── docs/                 # Documentation
    ├── SETUP.md          # Setup instructions
    ├── DEPLOYMENT.md     # Deployment guide
    └── API.md            # API documentation
```

## 🚀 Setup Instructions

### Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)
- Git
- A GitHub account
- A Netlify account (for deployment)

### Local Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/jono420dante-art/artbyjennefer.git
   cd artbyjennefer
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Create Environment File**
   ```bash
   cp .env.example .env.local
   ```
   
   Edit `.env.local` with your configuration:
   ```
   VITE_API_URL=http://localhost:3000
   VITE_SITE_NAME=Art by Jennefer Ann
   VITE_CONTACT_EMAIL=your-email@example.com
   ```

4. **Start Development Server**
   ```bash
   npm run dev
   ```
   
   The site will be available at `http://localhost:3000` (or your configured port)

5. **Build for Production**
   ```bash
   npm run build
   ```

### Recommended VSCode Extensions

- Live Server
- Prettier - Code formatter
- ESLint
- CSS Peek
- HTML Snippets

## 💻 Development

### Available Commands

```bash
# Start development server with hot reload
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Run linting
npm run lint

# Format code with Prettier
npm run format

# Deploy to Netlify
npm run deploy
```

### Development Workflow

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Make your changes
3. Test locally: `npm run dev`
4. Build test: `npm run build`
5. Commit and push: `git commit -am "Description"` and `git push origin feature/your-feature`
6. Create a Pull Request

### Adding New Artwork

1. Add image files to `src/images/portfolio/`
2. Create a markdown file in `content/portfolio/` with metadata:
   ```markdown
   ---
   title: "Artwork Title"
   category: "Paintings"
   year: 2024
   description: "Detailed description of the artwork"
   image: "/images/portfolio/artwork.jpg"
   featured: true
   ---
   
   Additional notes or story about the artwork...
   ```
3. Rebuild the site: `npm run build`

## 🎛️ Admin Dashboard

### Accessing the Admin Dashboard

1. Navigate to `/admin` on your live site (or `http://localhost:3000/admin` locally)
2. Sign in with your Netlify credentials (configured during Netlify setup)

### Admin Features

#### Portfolio Management
- **Add Artwork**: Upload images and add artwork details
- **Edit**: Modify existing artwork information
- **Delete**: Remove artwork from portfolio
- **Featured**: Mark artwork as featured on homepage
- **Categories**: Organize by art style or medium

#### Settings
- **Site Name**: Update portfolio site title
- **About Section**: Edit biography and description
- **Contact Information**: Manage contact details
- **Social Links**: Update social media profiles

#### Media Library
- **Upload**: Add new images
- **Organize**: Create folders and organize assets
- **Optimize**: Automatic image optimization

#### User Management
- **Add Users**: Invite collaborators (admin plan required)
- **Roles**: Assign editor or admin roles
- **Permissions**: Control what users can edit

### CMS Configuration

The admin dashboard uses Netlify CMS (Decap CMS). Configuration is in `admin/config.yml`:

```yaml
backend:
  name: github
  repo: jono420dante-art/artbyjennefer
  branch: main
  
publish_mode: editorial_workflow

media_folder: "src/images/uploads"
public_folder: "/images/uploads"

collections:
  - name: "portfolio"
    label: "Portfolio"
    folder: "content/portfolio"
    create: true
    slug: "{{slug}}"
    fields:
      - { label: "Title", name: "title", widget: "string" }
      - { label: "Category", name: "category", widget: "select", options: ["Paintings", "Drawings", "Sculptures", "Digital Art"] }
      - { label: "Year", name: "year", widget: "number" }
      - { label: "Description", name: "description", widget: "text" }
      - { label: "Featured Image", name: "image", widget: "image" }
      - { label: "Featured", name: "featured", widget: "boolean", default: false }
```

### Tips for Admin Use

- ✅ Always save drafts before publishing
- ✅ Use preview to check how artwork appears
- ✅ Optimize images before uploading (recommended max 2MB)
- ✅ Use descriptive titles and categories
- ✅ Add alt text to all images for accessibility
- ✅ Keep descriptions concise and engaging

## 📦 Deployment Guide

### Deploying to Netlify

#### Method 1: GitHub Integration (Recommended)

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Connect to Netlify**
   - Go to [netlify.com](https://netlify.com)
   - Sign up or log in
   - Click "New site from Git"
   - Select GitHub and authorize Netlify
   - Choose your repository: `artbyjennefer`
   - Confirm build settings:
     - **Build command**: `npm run build`
     - **Publish directory**: `public` (or `dist`)
     - **Node version**: 18.x or higher

3. **Environment Variables**
   - In Netlify dashboard: Settings → Build & deploy → Environment
   - Add your environment variables:
     ```
     VITE_API_URL=https://yourdomain.com
     VITE_SITE_NAME=Art by Jennefer Ann
     VITE_CONTACT_EMAIL=your-email@example.com
     ```

4. **Deploy**
   - Netlify will automatically deploy when you push to main branch
   - View deployment status in the Netlify dashboard

#### Method 2: Netlify CLI

1. **Install Netlify CLI**
   ```bash
   npm install -g netlify-cli
   ```

2. **Login to Netlify**
   ```bash
   netlify login
   ```

3. **Deploy**
   ```bash
   netlify deploy --prod
   ```

### Configuring Custom Domain

1. **In Netlify Dashboard**
   - Domain management → Custom domains
   - Add your domain (e.g., artbyjennefer.com)

2. **Update DNS Records**
   Follow Netlify's instructions for your domain registrar

3. **Enable HTTPS**
   - Netlify automatically provisions SSL certificate
   - Takes 5-24 hours to activate

### Setting Up CMS Authentication

1. **Register OAuth App on GitHub**
   - Go to Settings → Developer settings → OAuth Apps
   - Create a new OAuth application
   - Set Authorization callback URL to: `https://api.netlify.com/auth/done`

2. **Add to Netlify**
   - Site settings → Build & deploy → Deploy key
   - Enter GitHub OAuth credentials from step 1

3. **Enable Admin Dashboard**
   - Push `admin/config.yml` with proper settings
   - Access at: `https://yourdomain.com/admin`

### Continuous Deployment

Automatic deployments are triggered when you:
- Push to the `main` branch
- Merge a pull request
- Update content through the CMS

### Deployment Checklist

- [ ] Environment variables configured
- [ ] Domain connected and DNS updated
- [ ] SSL certificate activated
- [ ] GitHub OAuth app configured
- [ ] Admin dashboard accessible
- [ ] Contact form tested
- [ ] Images optimized
- [ ] SEO meta tags updated
- [ ] Analytics configured
- [ ] Staging site previewed

## 🔐 Environment Variables

Create a `.env.local` file in the root directory:

```env
# Site Configuration
VITE_SITE_NAME=Art by Jennefer Ann
VITE_SITE_URL=https://artbyjennefer.com
VITE_SITE_DESCRIPTION=Professional art portfolio

# API Configuration
VITE_API_URL=http://localhost:3000
VITE_API_KEY=your_api_key_here

# Contact Configuration
VITE_CONTACT_EMAIL=jennefer@example.com
VITE_CONTACT_PHONE=+1 (555) 123-4567

# Services
VITE_ANALYTICS_ID=G-XXXXXXXXXX
VITE_FORM_SERVICE=netlify

# Feature Flags
VITE_ENABLE_COMMENTS=false
VITE_ENABLE_NEWSLETTER=true
```

### Environment Variables Reference

| Variable | Purpose | Required |
|----------|---------|----------|
| `VITE_SITE_NAME` | Website title | Yes |
| `VITE_SITE_URL` | Base URL for SEO | Yes |
| `VITE_CONTACT_EMAIL` | Inquiry email address | Yes |
| `VITE_ANALYTICS_ID` | Google Analytics tracking | No |
| `VITE_API_URL` | Backend API endpoint | No |

## 🔧 Troubleshooting

### Common Issues

#### Build Fails on Netlify
```
Error: Missing environment variable
```
**Solution**: Check that all required environment variables are set in Netlify Settings → Environment

#### Admin Dashboard Not Loading
```
Error: Admin dashboard blank or 404
```
**Solutions**:
- Verify `admin/index.html` and `admin/config.yml` exist
- Check GitHub OAuth configuration
- Clear browser cache (Ctrl+Shift+Del)
- Check browser console for errors (F12)

#### Images Not Showing
```
Images appear as broken links
```
**Solutions**:
- Verify image paths in markdown files
- Check that images are in `src/images/` folder
- Ensure images are committed to git
- Rebuild site: `npm run build`

#### Deployment Stuck
```
Build pending for 30+ minutes
```
**Solutions**:
- Clear cache: Netlify Settings → Clear cache and redeploy
- Check build logs for errors
- Verify all dependencies installed: `npm ci`
- Try manual deploy from CLI: `netlify deploy --prod`

#### Form Submissions Not Working
```
Contact form returns error
```
**Solutions**:
- Verify site name in Netlify matches repository
- Check form name attribute: `name="contact"`
- Ensure form has `netlify` attribute
- Test locally first: `npm run dev`
- Check Netlify Forms settings: Forms → View submissions

#### CMS Authentication Failed
```
Netlify CMS shows authorization error
```
**Solutions**:
- Verify GitHub OAuth credentials in Netlify
- Check callback URL matches: `https://api.netlify.com/auth/done`
- Clear browser cookies and try again
- Ensure GitHub repo is public or properly authorized

### Debug Mode

Enable debug logging:
```bash
DEBUG=* npm run dev
```

View detailed build logs:
1. Netlify Dashboard → Deploys
2. Click on failed deploy
3. Scroll to "Build log"

### Performance Debugging

Check Lighthouse score:
1. Open site in Chrome
2. Press F12 → Lighthouse
3. Click "Analyze page load"

Optimize images:
- Use WebP format
- Compress before uploading
- Use appropriate dimensions
- Implement lazy loading

## 🤝 Contributing

### Code Style

- Use Prettier for formatting: `npm run format`
- Follow ESLint rules: `npm run lint`
- Use meaningful variable names
- Add comments for complex logic

### Git Workflow

1. **Create Feature Branch**
   ```bash
   git checkout -b feature/descriptive-name
   ```

2. **Make Changes**
   - Keep commits atomic and descriptive
   - Reference issues: `Fixes #123`

3. **Submit Pull Request**
   - Provide clear description
   - Link related issues
   - Request review from maintainers

### Reporting Issues

Include:
- What you expected to happen
- What actually happened
- Steps to reproduce
- Screenshots/error logs
- Your environment (OS, browser, Node version)

## 📚 Additional Resources

- [Netlify Documentation](https://docs.netlify.com)
- [Netlify CMS Documentation](https://decapcms.org)
- [MDN Web Docs](https://developer.mozilla.org)
- [CSS Tricks](https://css-tricks.com)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Art by Jennefer Ann**

For inquiries about artwork or commissions, please contact:
- Email: [contact@artbyjennefer.com](mailto:contact@artbyjennefer.com)
- Website: [artbyjennefer.com](https://artbyjennefer.com)

---

**Last Updated**: January 5, 2026

For questions or support, please open an issue on GitHub or contact the repository owner.
