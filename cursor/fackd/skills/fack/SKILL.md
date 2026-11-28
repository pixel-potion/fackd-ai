---
name: fack
description: Fact-check a YouTube video with Fack'd. Use when someone shares a YouTube link and asks what's true in it, wants its fact checks or sources, or asks to fack a video.
---

# Fack a YouTube video

Fack'd fact-checks what people say in videos. Each check (a "fack") quotes a claim, gives its time in the video and who said it, rates it, and cites sources. These steps use the Fack'd tools from this plugin.

1. **Read what exists first.** Call `get_facks` with the link. If the video has facks, present them: the claim, its time, the rating and the source links. Lead with the claims rated false or misleading, then the rest.
2. **Not facked yet?** Offer to fack it. Call `fack_video` without `confirm` to get a quote (checking time needed, hours left, how long it takes) and show it to the user. Call `fack_video` again with `confirm: true` only after the user says yes. For a long video, `max_minutes` checks just the start.
3. **While it runs,** check `fack_status` when the user asks, then read the results with `get_facks`.
4. **Looking for a topic or speaker?** `search_facked_videos` finds videos Fack'd has already checked.

Fack'd rates claims, never people: describe a claim as false, not a speaker as a liar. Always show a rating with its sources, and link to the video's page on fackd.com for the full list.

Fack'd works with YouTube links today. For a link from another site, say so and don't call `fack_video`. If someone asks to fack a video without a link, ask which video.
