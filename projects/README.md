# How to Add Your Projects

This guide explains how to add your actual project content to your portfolio.

## Option 1: Convert Jupyter Notebook to HTML (Recommended)

If you have a Jupyter notebook with your Strava analysis, you can convert it to HTML and use it directly:

### Method A: Export from Jupyter/Cursor

1. **In Jupyter or Cursor with Jupyter extension:**
   ```bash
   jupyter nbconvert --to html your_notebook.ipynb --output strava-analysis.html
   ```

2. **Move the generated HTML to the projects folder:**
   ```bash
   mv strava-analysis.html projects/
   ```

3. **Optional: Clean up the styling** by adding this to the `<head>` section:
   ```html
   <link rel="stylesheet" href="project-style.css">
   <style>
       body { max-width: 900px; margin: 80px auto; padding: 0 2rem; }
       /* Add back button */
       body::before {
           content: "← Back to Portfolio";
           display: block;
           margin-bottom: 2rem;
           color: #2563eb;
       }
   </style>
   ```

### Method B: Use nbviewer (Quick & Easy)

1. **Upload your notebook to GitHub** in a repository
2. **Go to:** https://nbviewer.org/
3. **Paste your GitHub notebook URL**
4. **Copy the nbviewer link** and use it in your portfolio:
   ```html
   <a href="https://nbviewer.org/github/ctagg11/your-repo/blob/main/strava_analysis.ipynb">
   ```

## Option 2: Use the Template I Created

I've created a template at `projects/strava-analysis.html` that looks like a rendered notebook. Here's how to customize it:

### 1. Replace the Content

Edit `projects/strava-analysis.html` and replace:
- **Title**: Change "Analyzing My Strava Running Data"
- **Overview section**: Add your intro text
- **Code blocks**: Replace example code with your actual code
- **Output blocks**: Add your actual outputs

### 2. Add Your Visualizations

Replace the placeholder sections with your actual charts:

```html
<!-- Replace this: -->
<div class="viz-placeholder">
    <p>📊 <em>Visualization: Weekly mileage trend</em></p>
</div>

<!-- With this: -->
<img src="images/weekly_mileage.png" alt="Weekly Mileage Chart" style="width: 100%; border-radius: 8px;">
```

### 3. Save Your Plots

In your Jupyter notebook or Python script:

```python
# Save plots to the projects/images folder
import matplotlib.pyplot as plt

plt.figure(figsize=(12, 6))
# ... your plotting code ...
plt.savefig('../projects/images/weekly_mileage.png', dpi=150, bbox_inches='tight')
plt.show()
```

Create the images folder:
```bash
mkdir -p projects/images
```

## Option 3: Embed Live Notebook (Advanced)

You can use Google Colab or Kaggle to host interactive notebooks:

1. **Upload to Google Colab**
2. **Set sharing to "Anyone with link"**
3. **Get embed link**: File → Share → Copy link
4. **Use iframe in your HTML:**

```html
<iframe src="https://colab.research.google.com/drive/YOUR_NOTEBOOK_ID" 
        width="100%" height="800px" frameborder="0">
</iframe>
```

## Adding More Projects

To add another project:

1. **Copy the template:**
   ```bash
   cp projects/strava-analysis.html projects/new-project.html
   ```

2. **Update the content** in `new-project.html`

3. **Add a project card** in `index.html`:
   ```html
   <div class="project-card">
       <div class="project-image">
           <img src="IMAGE_URL" alt="Project Name">
           <div class="project-overlay">
               <a href="projects/new-project.html" class="project-link">View Project</a>
           </div>
       </div>
       <div class="project-content">
           <h3 class="project-title">Your Project Title</h3>
           <p class="project-description">Brief description...</p>
           <div class="project-tags">
               <span class="tag">Python</span>
               <span class="tag">Tool</span>
           </div>
       </div>
   </div>
   ```

## Tips for Great Project Pages

1. **Start with context**: What question were you trying to answer?
2. **Show your process**: Include key code snippets, not everything
3. **Visualize results**: Charts are more engaging than tables
4. **Explain insights**: What did you learn? What's interesting?
5. **Add links**: Link to GitHub repo, data sources, etc.
6. **Keep it concise**: Aim for 5-10 minute read time

## Example Workflow

Here's a complete workflow for adding your Strava project:

1. **Finish your analysis** in a Jupyter notebook
2. **Export key visualizations**:
   ```python
   plt.savefig('projects/images/chart1.png', dpi=150, bbox_inches='tight')
   ```
3. **Edit** `projects/strava-analysis.html` with your content
4. **Replace placeholders** with actual images
5. **Test locally**: Open the HTML file in your browser
6. **Commit and push**:
   ```bash
   git add projects/
   git commit -m "Add Strava analysis project"
   git push
   ```

## Need Help?

- Check out the example template at `projects/strava-analysis.html`
- Look at other data science portfolios for inspiration
- Keep the markdown-like structure for readability

---

**Quick Start:**
The fastest way is to just export your Jupyter notebook to HTML and drop it in the `projects/` folder!

