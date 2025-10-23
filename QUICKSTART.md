# Quick Start: Adding Your Strava Project

## What I've Set Up For You

Your portfolio now has a project system! I've created:

1. **`projects/` folder** - Where all your project pages live
2. **Template HTML page** - A styled project page with code blocks (like a rendered notebook)
3. **Template Jupyter notebook** - Start your analysis here
4. **Example Strava project** - Already linked from your main portfolio page

## 3 Ways to Add Your Strava Analysis

### Option 1: Use Jupyter Notebook (Recommended) ⭐

1. **Work in the template notebook:**
   ```bash
   # Open in Cursor
   projects/strava-analysis-template.ipynb
   ```

2. **Add your Strava data and analysis**

3. **Save your plots:**
   ```python
   plt.savefig('images/my_chart.png', dpi=150, bbox_inches='tight')
   ```

4. **Export to HTML:**
   ```bash
   cd projects
   jupyter nbconvert --to html strava-analysis-template.ipynb --output strava-analysis.html
   ```

5. **Done!** The page is already linked from your portfolio

### Option 2: Edit the HTML Template

1. **Open:** `projects/strava-analysis.html`

2. **Replace:**
   - Example code with your actual code
   - Placeholder visualizations with your charts
   - Text with your actual findings

3. **Add images:**
   ```bash
   # Put your chart images in:
   projects/images/
   ```

### Option 3: Quick Deploy (Fastest)

If you already have a Jupyter notebook:

```bash
# Just convert it and drop it in projects/
jupyter nbconvert --to html your_strava_notebook.ipynb
mv your_strava_notebook.html projects/strava-analysis.html
```

## Your Portfolio Structure

```
github_portofilo/
├── index.html                          # Main portfolio page
├── style.css                           # Main styles
├── script.js                          # Main JavaScript
└── projects/                          # All your projects go here
    ├── strava-analysis.html           # Your Strava project page
    ├── project-style.css              # Styling for project pages
    ├── strava-analysis-template.ipynb # Jupyter template
    ├── images/                        # Your visualization images
    └── README.md                      # Detailed guide
```

## Adding More Projects

1. **Copy the template:**
   ```bash
   cp projects/strava-analysis.html projects/new-project.html
   ```

2. **Edit the content**

3. **Add a card in `index.html`:**
   ```html
   <div class="project-card">
       <div class="project-image">
           <img src="YOUR_IMAGE_URL" alt="Project">
           <div class="project-overlay">
               <a href="projects/new-project.html" class="project-link">View Project</a>
           </div>
       </div>
       <div class="project-content">
           <h3 class="project-title">Your New Project</h3>
           <p class="project-description">Description here...</p>
           <div class="project-tags">
               <span class="tag">Python</span>
           </div>
       </div>
   </div>
   ```

## Deploy Your Changes

```bash
git add .
git commit -m "Add Strava analysis project"
git push
```

Your live site will update automatically! 🎉

## Tips

- **Code blocks**: Use syntax highlighting - it's already set up
- **Visualizations**: Save plots at 150 DPI for web
- **Keep it focused**: 5-10 minute read time is ideal
- **Tell a story**: What question? What did you find? Why does it matter?

## Example Workflow

1. Do your analysis in `strava-analysis-template.ipynb`
2. Export to HTML: `jupyter nbconvert --to html ...`
3. Push to GitHub: `git push`
4. Check your live site: `https://ctagg11.github.io`

## Need Help?

- Check `projects/README.md` for detailed instructions
- Look at `projects/strava-analysis.html` for the template example
- The styling is in `projects/project-style.css`

---

**You're all set!** Click on your Strava project card on the main portfolio page to see the template in action.

