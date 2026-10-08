# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Affordable Plan Options (later feature)
It directly answers "can I afford this?" for variable income, but it needs real BE logic and must never default to the highest payment.
- **My finalized Must-Haves (after overriding the AI):** One-question budget input, no documents. Ask "What can you comfortably pay each month in a low-income month?" and give a reason for asking it.

2 to 3 rules-based plan options showing monthly amount, number of instalments, end date, and total to pay. Options are sized to her stated budget, with bounds and rules held as configuration, not hard-coded.

A plain-language "why this option" line on each option, for example "based on the amount you told us."

Neutral presentation: no option pre-selected, none defaulting to the highest payment, and the lowest-burden option always visible.

"None of these fit" exit to an agent, passing the amount entered and the options viewed.

Confirmation step showing the plan terms, requiring an explicit confirm, with a way back. It reuses the F5 consequence panel from the Now lane.

Mobile-first layout in German, usable on a 375px-wide phone with no horizontal scroll.
- **What I demoted from Must → Should/Won’t, and why:** Show the combined total across both claims, with the sum of monthly amounts if she sets up a plan on each

Gives Mara the two-claim picture without building F6. (Two claims one plan overview, later item)

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The prototype has no generative model. Every figure comes from a deterministic function that is checked against the balance before it renders, and every sentence is a static template with numbers inserted. Consequence text is a single compliance-approved string, never generated. If any check fails, the screen falls back to the agent route rather than showing unverified content.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** Some plans may show only one option. With your rules, amounts between €35 and €39 leave just one plan that stays within 24 months, so you'll see one card instead of 2–3.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://lovable.dev/preview/hWEY7fjG7w27UzMAksCZk4oiIKddf3w4
