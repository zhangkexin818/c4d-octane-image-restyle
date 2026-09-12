# C4D + Octane Image Restyle

A Codex skill for restyling one image or a batch of images as bright, premium Cinema 4D + Octane animated-film renders.

It preserves the source subject, composition, palette, props, and aspect ratio by default, while applying a refined candy-ceramic material system, high-key cinematic lighting, and polished stylized 3D direction.

## Use it for

- Single-image C4D / Octane image restyling
- Batch conversion with a consistent visual language
- Stylized character, product, prop, and illustration renders

## What it preserves

- Subject identity, silhouette, count, pose, and key props
- Composition, crop, camera angle, overlap order, and color zoning
- Input aspect ratio, unless a new ratio is explicitly requested

## What it does not produce

Rendered images only. It does not produce editable `.c4d` files, meshes, UVs, texture maps, or a complete 3D scene.

## Install

Copy the `SKILL.md` file into your Codex skills directory, then invoke `c4d-octane-image-restyle` with one or more images.

Example request:

```text
Use c4d-octane-image-restyle to convert these images into bright, premium C4D + Octane renders. Keep their original compositions and output each image separately.
```
