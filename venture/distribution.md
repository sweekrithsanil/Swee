# Automated distribution: AI motion videos

Goal: a steady stream of short videos that make small-business owners say "I
want that for my shop", with as little daily effort as possible.

**The rule:** automate making and scheduling. Don't automate fake engagement
(mass comments, DMs, follows). Instagram bans that, and it would hurt the brand.
Every video gets a quick human look before it goes out.

## The loop

```
Idea -> Script -> Scene -> Voice -> Video -> Captions -> You approve -> Schedule -> Reply to leads -> Learn
```

| Step | What happens | Tool |
| --- | --- | --- |
| Idea | Find what's working in the niche this week | Agent Reach (`.agents/skills/agent-reach`), **local Claude Code only** |
| Script | 3 hooks, pick the best, 20-30 second script | Claude (the Instagram skill from `instagram-agent-skill` once installed) |
| Scene | The playable dashboard for that business type, screen-recorded as motion | Our HTML scenes (like Kitchen Run) recorded with Chromium + ffmpeg |
| Voice | AI voiceover in English, later Kannada/Hindi | ElevenLabs (connected in this setup) |
| Video | Extra AI motion clips and cutaways | ElevenLabs video / image tools |
| Captions | Burned-in subtitles, hook text on the first second | ffmpeg |
| Approve | You watch it, say yes or no | You, 5 minutes |
| Schedule | Queue at the best time | Scheduled routine + Instagram's own scheduler (Meta Business Suite) |
| Reply | Keyword comment gets the demo link on WhatsApp | WhatsApp Business auto-reply |
| Learn | Weekly numbers, keep what works | Claude weekly report |

## Weekly rhythm (about 1 hour of your time)

- **Monday:** Claude proposes 5 video ideas with hooks. You pick 3.
- **Tuesday:** Claude produces the 3 videos. You approve or reject.
- **Wed / Fri / Sun:** one video posts each day.
- **Sunday night:** Claude writes the week's report (views, comments, demo
  requests, which hook won).

## Video formats (reuse the same scene, change the business)

1. **"Your shop as a game."** 15 seconds, silent scene + one line of text.
   Example: "This is what a home kitchen looks like when orders are a game."
2. **Before / after.** Notebook page on the left, playable scene on the right.
3. **One number a day.** "3 scooters out, 2 orders late. Here's the fix."
4. **Festival special.** Ganesh Chaturthi, Diwali, Onam rush simulations.
5. **Customer story.** Once we have one: their scene, their words.

Hook ideas to test first (ASSUMPTION): "I turned a tiffin business into a
video game", "Your bakery's stock, but you can see it move", "What if your
clinic's waiting room was a level".

## Funnel

1. Reel ends with: "Comment KITCHEN and I'll send you a free demo."
2. WhatsApp Business auto-reply asks 2 questions (business type, can you send
   last week's orders).
3. We build the free demo in 48 hours (template + their data).
4. Demo goes back on WhatsApp. If they like it: setup + monthly plan.

## Metrics and kill rules

| Metric | Keep going if | Change something if |
| --- | --- | --- |
| Views per reel | Rising week to week | Flat for 3 weeks: change the hook |
| Comment keyword rate | 1%+ of views (ASSUMPTION) | Under 0.3%: change the call to action |
| Demo requests per week | 3+ | Under 1 for 4 weeks: change the segment |
| Demo to paid | 1 in 5 (ASSUMPTION) | Under 1 in 10: change the offer or price |

## Rules to stay safe

- Label videos made with AI voices or clips where the platform asks for it.
- Don't copy other creators' videos. The reel that inspired this is a reference,
  not source material.
- Don't claim customers, numbers or results we don't have yet. Demo data is
  marked "sample".
- Get permission before showing any real customer's data.

## What can't run in this cloud session

- Agent Reach: social sites are blocked here. Use it on a local install.
- Posting to Instagram: needs your Instagram Business account and Meta
  Business Suite, connected by you.

## Next steps

1. Install the Instagram skill locally or allow it here (see chat).
2. Choose the first segment and record the first 3 videos.
3. Set up WhatsApp Business with the keyword auto-reply. TODO.
