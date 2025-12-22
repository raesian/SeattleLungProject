---
title: EXOIRI Website - Home Base Configuration
layout: page
nav_exclude: true
---
# EXOIRI Website - Home Base Configuration
## 🏠 Stable Working Version - Save Point

This document represents the stable "home base" configuration for the EXOIRI website. All features are working perfectly and this serves as our fallback point.

## ✅ Key Features

### Logo Configuration
- **Size**: 160px (height and width)
- **Position**: Centered, 60px from top of green banner
- **Style**: Circular with transparent background, drop shadow
- **File**: `EXOIRI_Logo-removebg-preview.png`

### Navigation
- **Layout**: Overlaid on green banner (not fixed)
- **Tabs**: Home, Lab Members, Donate, Media, Projects
- **Style**: White text, clean spacing
- **Position**: Top-right of banner

### Banner Title
- **Text**: "Exo-Immuno Research Institute"
- **Style**: Large, bold, white text with underline
- **Position**: Centered horizontally in banner

### Family Tree
- **Type**: CSS-based template (replaced image-based)
- **Size**: Shrunk overall for better fit
- **Font**: Standardized to Arial throughout
- **Sections**: PIs, Research Staff, Graduate Students, Interns
- **Layout**: Responsive grid system

### Homepage
- **Research Cards**: 3+2 layout (3 on top, 2 on bottom)
- **Style**: Black background with white text and green borders
- **Images**: Updated to working PNG versions

### Branding
- **Organization Name**: "Exo-Immuno Research Institute" (replaced "Seattle Lung Project")
- **Site Title**: Updated in `_config.yml`
- **Consistent**: All references updated throughout site

## 🔧 Technical Details

### Jekyll Server
- **URL**: http://127.0.0.1:4000/
- **Status**: Running and stable
- **Auto-regeneration**: Enabled

### Key Files Modified
- `_config.yml`: Site title updated
- `_includes/nav.html`: Logo and navigation
- `css/seattle-lung.css`: Logo styling and positioning
- `index.html`: Homepage layout
- `LabMembers.markdown`: Family tree implementation

### CSS Classes
- `.navbar-brand img`: 160px logo with positioning
- `.navbar-brand`: 60px margin-top for positioning
- `.navbar-custom`: Transparent overlay on banner

## 🚀 Status
**PERFECT** - All features working as intended. This is our stable home base configuration.

## 📝 Notes
- Logo is perfectly centered and sized
- Navigation is clean and functional
- Banner title displays correctly
- Family tree is responsive and complete
- All branding is consistent
- Jekyll server is stable

**Date Saved**: October 15, 2025
**Status**: ✅ STABLE - Ready for future modifications

