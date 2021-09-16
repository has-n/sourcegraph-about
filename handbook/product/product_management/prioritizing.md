# Prioritizing

## Saying "no"

We receive tons of feature requests and bug reports, more than we can handle. This means we must frequently say "no" or prioritize things less urgently than some people would like. Our job is to find the most important things to work on.

## How do I get something prioritized by our product team?

- [Create a GitHub issue](https://github.com/sourcegraph/sourcegraph/issues/new/choose) OR [write an RFC](../../communication/rfcs/index.md).
  - Include as much detail as possible about the issue.
  - Provide context around urgency and priority.
  - Link to the customer (if applicable) in this [spreadsheet](https://docs.google.com/spreadsheets/d/1OEhzdMSlkGOaWyGKwdiAGlirsKKj9EN45Izn7kdKNTg/edit#gid=0)
  - Add the team label on the issue for the team that should be responsible for it.
- Share with the team in any of the following ways:
  - Post link to the issue in Slack and ask the team to prioritize the issue in the next team sync (or let them know it is a P0 that should be handled immediately).
  - Send to the Product Manager to prioritize with the team.
  - Add the item to the [team's board](planning.md) for consideration

### Engineering prototyping

Sometimes there is a general product area that the CEO/CTO/Product Manager/CE/Sales seem interested in, and a developer is passionate/inspired/excited about it and wants to work on prototyping in that area. The developer has total freedom for a couple months to work on it part-time as long as they make progress in prototyping with the Sales and CE teams and are showing progress to customers regularly. The sole test will be, if we ask the Sales/CE teams "is $DEVELOPER's prototype/project drawing interest in customer calls and is $DEVELOPER iterating on it well in response to feedback?"

## Prioritizing bug fixes and small tasks

Bugs and issues from customers come up regularly and need to be prioritized. Many of these tasks are quick (< 1 day) and should be prioritized within the iteration. Larger tasks should be added to the project roadmap. Customer issues should include context about how important that customer is, and how important this particular issue is to the customer so that teams can effectively prioritize. The goal is not to have the engineering teams jump at every customer request, but to thoughtfully triage them when compared to the rest of the work they have slated. If there is any ambiguity in importance, the PM can be consulted to help make prioritization decisions.

Each team may decide how they would like to keep track of the backlog of issues, whether that is in a kanban board, google doc, etc. Similarly, teams can decide how they would like to allocate resources to this, whether it is having one person working down the backlog each week, or assigning a set of issues to be accomplished within an iteration.

## Prioritizing requests that impact the project roadmap

Sometimes, we need to prioritize changes to our product on short notice due to new information we have. This change could be to benefit [customers](../../sales/index.md#customer) or [prospects](../../sales/index.md#prospect), or could be a strategic initiative.

If the requested change is large enough that it would impact the planned [project roadmap](../index.md#roadmap) of one or several [engineering teams](../../engineering/index.md#teams), we should handle its prioritization as follows:

1. The product manager should contact all relevant [engineering managers](../../engineering/roles.md#engineering_manager), providing the following information in the form of an [RFC](../../communication/rfcs/index.md):
   - Description of the desired functionality.
   - Context on why is this important: the customers or prospects that would benefit from the change, the size of the opportunity, and the risks of not doing this work.
   - Desired timeline for the change: when do we need this by?
   - Desired timeline for the evaluation: how soon do we need to know whether we can deliver this?
1. Engineering managers own providing a timely answer, either directly or by delegating evaluation of the request to a [software engineer](../../engineering/roles.md#software-engineer) on their project team. If cross-team coordination is needed to evaluate the request, engineering managers own facilitating this coordination. The evaluation should be provided in the form of an [RFC](../../communication/rfcs/index.md), or added to the original RFC provided by the product manager, and should include:
   - An estimation of the amount of work needed to implement the request.
   - If the amount of work needed spans more than one milestone, a proposed breakdown of incremental changes (for example, shipping a first functional but slow implementation in milestone N then working on performance in milestone N+1).
   - An overview of work that would get deprioritized if we chose to prioritize the request.
   - Any concerns raised by the request: stability, scalability, cost, performance.
   - A recommendation on whether to move forward with prioritizing the request:
     - OK to move forward.
     - Recommend not moving forward: this may be because of outstanding concerns, or because prioritizing the request would lead to deprioritizing important engineering goals.
1. Based on the evaluations provided by engineering manager, the product manager owns:
   - Making a final decision on whether to prioritize the request.
   - Communicating this decision to the engineering and sales/CE teams.
1. Engineering managers own updating the project roadmap and iteration plans to reflect the product manager's decision.

## Prioritizing things that impact current iteration plans

Sometimes, we need to prioritize changes to our product on _very_ short notice due to new information we have. Generally, short-term re-prioritization should not significantly change any in-progress iteration (milestone or sprint), but should provide the engineering team with sufficient data to alter their _upcoming_ iteration. Interrupting the current iteration can negatively impact engineering velocity and morale, can delay planned feature delivery, and contribute to engineer context switch fatigue and burnout.

However, extenuating circumstances exist that would encourage us to break this rule (all subject to interpretation):

- A bug that is significantly impacting Sourcegraph Cloud.
- A bug that is significantly impacting a managed or on-premise instance.
- A bug that is significantly impacting a prospective customer.
- Critical, time-sensitive opportunities.

Important questions to ask while re-prioritizing and proposing solutions for critical, short-term work:

- Is an instance totally broken?
- What is the impact to the business?
- What happens if we don't do this?
- What is the real (vs. perceived) urgency?
- How does this impact the work that is planned?
- Is this thing more important than what is planned?
- Is this a hack? Will this be a sustainable solution?
- Can we do it "right"? How long would that take?
- Are we already planning on solving this? How long until we work on this? Is that timeline acceptable?

## Customer requests

Customer issues should reference the link to the company in HubSpot. **Note that the URL should never be hidden in a markdown link (such as `[company name](https://app.hubspot.com/contacts/XXXXXXX/company/XXXXXXX)`) as GitHub issue search doesn't search the full markdown, only the rendered text.**

Please make sure the URL looks like `https://app.hubspot.com/contacts/XXXXXXX/**company**/XXXXXXX`. If the link ends in `/**deal**/XXXXXXX` or `/**ticket**/XXXXXXX` searches for the company's id won't return the comprehensive set of issues.

### Finding all requests from a given customer

Visit the company's page on HubSpot, copy the unique identifier at the end of the URL, and search in GitHub. All issues filed on behalf of the company will appear.

> NOTE: Pro tip: use the [HubSpot Sourcegraph extension](https://sourcegraph.com/extensions/sourcegraph/hubspot) for autocompleting names and adding customer names to your view!