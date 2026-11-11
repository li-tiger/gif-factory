---
name: pixel-gif-sticker-pack
description: Create or repair character sticker GIFs, electronic lenticular flip cards, character-led dynamic posters, mascot-led brand films, compact low-frame storybooks, or handwritten artistic signature loops. Choose appearance, movement and output purpose separately; assess source suitability and deliver reviewed media with verified downloads.
---

# Tiger GIF 工厂

Carry forward the latest reference, required count, format, language, and visual constraints. For a GLB, render a front or three-quarter reference with the face and identifying details visible. If the user supplied a drawing, preserve the recognizable silhouette, facial features, palette, and signature accessories. Use only imagery the user provided or authorized for the task.

## Browse styles first when the user asks for a look

Use [the style index](styles/README.md) to resolve Chinese/English style names, then read only that `styles/<id>/STYLE.md` and its linked production reference. The six GIF gallery groups are discovery categories, not six new rendering engines. Compact storybooks and brand films are separate narrative extensions. Continue to record appearance, movement and purpose separately, and preserve accepted user choices. Do not invent a new style by only changing a character or promote a pending repair because it appears in the full gallery.

Use **Tiger GIF 工厂** as the display name and `$pixel-gif-sticker-pack` as the invocation identifier. The homepage is a style chooser; [GALLERY.md](GALLERY.md) holds complete series and their status, while [GUIDE.md](GUIDE.md) holds longer usage instructions. Mascot brand films and compact storybooks remain extensions, not GIF loop presets.

## Choose the output purpose

| Request | Route |
| --- | --- |
| 动态艺术签名／名字＋物体＋渐变／两笔书写 | [Dynamic signatures](references/dynamic-signatures.md), then [standalone module](skills/dynamic-art-signature/SKILL.md) |
| 独立聊天表情包 | Sticker workflow below |
| 收藏卡／双身份变画，主要展示两幅图 | [Lenticular cards](references/lenticular.md) |
| 演出预告／角色主视觉／人物与字体联动／P5 式整体融合海报 | [Dynamic posters](references/dynamic-posters.md) |
| 吉祥物带动产品、包装与品牌的短片 | [Brand films](references/brand-film.md) |
| 动态绘本／固定画面叙事／页内单次动作／翻书故事 | [Compact storybooks](references/storybook.md), then [standalone Skill](skills/compact-storybook/SKILL.md) |

For dynamic posters, distinguish **preserve artwork + animated type** from **integrated artwork/background/type redesign**. The approved P5-inspired route is a limited-palette, ink/halftone composition with meaningful character-state contrast and type interacting with the figure; it is not letter stickers pasted onto unchanged full-color artwork. The current nine-poster examples encode two complete poster key states, not independently animated glyphs. Read only the selected purpose reference; a GIF preview of a game UI is not a working interactive UI.

For **electronic lenticular cards / 电子光栅卡 / 人脸面罩切换 / 双状态变画**, read [the lenticular workflow](references/lenticular.md) first: assess whether two images can align, establish the requested composition, then export the flip. This is an output/movement category usable with photographic or illustrated art, not a fourth appearance style. Default for this series is fixed 480×720 opaque posters, six-second loops, fixed titles; do not run the square transparent-sticker presets or a brand-film sequence.

For independently usable chat GIFs, follow the sticker workflow below. For a mascot-led shop, product or independent-brand promo, read [brand films](references/brand-film.md): connect character acting to a visual cause and result, then to the brand. Appearance, movement and purpose are separate choices. A brand film does not automatically require a new sticker pack; a sticker request does not require an advertising story. Reuse accepted choices and prior authorization rather than restarting approvals.

For **compact storybooks**, use the standalone storybook Skill: preserve the requested art style; default to fixed framing, real 6fps, a roughly three-second once-only action and a brief result hold. Keep props continuous between pages and inspect contact anchors. Do not force loops, smooth interpolation, montage shots, or long idle padding. This route has its own output and review rules.

For **dynamic artistic signatures**, integrate the motif into letter anatomy; preserve the accepted two-gesture rhythm, roughly one-second pause, clean blank background, and decelerating final terminal. Default to flat handwritten ink, no metallic material, shake or recoil. Inspect independently separated stroke layers and body-to-tail handoff. Read the signature route instead of applying sticker atlases or whole-sprite bounce.

The remaining sections describe the **chat-sticker workflow**. For a lenticular-card, dynamic-poster, brand-film, storybook or signature brief, follow its selected reference instead; the square canvas, atlas layout, transparent margins and two-second sticker defaults below do not apply.

## Choose appearance and movement separately

Carry forward accepted choices rather than asking again. Choose two independent axes:

| Appearance | Rendering |
| --- | --- |
| [Pixel](references/appearance.md#pixel) | Deliberate pixel clusters and crisp stepped outlines; 320px; separate light/action exporters |
| [Clean illustration](references/appearance.md#illustration) | Anime, chibi, mascot or photo-to-illustration artwork; HD, 512px |
| [Photographic](references/appearance.md#photographic) | Photo-like people or pets; preserve accepted likeness and lighting; HD, 512px |

Subject categories such as anime, pets and public figures do not select a movement method. HD specifies sampling and resolution; it does not promise consistent anatomy or smoother motion. Photo-to-anime is an input transformation, not an extra appearance mode.

- **Light motion:** one distinct expression/pose per sticker, animated with small bounce, nod, sway, squash and optional accents. Use `export_pack.py`. Keep captions fixed. A pack must still contain distinct visible expressions/poses, not one portrait with 25 captions.
- **Consecutive character action:** generated sequential poses with coordinated face, head, shoulders, torso and relevant limbs, plus hair/clothing follow-through. Use the keyframe workflow below. A frozen body with only a rotating arm does not fulfill this mode. Do not substitute light motion to hide a failed action without telling the user.

If the user says “like the approved full-character action,” preserve that method. When matching an existing reference, preserve its appearance unless a style conversion was requested. For photographic actions, pilot one restrained gesture before expanding; do not automatically add beauty filters. Rejection of one selfie animation does not reject all photographic stickers.

Read the selected section of [the appearance guide](references/appearance.md), then read [light motion](references/light-motion.md), [pixel consecutive actions](references/pixel-actions.md), or [HD consecutive actions](references/keyframes.md) for the selected combination. Record appearance, movement, reference, count, captions and acceptance status separately in the production notes. If an essential appearance/movement choice remains ambiguous, ask a short choice question; otherwise reuse the user's latest accepted settings and proceed. An approved sample followed by a request to expand it carries those settings into the batch.

Do not assume all six combinations have the same ready-made exporter or visual reliability. Pixel + consecutive actions uses `export_pixel_actions.py` and the accepted four-character pack as a reference. Pilot new identities/actions before expanding. `export_keyframes.py` uses smooth HD sampling and is reserved for illustration/photographic actions. See [the version-specific sample status](references/appearance.md#sample-status): a new revision remains pending until accepted; an abandoned experiment is not a default template.

## Design and generate

- For a large pack, plan categories first and give each sticker a chat line, a visible pose or prop, and an animated beat. Review neighboring concepts for semantic duplicates. An identical pose with new text alone is insufficient.
- Match the main action to the caption. For example, show one nod for “好的”, one pass across the frame for “一位靓仔偶然路过”, or one face-covering tearful reaction for “猛虎落泪”. Keep one main action per loop and use accents only to support that action.
- When playback feels rushed or the caption needs reading time, start with a 2.8–3 second loop. Hold a readable pose before or after the gesture, with most of the extra time on the hold. Adjust after watching the exported GIF at chat size. Follow any explicit duration request.
- Preserve user-supplied lines. When the user asks for memes, choose phrases that fit both the chat situation and the visible action. Break long captions at a natural phrase boundary, keep the text fixed throughout playback, and check legibility in the exported GIF. Use a compositor that supports multiline captions when needed.
- Use the image generation tool for new pose art. Ask for one transparent sprite atlas at a time, usually a 4 × 4 sheet with wide gutters and no lettering. Give exact reading order, stable framing and identity anchors. Keep lettering in composition, where it can be verified.
- Inspect each atlas at full size. Count actual occupied cells, map each cell to its visible pose, and correct a mismatched caption or regenerate an unusable sprite. Watch for swapped cells, clipped hair or hands, and artifacts across gutters. A 100-sticker pack needs 100 accepted entries.
- For tiny chat previews, prefer strong readable facial expressions and a legible caption. Let each motion settle naturally into the next loop. Keep the original source and generated atlases outside the shareable ZIP unless requested.

## Articulated actions

When the user requests the gesture to unfold over time, use [the pixel action workflow](references/pixel-actions.md) with `scripts/export_pixel_actions.py` for pixel art, or [the HD keyframe workflow](references/keyframes.md) with `scripts/export_keyframes.py` for illustration/photographic art. If the request is explicitly light motion, a static waving/heart pose plus a small preset remains appropriate. Generate consecutive poses of the same character and compose them with shared alignment. Keep photographic and anime rendering styles as requested. Whole-sprite deformation alone does not fulfill a request for articulated motion.

For subtle idle movement or a large pack of distinct static poses, the existing motion-preset exporter remains appropriate. Keyframe GIFs may have visible pose transitions or identity drift; inspect them and describe material limits. Use a video or rigged compositor only when needed for genuinely smooth continuous motion, preserving the user's chosen provider and method.

Read [the visual stability gate](references/stability.md) for every new consecutive-action workflow and when repairing choppy/frame-skipping playback or an inconsistent frame. Review identity/pose anchors before filling transitions. Inspect the actual decoded frames, native-size face details, normal playback, and the loop seam. Frame count, distinct pixels, smooth timing and a valid ZIP are technical checks, not a visual acceptance decision. Repair a rejected frame and its neighbors, re-export, then repeat review. Keep assistant review separate from user acceptance; do not promise automatic elimination of all temporal or visual defects.

## Automatic clear rendering

The bundled exporter now defaults to **hd**: it renders directly from original atlas crops into 512 × 512 frames with LANCZOS resizing and BICUBIC continuous deformation. Use this default for photographic people, realistic pets and detailed illustration. A user invoking this Skill does not need to request a separate clarity fix or edit a compositor.

- Preserve the accepted face, expression, caption and pose while exporting. For a named person with an ambiguous name, resolve the identity from the user's handle or reference before generating it.
- Use `--render-style pixel` (or manifest `"render_style": "pixel"`) only when the user explicitly wants pixel art or the reference is intentionally pixel-based. That mode preserves the original 320 × 320 pixel pipeline. The CLI flag overrides the manifest.
- HD previews default to a clean grid without headings and are assembled from decoded final GIFs; `--preview-layout chapters` opts into category headings. Follow any explicit user choice about preview titles.
- If a face still looks blurry, inspect the original crop and decoded output at the same display size. Read [the clarity guide](references/clarity.md) for source-resolution limits and before/after validation. Enlarging an already pixelated export cannot recover lost details.

## Compose and verify

For a repeatable workflow, use [the atlas exporter](scripts/export_pack.py) with Python 3 and Pillow. It uses FFmpeg for MP4 playback. Run `python3 scripts/export_pack.py --help` and read [the manifest format](references/manifest.md) for cell overrides and motion presets. Choose a local font that covers the requested captions. Use another compositor when the brief requires actual skeletal or frame-by-frame character animation.

For sticker deliverables, give one transparent looping GIF per entry, grouped in a ZIP. Default to clear 512 × 512 GIFs and roughly two seconds per loop; use 320 × 320 only for the intentional pixel path. Respect explicit target-platform size limits with an appropriate compositor or final downsampling, then re-verify the result. A separate MP4 assembled from the decoded GIFs makes playback inspectable even in a chat surface that shows a still. A static contact sheet can help compare designs when clearly identified as a still. For lenticular cards, use the opaque full-bleed format, source-suitability checks, actual-duration audit and GIF deliverables in [lenticular.md](references/lenticular.md); do not require sticker transparency or an MP4. For dynamic posters, follow [the poster design and loop checks](references/dynamic-posters.md); do not apply the card rule that all display titles remain fixed to a brief requesting animated type. For brand-film deliverables, use the format and editable-source checks in the brand-film reference instead of forcing the sticker canvas or loop duration onto the film.

Verify exact count and unique captions, visible movement, frame timing, loop flag, alpha, safe margins, ZIP integrity and MP4 decoding. Inspect each category visually. Report actual deliverables and any limits that affect use. A local playback check does not establish compatibility with a specific messaging platform.

