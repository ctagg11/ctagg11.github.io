# Data Science Portfolio

A clean, modern, and professional portfolio website showcasing data science projects and skills.

## 🌟 Features

- **Responsive Design**: Fully responsive layout that works on all devices
- **Modern UI/UX**: Clean and professional design with smooth animations
- **Project Showcase**: Grid layout to display your data science projects
- **Skills Section**: Organized display of your technical skills
- **Contact Form**: Integrated contact form with Formspree
- **Smooth Scrolling**: Enhanced navigation with smooth scroll effects
- **Mobile-Friendly**: Hamburger menu for mobile devices
- **Performance Optimized**: Fast loading times and optimized assets

## 🚀 Getting Started

### Prerequisites

- A GitHub account
- Git installed on your local machine (optional, for local development)

### Setup Instructions

1. **Clone or Download** this repository to your local machine

2. **Customize Your Content**:
   - Open `index.html` and update:
     - Your name in the hero section
     - Project descriptions, titles, and links
     - Skills and technologies
     - Contact information (email, LinkedIn, GitHub)
     - Social media links
   
3. **Update Images**:
   - Replace placeholder images with your own project screenshots
   - Store images in an `images/` folder or use external URLs
   
4. **Configure Contact Form**:
   - Sign up for [Formspree](https://formspree.io/) (free)
   - Replace `YOUR_FORM_ID` in the form action with your Formspree endpoint
   - Or use an alternative form service like Netlify Forms

5. **Deploy to GitHub Pages**:
   - Create a new repository named `USERNAME.github.io` (replace USERNAME with your GitHub username)
   - Push your code to the repository
   - Go to repository Settings → Pages
   - Select the branch to deploy (usually `main` or `master`)
   - Your site will be live at `https://USERNAME.github.io`

## 📁 File Structure

```
.
├── index.html          # Main HTML file
├── style.css           # CSS stylesheet
├── script.js           # JavaScript file
├── README.md           # This file
└── images/            # (Create this folder for your images)
```

## 🎨 Customization

### Colors

Update the CSS variables in `style.css` to match your brand:

```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #64748b;
    --accent-color: #0ea5e9;
    /* ... more colors */
}
```

### Projects

Add or remove project cards in the `projects-grid` section of `index.html`. Each project follows this structure:

```html
<div class="project-card">
    <div class="project-image">
        <img src="your-image.jpg" alt="Project Name">
        <div class="project-overlay">
            <a href="project-link" class="project-link">View Project</a>
        </div>
    </div>
    <div class="project-content">
        <h3 class="project-title">Project Title</h3>
        <p class="project-description">Description...</p>
        <div class="project-tags">
            <span class="tag">Technology</span>
        </div>
    </div>
</div>
```

### Skills

Update the skills sections in `index.html` to reflect your expertise. Add or remove skill categories as needed.

## 🛠️ Technologies Used

- HTML5
- CSS3 (with CSS Variables)
- Vanilla JavaScript
- Google Fonts (Inter)
- Intersection Observer API
- Formspree (for contact form)

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🎯 SEO Tips

1. Update the `<meta name="description">` tag in `index.html`
2. Add relevant keywords to your project descriptions
3. Use descriptive alt text for all images
4. Consider adding a sitemap.xml
5. Submit your site to Google Search Console

## 📈 Analytics (Optional)

To track visitors, add Google Analytics:

1. Sign up for Google Analytics
2. Get your tracking ID
3. Add the tracking code to the `<head>` section of `index.html`

## 🤝 Contributing

Feel free to fork this repository and customize it for your own use. If you make improvements, pull requests are welcome!

## 📄 License

This project is open source and available under the MIT License.

## 📧 Contact

If you have questions or suggestions, feel free to reach out:

- GitHub: [@ctagg11](https://github.com/ctagg11)
- Email: your.email@example.com

## 🙏 Acknowledgments

- Images from [Unsplash](https://unsplash.com)
- Icons from inline SVGs
- Fonts from [Google Fonts](https://fonts.google.com)

---

**Happy coding! 🚀**

