---
name: admode
description: Make ads with Admode. Static image ads, AI UGC, podcast and animated video ad prompts built on long-running Meta ads and checked by Admode before anything is rendered, new versions of a winning ad, ad copy, editing a finished video ad, syncing Meta ads, and the VOC research, Foundation Pack and Brand DNA the ads are built on. Use when the user asks for any of these and Admode's tools are connected.
---

# Admode

Admode works through its tools, whose names start with `admode_`. Each job's instructions and Admode's checks come from those tools, so this skill only says how to begin.

## Start a job

1. Load the user's brand with `admode_get_brand`. If they have more than one brand, it lists them: ask which one, then call it again with that brand.
2. Start the job with the tool that fits, before asking the user anything, because its result says what to ask:
   - static or image ads: `admode_generate_static_ads`
   - new versions of a static ad that works: `admode_generate_static_iterations`
   - AI UGC or creator-style video ads: `admode_generate_ugc_ads`, or `admode_generate_ugc_blueprint_ads` for an ad built like a video the user brings
   - podcast-style video ads: `admode_generate_podcast_ads`
   - animated video ads: `admode_generate_pixar_ads`, `admode_generate_claymation_ads` or `admode_generate_skeleton_ads`
   - ad copy: `admode_generate_ad_copy`
   - editing a finished video ad: `admode_edit_video_ad`
   - research: `admode_generate_voc_research`, `admode_generate_foundation_pack` or `admode_generate_brand_dna`
   - the user's Meta ads and their numbers: `admode_sync_meta_ads`
   - videos, images or music to keep for editing: `admode_upload_media`
3. Follow each result: it says what to ask, which tool comes next and when to check. Copy the ticket exactly from the latest result.

## Saved work and workflows

`admode_get_brand` lists the user's saved work and their own workflows. To carry on with saved work, call it again with `work`; to run a workflow, call it again with `workflow`.

## Before anything is rendered

Show the user the checked prompts first. Render only after they agree, with their own image and video tools: Admode writes and checks prompts, and doesn't render.

## If Admode isn't connected

If the `admode_` tools aren't available, tell the user how to connect Admode to their app: https://admode.ai/docs#connect
