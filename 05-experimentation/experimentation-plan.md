# A/B Experiment Brief, Riverty business-unit case

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Affordable Plan Options v1 (PRD M1 to M7 as one package): self-declared monthly budget, 2 to 3 sized plan options with “why this option”, consequence panel, confirm, agent exit |
| Persona | Mara, 38, consumer. Shift worker with variable income, opens the portal on her phone after a reminder. Goal: settle a claim with an affordable plan she can keep |
| Expected outcome | Self-service agreement among starters 46% to 50% (+4 pp), with the 60-day miss rate no worse than control |
| Primary success metric | Self-service agreement rate among starters: share of journey starters who create a plan with no agent contact before plan creation |
| Baseline rate | 46% (replace with the pilot segment’s measured rate from Phase 0) |
| Guardrail metric | 60-day missed-payment rate among new agreements (baseline 19%) |
| Guardrail boundary | Variant no more than +3pp above concurrent control (non-inferiority, one-sided α = 0.025) |
| Second guardrail | 7-day agent contact among starters (baseline 31%): variant no more than +2pp above control |
| Minimum Detectable Effect | +3 pp absolute (46% to 49%); target +4 pp |
| Sample size per arm | 4,349 |
| Traffic split | 50/50, randomised at consumer level |
| Test duration | Minimum 4 weeks, run until at least 4,349 starters per arm (8,698 total). Miss-rate read 60 days after enrolment closes |
| Significance threshold | 0.05 two-sided (equivalent to 0.025 one-sided) |

## Control vs. Variant
- **Control (A):** Current German portal instalment journey for the pilot segment, unchanged. After opening the portal from a reminder/colleciton letter, the consumer starts an instalment request and is asked for income information, with income documents uploaded at the income step. No reason is given for why income is requested, and no plan options sized to the consumer’s situation are shown before commitment. Documents that are unclear or unreadable go to manual review or clarification by an agent. Phone and email routes to an agent remain available at all times.
- **Variant (B):** The income step changes from document upload to one question (“What can you comfortably pay each month in a low-income month?”, with a “why we ask” line), and the answer produces 2 to 3 plan options sized to that amount, each showing monthly amount, number of payments, end date and total. No option is pre-selected. Everything after the option is chosen is identical to control.
- **Held constant (isolation check):** Outreach and the notification that sends consumers to the portal, including timing and content
How consumers reach the instalment journey from the portal
Eligibility rules, and the minimum and maximum plan terms the control could already grant
Confirmation step, consequence wording and payment processing
Agent availability, staffing and routing, including phone and email
Any other backlog release (for example “Why We Ask” labels or the consequence panel) in the pilot segment during the test

## Hypothesis
> I believe that Affordable Plan Options v1 (PRD M1 to M7 as one package): self-declared monthly budget, 2 to 3 sized plan options with “why this option”, consequence panel, confirm, agent exit for Mara, 38, consumer. Shift worker with variable income, opens the portal on her phone after a reminder. Goal: settle a claim with an affordable plan she can keep will result in Self-service agreement among starters 46% to 50% (+4 pp), with the 60-day miss rate no worse than control, as measured by a +3 pp absolute (46% to 49%); target +4 pp change in Self-service agreement rate among starters: share of journey starters who create a plan with no agent contact before plan creation within Minimum 4 weeks, run until at least 4,349 starters per arm (8,698 total). Miss-rate read 60 days after enrolment closes. We will protect 60-day missed-payment rate among new agreements (baseline 19%) throughout the test.

## Shipping criteria
> We will **ship** if Self-service agreement rate among starters: share of journey starters who create a plan with no agent contact before plan creation improves by ≥ +3 pp absolute (46% to 49%); target +4 pp at 0.05 two-sided (equivalent to 0.025 one-sided) and 60-day missed-payment rate among new agreements (baseline 19%) does not reach Variant no more than +3pp above concurrent control (non-inferiority, one-sided α = 0.025) after Minimum 4 weeks, run until at least 4,349 starters per arm (8,698 total). Miss-rate read 60 days after enrolment closes.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of Minimum 4 weeks, run until at least 4,349 starters per arm (8,698 total). Miss-rate read 60 days after enrolment closes, no results reviewed before this date.
