---
name: pptx
description: "Presentation creation, editing, and analysis. When Claude needs to work with presentations (.pptx files) for: (1) Creating new presentations, (2) Modifying or editing content, (3) Working with layouts, (4) Adding comments or speaker notes, or any other presentation tasks"
license: Proprietary. LICENSE.txt has complete terms
---

# PPTX creation, editing, and analysis

## Overview

A user may ask you to create, edit, or analyze .pptx presentations. A .pptx file is a ZIP archive containing XML (OOXML format). Three main workflows exist:

1. **Creating from scratch** - HTML-to-PowerPoint via html2pptx.js
2. **Editing existing** - Unpack XML, modify, validate, repack
3. **Using templates** - Extract inventory, rearrange slides, replace text

## Workflow Decision Tree

### Creating New Presentations
Use the **HTML-to-PowerPoint** workflow with html2pptx.js

### Editing Existing Presentations
Use the **Unpack-Modify-Repack** workflow

### Template-Based Creation
Use the **Template workflow** with inventory.py and replace.py

## Creating New Presentations

### Design Requirements (BEFORE coding)
1. Analyze content and establish design approach
2. Select from web-safe fonts only: Arial, Helvetica, Times New Roman, Georgia, Courier New, Verdana, Tahoma, Trebuchet MS, Impact
3. Choose color palette matching subject matter (not generic/default)
4. Ensure strong contrast and consistent visual hierarchy

### Workflow
1. Create HTML slides with proper PowerPoint dimensions (typically 1280×720px or 1920×1080px)
2. Use `class="placeholder"` for charts/tables that need special handling
3. Rasterize gradients as PNGs first (gradients don't convert well)
4. Convert to PowerPoint:
   ```bash
   node html2pptx.js input.html output.pptx
   ```
5. Validate with thumbnail grid:
   ```bash
   python thumbnail.py output.pptx
   ```

## Editing Existing Presentations

### Workflow
1. **Unpack** the presentation:
   ```bash
   python unpack.py input.pptx unpacked/
   ```

2. **Edit** XML files in `unpacked/ppt/slides/slide{N}.xml`

3. **Validate** immediately after each change:
   ```bash
   python validate.py unpacked/
   ```

4. **Repack**:
   ```bash
   python pack.py unpacked/ output.pptx
   ```

5. **Verify** with thumbnails:
   ```bash
   python thumbnail.py output.pptx
   ```

## OOXML File Structure

```
ppt/
  presentation.xml          # Metadata, slide order
  slides/
    slide1.xml              # Slide 1 content
    slide2.xml              # Slide 2 content
    ...
  notesSlides/
    notesSlide1.xml         # Speaker notes for slide 1
  theme/
    theme1.xml              # Colors and fonts
  media/                    # Images and media files
  slideLayouts/             # Slide layout templates
  slideMasters/             # Master slide definitions
```

## Template-Based Workflow

1. **Extract inventory**:
   ```bash
   python inventory.py template.pptx > inventory.md
   ```

2. **Analyze** slide layouts and map content to template

3. **Rearrange slides** (duplicate/reorder):
   ```bash
   python rearrange.py template.pptx config.json output.pptx
   ```

4. **Generate replacement text** as JSON mapping slide/shape to new text

5. **Apply replacements**:
   ```bash
   python replace.py output.pptx replacements.json final.pptx
   ```

## Design Principles

- **Visual hierarchy**: Use size, weight, and color contrast clearly
- **Minimal text**: Slides communicate visually, not paragraphs
- **Consistency**: Match fonts, colors, spacing across slides
- **Two-column layouts**: Preferred for charts/tables over vertical stacking
- **No clutter**: White space is intentional

## Scripts Reference

| Script | Purpose |
|--------|---------|
| `unpack.py` | Extract PPTX to directory |
| `pack.py` | Repackage directory to PPTX |
| `validate.py` | Check XML validity |
| `html2pptx.js` | Convert HTML to PowerPoint |
| `rearrange.py` | Duplicate/reorder slides |
| `inventory.py` | Extract text shapes inventory |
| `replace.py` | Update text content |
| `thumbnail.py` | Generate visual grid for review |

## Dependencies

- **markitdown**: Content extraction
- **pptxgenjs**: PowerPoint generation
- **playwright**: Screenshot/thumbnails
- **LibreOffice**: `sudo apt-get install libreoffice`
- **Poppler**: `sudo apt-get install poppler-utils`
- **defusedxml**: `pip install defusedxml`
