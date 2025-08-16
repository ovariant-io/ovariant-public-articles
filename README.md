# Ovariant Public Articles

Ovariant's public article repository that allows easy sharing and access to articles and publications.

## Repository Structure

```
/
├── README.md                    # This file
├── articles/                    # All article content organized by category
│   ├── product-updates/        # Product announcements and feature releases
│   ├── technical/              # Technical deep-dives and development content  
│   ├── case-studies/           # Customer stories and use cases
│   ├── tutorials/              # How-to guides and step-by-step instructions
│   └── announcements/          # Company news and general announcements
├── assets/                     # Media files and static assets
│   ├── images/                 # Images referenced in articles
│   └── videos/                 # Video files referenced in articles
├── templates/                  # Templates for consistent article creation
│   ├── article-template.md     # Standard article template
│   └── frontmatter-schema.md   # Frontmatter field definitions
├── .github/                    # GitHub-specific configuration
│   └── workflows/              # Automated validation and deployment
│       └── validate.yml        # Article validation workflow
└── config/                     # Site configuration files
    ├── site-config.yml         # Main site configuration
    └── metadata.json           # Repository metadata and conventions
```

## Creating Articles

### 1. Choose the Right Category

- **product-updates**: Product announcements, feature releases, updates
- **technical**: Technical deep-dives, architecture, development topics  
- **case-studies**: Customer stories, use cases, success stories
- **tutorials**: How-to guides, step-by-step instructions
- **announcements**: Company news, events, general announcements

### 2. Use the Article Template

Copy `/templates/article-template.md` to your chosen category folder and rename it following the naming convention:

```
YYYY-MM-DD-article-title.md
```

### 3. Required Frontmatter

Every article must include these frontmatter fields:

```yaml
---
title: "Your Article Title"
date: YYYY-MM-DD
category: "category-name"
author: "Author Name"  
excerpt: "Brief 1-2 sentence description"
---
```

### 4. Optional Frontmatter

Additional fields you can include:

- `tags`: Array of relevant tags
- `featured_image`: Path to featured image
- `draft`: Set to true for draft articles
- `updated`: Last updated date
- `reading_time`: Estimated reading time in minutes

## Adding Assets

### Images
- Place images in `/assets/images/`
- Use descriptive filenames
- Reference in articles as `/assets/images/filename.jpg`

### Videos  
- Place videos in `/assets/videos/`
- Use descriptive filenames
- Reference in articles as `/assets/videos/filename.mp4`

## Validation

The repository includes automated validation via GitHub Actions that checks:

- ✅ Frontmatter exists and is properly formatted
- ✅ Referenced images and assets exist
- ✅ Markdown syntax is valid
- ✅ Links are not broken

## Contributing

1. Create a new branch for your article
2. Use the appropriate template from `/templates/`
3. Follow the naming conventions
4. Add any required assets to `/assets/`
5. Test locally if possible
6. Submit a pull request

The validation workflow will automatically check your article before it can be merged.

## Configuration

Site-wide settings can be modified in:
- `/config/site-config.yml` - Main site configuration
- `/config/metadata.json` - Repository metadata and conventions

For questions or issues, please open a GitHub issue or contact the content team.