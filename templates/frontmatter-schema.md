# Frontmatter Schema

This document defines the required and optional frontmatter fields for articles.

## Required Fields

- `title`: String - The article title
- `date`: String (YYYY-MM-DD) - Publication date
- `category`: String - Article category (see options below)
- `author`: String - Author name
- `excerpt`: String - Brief description (1-2 sentences)

## Optional Fields

- `tags`: Array of strings - Relevant tags for categorization
- `featured_image`: String - Path to featured image (relative to repo root)
- `draft`: Boolean - Set to true for draft articles (default: false)
- `updated`: String (YYYY-MM-DD) - Last updated date
- `reading_time`: Number - Estimated reading time in minutes

## Category Options

- `product-updates`: Product announcements, feature releases, updates
- `technical`: Technical deep-dives, architecture, development topics
- `case-studies`: Customer stories, use cases, success stories
- `tutorials`: How-to guides, step-by-step instructions
- `announcements`: Company news, events, general announcements

## Example

```yaml
---
title: "Introducing Our New API Gateway"
date: 2025-01-15
category: "product-updates"
author: "Engineering Team"
tags: ["api", "gateway", "infrastructure"]
excerpt: "Learn about our new API gateway that improves performance and reliability."
featured_image: "/assets/images/api-gateway-hero.jpg"
draft: false
reading_time: 5
---
```