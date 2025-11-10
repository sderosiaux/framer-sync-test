# Framer GitHub Sync Test Repository

This repository contains sample markdown files to test the [Framer GitHub Sync plugin](https://www.framer.com/marketplace/plugins/github-sync/).

## Repository Structure

```
├── blog/                    # Blog posts collection
│   ├── getting-started.md
│   ├── advanced-animations.md
│   └── cms-best-practices.md
├── docs/                    # Documentation collection
│   ├── introduction.md
│   ├── guides/
│   │   ├── installation.md
│   │   └── configuration.md
│   └── api/
│       └── overview.md
├── portfolio/              # Portfolio projects collection
│   ├── project-alpha.md
│   └── project-beta.md
└── team/                   # Team members collection
    ├── john-doe.md
    └── jane-smith.md
```

## Framer CMS Collections

You can create separate CMS collections in Framer for each folder:

### 1. Blog Collection
- **Base Path**: `/blog`
- **Content Type**: Blog posts and articles
- **Fields**: title, description, author, date, category, tags, featured, readTime

### 2. Documentation Collection
- **Base Path**: `/docs`
- **Content Type**: Technical documentation
- **Fields**: title, description, section, order, lastUpdated, version

### 3. Portfolio Collection
- **Base Path**: `/portfolio`
- **Content Type**: Project case studies
- **Fields**: title, description, client, date, category, tags, status, featured

### 4. Team Collection
- **Base Path**: `/team`
- **Content Type**: Team member profiles
- **Fields**: name, role, bio, email, avatar, skills, joinDate, active

## Using with Framer

1. **Install the GitHub Sync Plugin** in your Framer project
2. **Connect your GitHub account** and authorize the plugin
3. **Select this repository** (or your fork of it)
4. **Configure base paths** for each collection you want to sync
5. **Import the content** and map the frontmatter fields to CMS fields

## Frontmatter Structure

All markdown files include YAML frontmatter with metadata:

```yaml
---
title: Your Title
description: Your description
author: Author Name
date: 2025-01-15
category: Category Name
tags: [tag1, tag2, tag3]
featured: true
---
```

## Image Handling

The plugin supports relative image paths. For example:

```markdown
![Hero Image](./images/hero.jpg)
```

The plugin will automatically convert these to absolute URLs when syncing to Framer.

## Testing Notes

- **Public Repository**: Works without authentication
- **Private Repository**: Requires a personal access token
- **Nested Folders**: Supported - slugs reflect the file path
- **MDX Files**: Supported, but custom components are discarded

## Next Steps

After importing, you can:

- Create dynamic pages in Framer that pull from these collections
- Add filters and sorting to display content
- Build a blog, documentation site, or portfolio
- Update content by editing markdown files and syncing changes

## Support

For issues with the GitHub Sync plugin, refer to:
- [Framer Plugin Documentation](https://www.framer.com/marketplace/plugins/github-sync/)
- [Framer Community Forums](https://www.framer.community/)
