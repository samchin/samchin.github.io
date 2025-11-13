# Next Steps - Completing Your Personal Website

Your single-page Bootstrap website is now set up! Here's what you need to do to make it yours:

## 🎯 Immediate Actions

### 1. Add Your Photos

**Profile Photo:**
- Add your headshot as: `dist/assets/images/profile-photo.jpg`
- Should be square (e.g., 600x600px or larger)
- Will be displayed as a circle

**Project Images:**
- Add images to: `dist/assets/images/projects/`
- See the list in `dist/assets/images/projects/README.md`
- Recommended size: 800x600px (4:3 ratio)
- Keep files under 500KB for fast loading

### 2. Update Your Information

Open `dist/index.html` and update:

- **Line 134-137**: Your name and tagline
- **Line 62**: Email address (appears in multiple places - search for `your.email@example.com`)
- **Lines 73-95**: GitHub and LinkedIn URLs
- **Line 106**: CV/resume link
- **Lines 118-144**: Your bio and research interests
- **Footer (line 300)**: Update copyright year/name if needed

### 3. Add Your CV

- Place your CV/resume as: `dist/assets/cv.pdf`
- Or update the link in the HTML if you want to use a different filename

## 🎨 Optional Customizations

### Change Colors

Edit `scss/custom.scss` (lines 8-13):

```scss
$primary: #2c3e50;        // Main dark color
$link-color: #3498db;     // Link blue
```

Then recompile:
```bash
sass --load-path=node_modules scss/custom.scss dist/custom.css
```

### Change Font

1. Pick a font from [Google Fonts](https://fonts.google.com/)
2. Update the `<link>` tag in `dist/index.html` (around line 20)
3. Update `$font-family-sans-serif` in `scss/custom.scss`
4. Recompile CSS

### Modify Project Details

Each project card in `dist/index.html` has:
- Image
- Title
- Description
- Button/link

Update the descriptions, add real paper links, or add/remove projects as needed.

## 📱 Testing

1. **Open the site:**
   ```bash
   open dist/index.html
   ```
   Or just double-click `dist/index.html` in Finder

2. **Test these features:**
   - [ ] Click navigation links (smooth scroll)
   - [ ] Click filter buttons (All, Electronics, Perceptual, Ceramics)
   - [ ] Hover over project cards (should lift up)
   - [ ] Resize browser window (responsive design)
   - [ ] Test on mobile device

3. **Check all links:**
   - [ ] Email links work
   - [ ] Social media links go to your profiles
   - [ ] CV downloads
   - [ ] Paper links work
   - [ ] Workshop/talk links work

## 🚀 Deployment

Once everything looks good, deploy the `dist/` folder:

### Option 1: GitHub Pages
```bash
# From your project root
git add dist/
git commit -m "Add personal website"
git subtree push --prefix dist origin gh-pages
```

### Option 2: Netlify
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the `dist/` folder
3. Done!

### Option 3: Vercel
```bash
cd dist
vercel
```

## 📝 Content Tips

### Bio Section
- Keep it conversational and authentic
- Highlight what makes your work unique
- 2-3 paragraphs is ideal

### Project Descriptions
- 2-3 sentences per project
- Focus on the "why" and impact, not just "what"
- Include years for context

### Research Interests
- 4-6 bullet points
- Be specific but accessible
- Use action-oriented language

## 🐛 Troubleshooting

**Images not showing?**
- Check file paths match exactly (case-sensitive)
- Verify images are in `dist/assets/images/`

**Styles look wrong?**
- Make sure `dist/custom.css` exists
- Try recompiling: `sass --load-path=node_modules scss/custom.scss dist/custom.css`

**Filtering not working?**
- Check browser console for JavaScript errors
- Make sure `js/bootstrap.bundle.min.js` exists

**Smooth scrolling not working?**
- Make sure all section IDs match nav links
- Check that JavaScript at the bottom of `index.html` is intact

## 📧 Questions?

If you run into issues or want to customize something specific, just ask!

---

**Current Status:** ✅ Site structure complete, ready for your content!

