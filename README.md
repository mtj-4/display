# Card Collection Gallery System

A beautiful, responsive gallery to showcase your trading card collection online with a light blue background and Arial font.

## Features

- 🎨 **Clean Design**: Light blue background with no gradients
- 📱 **Responsive Layout**: 5-column grid that adapts to different screen sizes
- 🖼️ **High-Quality Images**: Extracts front card images from your URLs
- ⚡ **Smooth Scrolling**: Optimized for smooth browsing experience
- 🔗 **Direct Links**: Click to view original card listings
- 🔤 **Arial Font**: Clean, readable typography

## Quick Start

### 1. Prepare Your Data

Create a CSV file named `data.csv` with your card data:

```csv
Title,URL
"2020 Bowman Chrome Sapphire Green Anthony Volpe PROSPECT AUTO /50 #BSPAAW PSA 10",https://alt.xyz/example1
"2024 Panini Prizm Lazer Prizm Caleb Williams #301 PSA 10",https://fanaticscollect.com/example2
"2023 Panini Mosaic Stained Glass CJ Stroud ROOKIE #SG-22 PSA 10 GEM MINT",https://alt.xyz/example3
```

### 2. Generate the Gallery

```bash
# Generate gallery from your CSV
py generate_gallery.py

# Or specify a different CSV file
py generate_gallery.py my_cards.csv
```

This creates `gallery.html` with your actual card data and images.

### 3. Preview Locally

Open `gallery.html` in your web browser to see your collection.

### 4. Publish to GitHub Pages

1. **Create a GitHub repository** (e.g., `my-card-collection`)
2. **Upload the files**:
   - `gallery.html` (rename to `index.html`)
   - `README.md` (optional)
3. **Enable GitHub Pages**:
   - Go to repository Settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"
4. **Your gallery will be live at**: `https://yourusername.github.io/my-card-collection`

## Customization

### Colors
The gallery uses a light blue theme:
- **Background**: `#87CEEB` (Sky Blue)
- **Buttons**: `#4682B4` (Steel Blue)
- **Text**: `#2c3e50` (Dark Blue-Gray)

### Layout
- **Desktop**: 5 columns
- **Tablet**: 4 columns  
- **Mobile**: 2-3 columns
- **Small mobile**: 1 column

### Images
The script automatically extracts front images from:
- `fanaticscollect.com` URLs
- `alt.xyz` URLs
- Falls back to placeholder images if extraction fails

## File Structure

```
gallery_system/
├── index.html              # Sample gallery template
├── generate_gallery.py     # Script to create gallery from CSV
├── data.csv               # Your card data (Title, URL columns)
├── gallery.html           # Generated gallery (after running script)
└── README.md              # This file
```

## Usage Examples

### Basic Usage
```bash
# Use default data.csv
py generate_gallery.py
```

### Custom CSV File
```bash
# Use your own CSV file
py generate_gallery.py my_collection.csv
```

### CSV Format
Your CSV file should have these columns:
- `Title`: The card title/name
- `URL`: The link to the card listing

Example:
```csv
Title,URL
"PSA 10 2020 Bowman Chrome #BSPAAW ANTHONY VOLPE Sapphire /50",https://alt.xyz/card1
"PSA 10 2024 Panini Prizm #301 CALEB WILLIAMS Prizm",https://fanaticscollect.com/card2
```

## Troubleshooting

### Images Not Loading
- Check if the original URLs are accessible
- Some sites may block automated requests
- The script will show placeholder images for failed extractions

### Layout Issues
- Ensure you're using a modern browser
- Check the responsive breakpoints in the CSS
- Test on different screen sizes

### CSV Issues
- Make sure your CSV has `Title` and `URL` columns
- Use quotes around titles with commas
- Check file encoding (UTF-8 recommended)

## Advanced Features

### Custom Domain
1. Add a `CNAME` file to your repository with your domain name
2. Configure DNS settings with your domain provider
3. Your gallery will be available at your custom domain

### Analytics
Add Google Analytics or other tracking by inserting the code in the `<head>` section of the generated HTML.

## Support

If you encounter issues:
1. Check that your CSV file exists and has the correct format
2. Verify your URLs are accessible
3. Test the gallery locally before publishing
4. Check browser console for any JavaScript errors

---

**Enjoy showcasing your card collection! 🏆**
