# GTM Launch Plan, Riverty business-unit case

| Field | Value |
|---|---|
| Feature | A fair way forward |
| Goal | Conversion |
| Launch tier | S, Minimal |

## Goal & Audience
- **Goal:** Conversion, Conversion. The feature’s job is to help more consumers who start an instalment request finish a plan on their own and keep it. The north-star SSR can rise while plans fail, so the goal is a sustainable agreement, measured by agreement rate (baseline 46%, target +4 pp) with the 60-day miss rate (baseline 19%) protected. Awareness is not needed: consumers are already sent to the portal by existing outreach.
- **Target audience:** Primary: Consumers who start an instalment request in the German portal in the pilot segment, like Mara (38, shift worker, variable income, on her phone after a reminder). Secondary: Collection agents like Daniel, who take escalated cases and need the handoff to work. Internal stakeholders who must be ready: compliance, data protection, and client account managers.

## Launch Tier
- **S, Minimal**, S for consumers: the pilot covers one segment in Germany, outreach and notifications stay unchanged, and no consumer-facing announcement is made, so the A/B result stays clean, will run for minimum 4 weeks. Silence carries little risk here because the feature appears at a point the consumer already reaches. The real launch risk is internal (agents who don’t know the new flow, compliance gaps on German copy), so enablement effort is high even though reach is low.

## Channels
1. **Owned: Existing reminder and collection letter, with digital reminder, leading to the portal. Unchanged in content and timing. This is the only way consumers arrive, and holding it constant is what keeps the test valid.**
2. **Owned: In-journey content in the portal: the “why we ask” line, option cards and consequence information are the launch. Mara learns about the feature by using it at the income step.**
3. **Owned: Agent channel (internal): briefing, a one-page guide and escalation notes, so agents like Daniel recognise cases that came through the new journey and know what the consumer saw.**

## Enablement & Assets
Agents (Daniel): short briefing on the new journey, a one-page cheat sheet on what consumers see, how “None of these fit” cases arrive, and how to log overrides.
Compliance and data protection: sign-off pack covering German copy, the self-declared budget, retention period, and plans without documents.
Clients and account managers: one-pager explaining the pilot, the control group, and the stop triggers.
Assets to build: German UI copy in a single strings file, consequence wording (compliance-approved), “why we ask” text, agent guide, stop-trigger dashboard.
Not needed: consumer announcement, email campaign, press.

## Ownership, Budget & Timeline
- **Ownership & budget:** PM (Fredrik): plan, experiment brief, post-launch metrics, go/no-go decision.
Design [Anna]: screens and German copy with compliance review.
Engineering [Anton], [Sara]: build, feature flag, step events.
QA [Sara]: test matrix, sample-ratio check.
Compliance lead [Bob]: copy and plan-bound sign-off, pause authority.
Data protection [Steven]: budget storage and retention.
Analytics lead [Lydia]: baseline re-measurement, interim safety look.
Agent team lead [John]: briefing and feedback loop.
Budget: no paid media. Costs are internal team time.
Asset gap: Agent guide one pager internal, external one pager tbd based on the test results.
- **Timeline:** 1: Beta, no consumers	1 to 8	Step-level tracking and baseline re-measurement (weeks 1 to 4), prototype tests with 8 to 12 participants (weeks 3 to 6), compliance, data protection and agent training (weeks 7 to 8)

2: Launch moment	9 to 16	A/B test in the pilot segment, 50/50, with interim safety look at 50% of sample. Minimum 4 weeks, running until about 4,349 starters per arm.

3: Post-launch	Enrolment close + 60 days	Miss-rate read, then the ship, iterate or kill decision. Extend to other segments only after that.

## Success Metrics
- **Metrics:** - Self-service agreement among starters: 46% to 50% (+4 pp target; ship threshold +3 pp), no agent contact before plan creation.
- 60-day missed-payment rate among new agreements: no more than +3 pp above control (baseline 19%).
- 7-day agent contact among starters: no more than +2 pp above control (baseline 31%; the 2 pp margin is a placeholder to agree with operations).
- **Bad signal to watch for:** Agreement rises but the 60-day miss rate rises with it (3 pp or more above control), or first-payment failure spikes early (after 60 days). That is the SSR trap: more plans created, fewer plans kept.
- **Likely post-launch decision:** Iterate, most likely, because the 60-day read may be inconclusive at the available sample. Scale (25%, then 50%) if agreement is up by at least 3 pp, the miss-rate upper bound stays below +3 pp, and contact and complaints hold. Kill if the full-sample agreement interval cannot reach +3 pp, or the miss rate is 3 pp or more above control with the interval excluding zero.
