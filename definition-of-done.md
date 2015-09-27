---
layout: mechanics
title: Definition of Done
order: 87
---

Scrum’s inspect-adapt cycles require transparency in order to be effective. Formally defining the meaning of ‘done’ reduces variability and the likelihood of undone work and measuring progress unambiguously (‘done’ or ‘not done’) increases transparency.

A perfect Definition of Done includes everything that the organization has to do to deliver the product to customers. Achieving this should be relatively easy for a one-team product group. When the team isn’t able to achieve the perfect Definition of Done then they define ‘done’ as a subset of the perfect set. The team’s goal is to improve so that, one day, their Definition of Done is perfect and they can ship each Sprint or more.

The Definition of Done is an agreed list of criteria that the software will meet for each Product Backlog Item. Achieving this level of completeness requires the Team to perform a list of tasks. When all tasks are completed, the item is done. Don’t confuse the Definition of Done with acceptance criteria, which are specific conditions an individual item has to fulfill to be accepted. The Definition of Done applies uniformly to all Product Backlog items.

## Creating the Definition of Done

The initial Definition of Done must be agreed before the first Sprint. This usually happens in the [Initial Product Backlog Refinement workshop](initial-product-backlog-refinement.html).

The following steps are taken in order to create the Definition of Done:
* Define the activities needed to ship to end customers.
* Decide which activities can be done each Sprint.

Let’s explore these steps in more detail.

### Define the activities needed to ship to end customers

They key question is, “What activities are currently required to ship our product?”

* Shipping means “delivering to end customers” and not “send out of the development department.”
* Challenge the need for intermediate artifacts. Do we really need that specification document?

The teams write post-it notes with required activities. These include activities such as coding and testing but may also include setting up customer support, creating hardware, or even marketing activities. We refer to this list as the required activities for having a Potentially Shippable Product.

With this step, you have created a [perfection goal](../principles/continuous-improvement-towards-perfection.html) for the organization—do all these activities for each item every Sprint. Product groups now often realize this will take a lot of improvements.

### Decide which activities can be done each Sprint

The key question is, “Considering our current context and capability, what activities can be completed each Sprint?” This subset is the initial Definition of Done. A Definition of Done is weak when it is a small subset and strong when it is almost equals Potentially Shippable.

The teams discuss their context and select the subset of the activities that all teams think they realistically can do during the Sprint. This is their initial Definition of Done (see example in Figure 1). The teams that can do more will expand this product Definition of Done within their teams.

The difference between the Definition of Done and Potentially Shippable is referred to as Undone Work. The Sprint is planned according to the Definition of Done and thus the Undone Work is excluded—it is planned to be left undone

<figure>
  <img src="/img/framework/dod.jpg" alt="dod.jpg">
  <figcaption>Figure 1. Potentially Shippable and Definition of Done.</figcaption>
</figure>

## Definition of Done terms

The terms Potentially Shippable and Definition of Done are often not used consistently, but in LeSS they have very precise meaning. To clarify the terms:

**Potentially Shippable**—All activities that must be performed before the product can be shipped.

**Definition of Done**—An agreement between the teams and the Product Owner on which activities are performed inside the Sprint. A Definition of Done is perfect when it equals to Potentially Shippable. The teams strive to improve towards a perfect Definition of Done.

**Undone Work**—The difference between the Definition of Done and Potentially Shippable. When the Definition of Done is perfect then there is no Undone Work. If this isn’t the case then the organization has to decide, (1) How do we deal with the Undone Work, and (2) How do we improve so that there is less Undone Work in the future.

**Unfinished, not finished, or not done**—Work that was planned in a Sprint but wasn’t completed. This is often confused with Undone Work. ‘Unfinished’ is work that the team planned for but didn’t finish whereas Undone Work was never even planned for. When a team has work that was not finished then they ought to feel anxious and discuss improvement actions during their Retrospective.

Teams should never leave work-in-progress at the end of the Sprint and “carry over” to the next one. This causes a lack of transparency and reduces scope flexibility. If they forecast too much work, they need to remove complete items which they haven’t started yet.

### Mathematics of Done

Potentially Shippable = Definition of Done + Undone Work
Work in Iteration = Product Backlog Item * Definition of Done
{: .box_top_bottom  .text_centered_bold }

## Undone Work -> Risk and Delay

Let’s first explore the effects of Undone Work by running through a scenario.

The teams completed—according to the Definition of Done—twenty Product Backlog Items in the first Sprint. They have no unfinished work but there is a lot of Undone Work due to their weak Definition of Done. After the teams completed—according to the weak Definition of Done—forty Product Backlog Items in three Sprints. The amount of Undone Work has grown enormously causing a false sense of progress.

But they can’t ship. They have ‘done’ the features but their weak Definition of Done caused a vast amount of Undone Work to accumulate. This Undone Work causes delay and hidden risk.

**Delay**—Extra effort is needed to perform the Undone Work. This causes a lack of flexibility for the Product Owner—he can’t directly respond to market needs and changes. The pain caused by this delay is aggravated by the fact that the effort to complete the Undone Work is highly variable and thus hard to predict.

**Risk**—The Undone Work causes a lack of transparency. Risks are hidden in it. For example, if performance testing is left Undone then it delays the risk of a non-performing system until close to release—when it hurts most.

A good Product Owner wants a perfect Definition of Done as that reduces product risk and avoids delay.

