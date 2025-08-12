# head(amame) Documentation

Comprehensive documentation website for head(amame) open-source DIY headphones, built with MkDocs Material.

## 🎧 About head(amame)

head(amame) is an open-source DIY headphone platform that brings high-end audio engineering to makers worldwide. Our mission is to democratize exceptional audio quality through completely open designs, comprehensive documentation, and an active community.

### Product Lines

- **head(amame)**: Premium platform with planar magnetic drivers ($180-285 build cost)
- **min(amame)**: Accessible entry point with dynamic drivers ($80-150 build cost)

## 📚 Documentation Features

This documentation site includes:

- **Comprehensive build guides** with step-by-step instructions
- **Interactive component tables** with real-time pricing
- **3D printing optimization guides** for various printers and materials
- **Community showcase** and contribution guidelines
- **Technical specifications** and measurement data
- **Troubleshooting resources** and FAQ
- **Blog** with development updates and community highlights

## 🚀 Local Development

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/headamame/docs.git
   cd docs
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Start development server**
   ```bash
   mkdocs serve
   ```

4. **Open in browser**
   ```
   http://localhost:8000
   ```

The development server includes live reload - changes to content will automatically refresh the browser.

### Project Structure

```
docs/
├── mkdocs.yml              # MkDocs configuration
├── requirements.txt        # Python dependencies
├── docs/                   # Documentation content
│   ├── index.md           # Homepage
│   ├── assets/            # Images, stylesheets, etc.
│   │   ├── images/        # Product photos, diagrams
│   │   └── stylesheets/   # Custom CSS
│   ├── head-amame/        # Premium platform docs
│   │   ├── getting-started/
│   │   ├── build-guide/
│   │   ├── technical/
│   │   ├── customization/
│   │   └── downloads/
│   ├── min-amame/         # Entry-level platform docs
│   │   ├── getting-started/
│   │   ├── build-guide/
│   │   ├── technical/
│   │   └── downloads/
│   ├── community/         # Community resources
│   ├── support/           # Help and troubleshooting
│   └── blog/              # Development blog
├── overrides/             # Theme customizations
└── .github/
    └── workflows/         # CI/CD for GitHub Pages
```

## 🎨 Theme and Styling

### Material Design Features

- **Modern interface** with light/dark mode toggle
- **Advanced search** with suggestions and highlighting
- **Mobile-responsive** design optimized for all devices
- **Navigation features** including tabs, sections, and instant loading
- **Content features** including code highlighting, admonitions, and tabs

### Custom Styling

The site includes custom CSS for maker/DIY aesthetic:

- **Component cards** with hover effects for build information
- **BOM tables** with sortable columns and supplier links
- **Print settings grids** for 3D printing parameters
- **Build progress indicators** for step-by-step guides
- **Cost calculators** for project budgeting
- **Gallery layouts** for community builds

### Color Scheme

- **Primary**: Deep purple (`#4c1d95`) - Technical sophistication
- **Accent**: Amber (`#f59e0b`) - Maker energy and creativity
- **Supporting colors**: Blue, green, orange for different component types

## 🔧 Customization

### Adding Content

1. **Create new page**: Add `.md` file in appropriate directory
2. **Update navigation**: Edit `nav` section in `mkdocs.yml`
3. **Add images**: Place in `docs/assets/images/` with descriptive names
4. **Use components**: Leverage custom CSS classes for consistent styling

### Custom Components

The site includes several custom components:

```markdown
<!-- Component card -->
<div class="component-card">
### Component Title
Component description and details
</div>

<!-- Build step -->
<div class="build-step">
<div class="step-number">1</div>
<div>
**Step Title**
Step description and instructions
</div>
</div>

<!-- Specification table -->
<div class="spec-table">
<div class="spec-label">Parameter</div>
<div class="spec-value">Value</div>
</div>
```

### Configuration Options

Key configuration options in `mkdocs.yml`:

- **Site information**: Update `site_name`, `site_url`, `site_description`
- **Theme settings**: Modify colors, fonts, and features
- **Plugin configuration**: Enable/disable features like search, git dates, social cards
- **Navigation structure**: Customize the site hierarchy
- **Extra settings**: Analytics, social links, version information

## 🚀 Deployment

### GitHub Pages (Recommended)

The site automatically deploys to GitHub Pages using GitHub Actions:

1. **Push to main branch** triggers the deployment workflow
2. **Build process** installs dependencies and generates static site
3. **Deployment** publishes to GitHub Pages with custom domain support

### Manual Deployment

For other hosting platforms:

```bash
# Build static site
mkdocs build

# Deploy to hosting platform
# (upload contents of site/ directory)
```

### Environment Variables

Set these for full functionality:

- `GOOGLE_ANALYTICS_KEY`: Google Analytics tracking ID
- `GITHUB_TOKEN`: For git revision dates (automatically provided in GitHub Actions)

## 🤝 Contributing

We welcome contributions to improve the documentation!

### Content Contributions

- **Fix errors**: Correct typos, outdated information, broken links
- **Add content**: Write new guides, expand existing sections
- **Improve clarity**: Rewrite confusing sections, add examples
- **Update information**: Keep component lists, prices, and suppliers current

### Technical Contributions

- **Theme improvements**: Enhance styling, add new components
- **Feature additions**: Implement new MkDocs plugins or functionality
- **Performance optimization**: Improve build times, page load speeds
- **Accessibility**: Ensure the site is usable by everyone

### Contribution Process

1. **Fork the repository** and create a feature branch
2. **Make your changes** following the style guide
3. **Test locally** to ensure everything works
4. **Submit a pull request** with a clear description of changes

### Style Guide

- **Markdown formatting**: Use consistent heading levels, bullet points, code blocks
- **Image optimization**: Compress images, use descriptive alt text
- **Link conventions**: Use relative links for internal content
- **Code examples**: Include complete, working examples with explanations

## 📄 License

- **Documentation**: [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Code and configurations**: [MIT License](https://opensource.org/licenses/MIT)
- **head(amame) designs**: [MIT License](https://opensource.org/licenses/MIT)

## 🔗 Links

- **Live Documentation**: [docs.headamame.com](https://docs.headamame.com)
- **Main Project**: [github.com/headamame](https://github.com/headamame)
- **Community Discord**: [discord.gg/headamame](https://discord.gg/headamame)
- **Reddit Community**: [reddit.com/r/headamame](https://reddit.com/r/headamame)
- **YouTube Channel**: [youtube.com/@headamame](https://youtube.com/@headamame)

## 🆘 Support

- **Documentation Issues**: Open an issue in this repository
- **Build Help**: Ask in [Discord #build-help](https://discord.gg/headamame)
- **General Questions**: Check the [FAQ](https://docs.headamame.com/support/faq/) first

---

Built with ❤️ by the head(amame) community using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).