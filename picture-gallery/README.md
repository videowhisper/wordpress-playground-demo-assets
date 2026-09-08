# Picture Gallery Playground demo assets

This folder is the source package for a separate, public GitHub repository that supplies assets to the WordPress Playground preview. It is intentionally outside Picture Gallery: do not add these files to the plugin ZIP or the WordPress.org SVN assets directory.

The current set contains six original, unbranded images and six pre-rendered 240×180 JPEG thumbnails. Picture Gallery renders filesystem paths from picture-source-file and picture-thumbnail, so the seeded preview avoids image resizing, FFmpeg, a media server, or an external WordPress service.

## Publish this package

1. Create a public repository under the VideoWhisper GitHub organisation, for example wordpress-playground-demo-assets.
2. Preserve the picture-gallery directory structure, including CREDITS.txt and PROMPTS.md, and commit the files.
3. Copy the resulting immutable raw GitHub base URL, for example https://raw.githubusercontent.com/videowhisper/wordpress-playground-demo-assets/<commit-sha>.
4. Replace every __ASSET_BASE_URL__ value in blueprint.seed.template.json with that base URL and copy the completed JSON to picture-gallery/assets/blueprints/blueprint.json.
5. Boot-test the preview before committing its SVN asset update. The seed variant lands on a real, populated gallery page; the currently published baseline blueprint instead lands on the verified admin configuration page.

## Asset contract

| Location | Purpose | Format |
| --- | --- | --- |
| images/originals/*.jpg | picture-source-file values | 1536×1024 JPEG, sRGB |
| images/thumbnails/*.jpg | picture-thumbnail values | 240×180 JPEG, centre-cropped |

The matching filename in both directories is intentional. The template writes the static files directly into Playground's wp-content/uploads tree, then inserts the Picture Gallery posts and their exact metadata. It does not call WordPress image processing or the plugin's thumbnail-generation function.

## Visual and policy checklist

- Source images are original ChatGPT output generated on 2026-08-20 and are documented in CREDITS.txt.
- Visual review completed: diverse home, studio, garden and landscape scenes; no people, visible text, watermarks, logos, product marks or sensitive material.
- Keep every future addition general-audience, unbranded and free of text, watermarks, trademarks, identifiable people and sensitive content.
- Do not bundle this content in the plugin or fetch it on plugin activation. It is for the disposable Playground sandbox only.

