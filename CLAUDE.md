# Claude Code Repository Understanding

## Repository Purpose
This is Ovariant's public article repository designed to house markdown files that will be scanned and rendered on a website. The repository follows SEO-friendly best practices with organized content structure and automated validation.

## Directory Structure

```
/
├── README.md                    # Repository documentation and usage guidelines
├── CLAUDE.md                    # This file - Claude's understanding of the repo
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

## Content Creation Workflow

### When creating new articles:

1. **Choose the appropriate category**:
   - `product-updates`: Product announcements, feature releases, updates
   - `technical`: Technical deep-dives, architecture, development topics  
   - `case-studies`: Customer stories, use cases, success stories
   - `tutorials`: How-to guides, step-by-step instructions
   - `announcements`: Company news, events, general announcements

2. **Use the naming convention**: `YYYY-MM-DD-article-title.md`

3. **Copy the template**: Use `/templates/article-template.md` as the starting point

4. **Required frontmatter fields**:
   ```yaml
   ---
   title: "Article Title"
   date: YYYY-MM-DD
   category: "category-name"
   author: "Author Name"
   excerpt: "Brief 1-2 sentence description"
   ---
   ```

5. **Optional frontmatter fields**:
   - `tags`: Array of relevant tags
   - `featured_image`: Path to featured image
   - `draft`: Set to true for draft articles
   - `updated`: Last updated date
   - `reading_time`: Estimated reading time in minutes

### When working with assets:

- **Images**: Place in `/assets/images/` with descriptive filenames
- **Videos**: Place in `/assets/videos/` with descriptive filenames
- **Reference format**: `/assets/images/filename.jpg` or `/assets/videos/filename.mp4`

## Important Commands & Workflows

### For migrating content from Confluence:
1. Use the Atlassian MCP server to fetch page content
2. Convert to markdown format with proper frontmatter
3. Place in appropriate category folder with correct naming convention
4. Ensure all referenced assets are moved to `/assets/` folder

### Validation:
The repository includes GitHub Actions workflow (`.github/workflows/validate.yml`) that automatically:
- Checks frontmatter exists and is properly formatted
- Validates referenced images and assets exist
- Checks markdown syntax
- Verifies links are not broken

## SEO Considerations

This structure is SEO-optimized with:
- **Clean URL structure**: Category-based hierarchy creates readable URLs
- **Rich metadata**: Frontmatter fields map to HTML meta tags
- **Content organization**: Category silos help search engines understand themes
- **Asset optimization**: Organized media structure for fast loading
- **Quality assurance**: Automated validation prevents SEO issues

### Potential SEO enhancements to consider:
- Add `canonical_url` field to frontmatter
- Include Open Graph fields (`og_image`, `og_description`)
- Add `schema_type` for structured data
- Include `related_posts` for internal linking

## Configuration Files

- **`/config/site-config.yml`**: Main site settings, categories, social links
- **`/config/metadata.json`**: Repository metadata and naming conventions
- **`/templates/frontmatter-schema.md`**: Complete frontmatter field documentation

## Best Practices

1. **Always use the article template** for consistency
2. **Follow naming conventions** for discoverability
3. **Include proper frontmatter** for SEO and site functionality
4. **Organize assets logically** with descriptive filenames
5. **Test locally** before committing if possible
6. **Use descriptive commit messages** for content changes

## Company Context

- **Organization**: Ovariant
- **Primary product**: Lua (women's health app)
- **Focus areas**: Women's health, AI-powered recommendations, symptom tracking
- **Contact**: developer@ovariant.io for technical support

This repository serves as the content foundation for Ovariant's public-facing articles and publications, designed to be easily maintainable and SEO-optimized for web rendering.