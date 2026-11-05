# MicroPayments creator catalog, setup and audio demo

This explicit WordPress Playground recipe combines a fictional creator catalog
with videos, photographs, documents and audio downloads. Try Styled tiles,
Cards, List, Creator feed and Justified; optional Fomantic layout buttons;
stars/likes; buyer and creator workspaces; and a reversible single-/multi-creator
presentation. The recipe pins its plugin/theme archives and public media to
specific releases and immutable asset commits.

The six generated cover images, two five-second still-motion videos and two
synthetic audio examples are neutral demonstration content. Audio uses locally
generated sine tones, not human voices, music or field recordings. The cover
art and demo media are CC0-1.0; the Blueprint/provisioning code is
GPL-2.0-or-later. See `asset-provenance.json`, `media/provenance.json` and
`media/audio-provenance.json` for sources and byte hashes.

## Audio samples

The full MP3 example reports 13 seconds after conservative duration rounding;
its independently approved public sample reports 3 seconds. Approval uses the
actual MicroPayments audio metadata reader and sample publication API, rather
than constructing approval metadata by hand. Samples play only after a press
of the native audio controls, request `preload="none"`, and pause when another
sample starts or the page becomes hidden. Browser codec support still applies.

The original Discover page, six original items, creator draft, three creators,
creator subscriptions and original illustrative purchase history remain.
There is one additional clearly fictional audio receipt. No payment is
collected. Prices, memberships, ratings, subscriptions and receipts are
illustrative; a paid page does not make these deliberately public demo
originals private.

## Creator setup

Discover links to an audio page, a separate dynamic creator-home page and a
workflow guide. The original homepage and theme navigation are retained.
The initial multi-creator presentation is applied through the actual setup
proposal/application methods without creating or replacing existing pages.

Use the sandbox administrator's **MicroPayments → Creator setup** screen to
choose a single creator or multiple creators, review changes, then apply.
Undo restores the latest unchanged setup fields and retains unedited generated
pages as drafts. Existing creator permissions, ownership, wallet/payment
configuration, offers, subscriptions and purchases keep their native workflows.

The recorder-to-reviewed-draft integration requires an installed compatible
VideoWhisper recorder and an actually accepted recording. This demo does not
fabricate accepted recorder receipts or imply that its generated tones were
captured by a person.

Provision only into a fresh disposable Playground sandbox. The scripts require
an explicit local provisioning flag and refuse an ordinary existing customer
site. The disposable default login belongs only to that sandbox. Media is
downloaded only for this explicit demo, never during normal plugin activation.

The release owner publishes and verifies the final immutable Blueprint URL
after the pinned MicroPayments release and its new audio assets are available.
