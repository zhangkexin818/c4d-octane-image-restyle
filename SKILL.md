---
name: c4d-octane-image-restyle
description: Transform one or multiple supplied images into a bright, premium Cinema 4D and Octane animated-film render while preserving each original subject, composition, and color layout. Use for C4D/Octane candy-ceramic 3D restyles and batch image restyling; not for creating editable 3D scene files.
metadata:
  short-description: Batch-restyle images as premium C4D + Octane renders
---

# C4D + Octane Image Restyle

Turn supplied images into polished C4D/Octane stills. The deliverable is a rendered image, not a Cinema 4D project, mesh, or texture package.

## Input handling

- Treat every supplied image as an independent source image unless the user explicitly asks for a composite.
- Preserve each image's subject identity, silhouette, count, pose, composition, camera angle, crop, overlap order, props, and original color zoning. Do not borrow elements between batch items.
- Preserve the input aspect ratio unless the user specifies another ratio. When a new ratio is requested, extend only the background; never stretch or redesign the subject.
- Keep all intended readable text, logos, and graphic marks exactly when the image tool can preserve them. If exact typography is essential, say that it needs compositing rather than regenerating it.

## Standard visual recipe

Use this core prompt for every item, replacing only bracketed fields when the user gives a preference:

```text
Restyle the supplied image as a premium Cinema 4D + Octane Render animated-feature-film still. Preserve the original [subject identity, silhouette, pose, composition, camera angle, crop, prop placement, overlap order, and color zoning] exactly; do not redesign, simplify, add, remove, or swap any core element.

Translate the image into refined stylized 3D with rounded, deliberate hard-surface and soft-sculpture forms, clean large shape language, precise bevels, controlled secondary facets, and physically coherent depth. Materials are a sophisticated mix of creamy ceramic, satin-finish designer resin, soft-touch rubber, translucent colored glass, and restrained candy-glaze accents. Keep most surfaces velvety semi-matte; reserve glossy highlights for eyes, wet details, liquid, glass, enamel, jewelry, or intentional polished accents. No cheap toy PVC, no dirty texture, no generic plastic sheen.

Preserve the source palette faithfully: bright, luminous, high-chroma but refined colors, rendered as material color rather than a filter. Use a clear sky-blue environment, warm sunlight from upper back/side, broad soft fill, pale cyan and warm peach shadow separation, subtle subsurface scattering where appropriate, delicate contact shadows, restrained bloom, soft atmospheric depth, and clean high-key exposure with no clipped highlights. [Keep the original background / extend only the background naturally / use a warm off-white studio cyclorama].

Cinema 4D art direction, Octane Render material realism, high-end stylized animated film, polished editorial visual design, [preserve original lens and framing / extreme close-up wide-angle low angle with controlled Dutch tilt], layered foreground-midground-background depth, soft cinematic depth of field, pristine 3D rendering, luminous midtones, detailed but calm surfaces.
```

Use the original lens and framing by default. Add the dynamic close-up clause only when the source already has, or the user explicitly wants, that energetic cinematic perspective.

## Negative constraints

Append this constraint block unless the user explicitly requests an exception:

```text
no composition change, no identity change, no altered pose, no changed crop, no extra characters, no missing props, no random decorations, no text changes, no logo changes, no photorealistic human skin, no flat 2D lineart, no low-poly, no cheap plastic toy, no PVC, no dirty texture, no gray desaturation, no dark moody lighting, no harsh HDR, no neon, no heavy bloom, no digital noise, no watermark
```

## Material routing

Choose material behavior from the source rather than applying every material at once:

- Characters and soft objects: creamy ceramic, soft-touch resin, satin rubber, subtle subsurface scattering.
- Jewelry, tools, machines, and armor: polished or brushed metal with clean bevels and controlled reflections.
- Transparent colored elements: optical glass or translucent resin with real thickness, refraction, and restrained caustics.
- Fabric-like areas: soft matte sculpted material with visible weave only when it is present in the source.
- Food, liquid, and candy: glossy glaze or translucent jelly, used sparingly as accent material.

Keep palette fidelity ahead of stylistic material variation.

## Batch workflow

For a batch, process images one by one. Use the exact same standard visual recipe and negative constraints for every image, varying only source-specific subject and background instructions. Do not combine unrelated inputs into one generated image or use one source image as a visual reference for another.

Before each result, confirm internally that its aspect ratio, subject count, key silhouette, palette, and important props match its corresponding input. Return each rendered image separately and label it with its source filename or sequence number. If an item fails to preserve a key feature, retry only that item with a more explicit preservation clause.

## Defaults and boundaries

- Default output: same aspect ratio as the input, bright sky-blue/peach high-key lighting, premium candy-ceramic Octane look.
- If the user asks for a different palette or setting, preserve the source's material hierarchy and composition while adapting only the requested look.
- For a request for actual `.c4d`, mesh, UV, texture maps, or render settings, explain that this skill produces render images and ask whether they want a separate 3D-production specification.
