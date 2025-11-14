# Sam Chin - Personal Website

A modern, minimalist single-page portfolio website built with Bootstrap 5.

## Features

- **Single-page design** with smooth scrolling navigation
- **Responsive layout** that works on desktop, tablet, and mobile
- **Project filtering** by category (Electronics, Perceptual Augmentation, Ceramics)
- **Minimalist design** with clean typography and generous white space
- **Interactive elements** with hover effects and fade-in animations

## Structure

### Sections

1. **Hero/About** - Profile photo, bio, social links, and research interests
2. **Projects** - Filterable grid of project cards with descriptions and links
3. **Talks & Workshops** - Event cards with roles and links
4. **Contact** - Social links and email
5. **Footer** - Copyright and back-to-top link

### File Organization

```
baochip-site/
├── dist/                          # Production files (deploy this folder)
│   ├── index.html                 # Main single-page site
│   ├── custom.css                 # Compiled CSS (generated from SCSS)
│   ├── js/
│   │   └── bootstrap.bundle.min.js
│   └── assets/
│       └── images/
│           ├── profile-photo.jpg  # Your headshot (add this)
│           ├── projects/          # Project images (add these)
│           └── favicon/           # Favicon files
├── scss/
│   └── custom.scss                # Source styles (edit this)
├── package.json
└── README.md
```

## Setup & Development

### Prerequisites

- Node.js and npm installed
- Sass compiler

### Installation

1. Install dependencies:
```bash
npm install
```

### Making Style Changes

1. Edit `scss/custom.scss` to customize colors, fonts, spacing, etc.

2. Compile SCSS to CSS:
```bash
sass --load-path=node_modules scss/custom.scss dist/custom.css
```

3. Open `dist/index.html` in your browser to preview changes

### Customization Guide

#### Update Personal Information

Edit `dist/index.html` and replace:
- Your name and tagline
- Bio text and research interests
- Email address (search for `mailto:your.email@example.com`)
- Social media links (GitHub, LinkedIn)
- CV link (`assets/cv.pdf`)

#### Add Your Photos

1. Add your profile photo as `dist/assets/images/profile-photo.jpg`
   - Recommended: Square aspect ratio, at least 600x600px

2. Add project images to `dist/assets/images/projects/`
   - See `dist/assets/images/projects/README.md` for the full list
   - Recommended: 800x600px (4:3 ratio), under 500KB each

#### Customize Colors

Edit `scss/custom.scss` and change these variables:

```scss
$primary: #2c3e50;        // Main color (navbar, headings)
$link-color: #3498db;     // Link color
$link-hover-color: #2980b9;
```

Then recompile the CSS.

#### Customize Fonts

The site uses Inter font by default. To change:

1. Update the Google Fonts link in `dist/index.html`
2. Update `$font-family-sans-serif` in `scss/custom.scss`
3. Recompile CSS

## Deployment

The site is automatically deployed to GitHub Pages using GitHub Actions.

### GitHub Pages (Current Setup)

- **Automatic deployment**: The site automatically deploys from the `dist/` folder whenever you push to the `master` branch
- **Workflow**: Located at `.github/workflows/deploy.yml`
- **Site URL**: https://samchin.github.io/
- **Setup**: GitHub Pages is configured to use GitHub Actions (Settings → Pages → Source: GitHub Actions)

### Other Hosting Options

- **Netlify**: Drag and drop the `dist/` folder
- **Vercel**: Deploy the `dist/` folder
- **Any web host**: Upload the `dist/` folder contents via FTP

## Browser Support

- Chrome, Firefox, Safari, Edge (latest versions)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Technologies Used

- Bootstrap 5.3.7
- Sass 1.89.2
- Vanilla JavaScript (no frameworks)
- Google Fonts (Inter)

## License

Feel free to use this template for your own personal website.
