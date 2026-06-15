---
name: replace-football-shoe-background
description: Replace football/soccer shoe product-photo backgrounds with realistic football field or turf scenes for e-commerce main images. Use when Codex is asked to put soccer cleats, turf shoes, TF/FG/AG boots, or similar footwear onto a supplied pitch/stadium/grass background while preserving the original shoes and making the composite look natural, commercial, and free of obvious Photoshop traces.
---

# Replace Football Shoe Background

## Purpose

Create polished e-commerce product main images by compositing football shoes onto a supplied football field, turf, or stadium background. Preserve the original product faithfully while making the shoes look naturally placed in the scene.

## Input Roles

Identify the inputs before editing:

- **Product image**: the shoe photo whose footwear must be preserved.
- **Background image**: the football field/turf/stadium scene to replace the product background.
- **Output target**: Unless specified by the user, the original file name and jpg format will be output, with an image ratio of 1:1, and the workspace path will be used.

If the images are local paths and the built-in image editor needs visual context, inspect them with `view_image` first. If the user attached images in the conversation, use those attachments directly.

## Workflow

1. Use the `imagegen` skill's built-in edit mode by default.
2. Treat the shoe image as the edit target and the field image as the background/reference image.
3. Prompt the editor to preserve the exact shoes: angle, scale relationship, proportions, colors, logos, material texture, outsole tread, stitching, laces, and any visible wear or speckles.
4. Remove the studio/white/background area completely. Avoid white fringing, halos, hard cut edges, and distorted shoe geometry.
5. Place the shoes on the turf with realistic perspective and scale. Keep the product centered and dominant for marketplace use.
6. Add natural grounding:
   - soft contact shadows under the sole/tread;
   - subtle ambient shadow where shoes touch grass;
   - a few foreground grass blades overlapping the bottom outsole only when it improves realism and does not hide sellable details.
7. Match lighting, color temperature, contrast, and sharpness. Keep the shoes crisp and the background softly blurred if the source background is blurred.
8. Save non-destructively in the current workspace unless the user asked to overwrite a source file.
9. The output image name is the same as the original image name, and the image format is JPG.
10. Output the original file name and in JPG format, with an image ratio of 1:1

## Prompt Pattern

Use a concise production prompt like:

```text
Edit the provided football shoe product photo using the provided football field/turf image as the new background.

Preserve the exact shoes from the product photo: same pair, angle, proportions, colors, logos, material details, outsole texture, stitching, and laces. Remove the original background completely and place the shoes naturally on the turf.

Make it look like a real e-commerce main-image product photograph, not a cutout. Add realistic contact shadows, subtle grounding, and a few natural foreground grass blades at the outsole edge only where appropriate. Match lighting, color temperature, perspective, and sharpness. Keep the shoes crisp, centered, clean, and sellable.

No text, watermark, people, extra objects, fake reflections, harsh shadows, halos, white fringe, distorted shoe shape, or obvious Photoshop traces.
```

## Quality Bar

Accept the result only when:

- the product is recognizable as the original shoe photo;
- the shoes appear to rest on the grass, not float above it;
- edges around white uppers, gray soles, and outsole lugs are clean;
- grass overlap is subtle and does not cover important product details;
- the final crop works as a square or marketplace main image;
- any inherited background defects that draw attention are removed.

## Output Naming

Use a descriptive non-destructive filename, for example:

- `<original-name>_足球场主图.png`
- `<original-name>_草坪背景主图.png`
- `<original-name>_field-main.png`

Report the final saved path and show a preview when the app supports local image rendering.
