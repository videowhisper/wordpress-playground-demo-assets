# VideoWhisper WordPress Playground demo assets

This public repository holds small, static, versioned demo asset packages for
VideoWhisper WordPress.org plugin previews. It is not a WordPress plugin and
none of its files are included in a plugin ZIP.

## Packages

- `picture-gallery/` — original and thumbnail JPEG fixtures plus the seed
  blueprint template for Picture Gallery.
- `broadcast-live-video/` — offline channel snapshots and thumbnails plus the
  seed blueprint template for Broadcast Live Video.

## Consuming an asset package

Use a `raw.githubusercontent.com` URL pinned to a commit SHA in a WordPress
Playground blueprint. Do not reference a moving branch such as `main` or
`trunk`. A blueprint may download these files only while its `networking`
feature is explicitly enabled.

When assets change, publish a new commit, run the Playground preview against
that commit SHA, then update the consuming plugin's SVN blueprint in the same
reviewable change. Do not fetch these files on plugin activation or bundle
them into a release archive.

## Asset standards

Packages must contain only original or correctly licensed, general-audience
content. Keep provenance and image-generation prompts with the package. Do
not include personally identifiable people, text, logos, watermarks,
trademarks, sensitive material, executable code, credentials, or tracking.

Unless a package says otherwise, assets are available under GPL-2.0-or-later.
