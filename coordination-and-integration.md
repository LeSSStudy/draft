---
layout: mechanics
title: Coordination & Integration
order: 80
---

Scrum values decentralized, self-organized coordination and integration over the centralized, controlled coordination found in traditional project management. LeSS coordination and integration concentrates on how to support decentralized coordination while providing enough boundaries and structure to avoid chaos.

## Just Talk

Probably the best way to coordinate between teams is to simply coordinate between the teams. Any member of a self-managing team would be able and expected to reach out to another team if there is an issue to be discussed. When there is a need for coordination then "just talk" by going to the other team, picking up the phone or, in the worst case, dropping them an email. You do not need a formal, official, usually slow coordination mechanism in order to coordinate. Get up and talk to people.

## Communicate in Code

LeSS groups adopt [continuous integration](../technical-excellence/continuous-integration), which means that everyone has all their code checked in to the central repository mainline (branches are an unnecessary complication that should be avoided). Everyone in the product teams synchronizes with the repository several times a day and will get all the changes that other people have made.

So, when you update, spend two minutes going over the changes that were made by others and see if they relate to what you are working on now. If so, feel free to get up and "just talk" in order to synchronize your work with the others!

## Send Observers to the Daily Scrum

A simple coordination method for teams is to send a representative —not the ScrumMaster—as a silent observer to the Daily Scrum of other teams doing related work. The observers then report back to their teams so they can take further action.

## Component communities and guardians

People working on the same components at the same time need to know of each other so they can ask questions and review each other’s code. Do this by creating component [Communities of Practice](../structure/communities.html) (CoPs), which should communicate via mailing lists, chat, occasional meetings, and other remote collaboration channels.

These communities are often organized by a “component guardian” who is usually a member of a feature team who has taken some additional responsibilities such as (1) being the teacher of how a component works, (2) monitoring the long-term health of a component, (3) organizing a component community, (4) organizing design workshops, and (5) reviewing code.

A component guardian doesn’t review code for approval before it’s committed. He’s a teacher and steward of the component, not a gate.

A component may have several guardians who share the work and thereby reduce key-person dependency.

Important!… Besides helping coordination, these practices help maintain or improve the code/design quality of a component, and increase learning.

## Scrum of Scrums

A Scrum of Scrums meeting is a Daily-Scrum-like meeting between teams, typically held two or three times per week.

Does it have to involve all teams? No. Subsets of teams can do it when they have a compelling need to coordinate.

A healthy Scrum of Scrums meeting is attended by team members who do actual development work and not ScrumMasters or the Product Owner. The people in the Scrum of Scrums are there for the sole purpose of coordinating real work between teams.

Usually the format is three questions, similar to a Daily Scrum:

* What did my team do that is relevant to other teams?
* What will my team do that is relevant?
* What are my team’s obstacles that other teams should know about or can help with?

Naturally, use and evolve whatever questions your group finds useful.

A caution: The desire to hold a Scrum of Scrums can be a sign of unnecessary dependency or coordination problems caused by single-function groups and component teams, or by teams not able or willing to identify and do shared work.

It can also be a sign of ScrumMasters who are actually team leads or managers getting together for a “leadership meeting.” Don’t let that happen because it will tend to diminish the self-organization of the teams involved as they sense that someone is taking over command and control leadership.


## Multi-team meetings

It is common for some teams to need to work closely together whereas others may not feel that need. For teams that work closely together, it is common to have multi-team LeSS meetings. Some examples would be:

* Multi-team [Product Backlog Refinement](product-backlog-refinement.html)
* Multi-team [Sprint Planning Two](sprint-planning_two.html)
* Multi-team [Design Workshops](../technical-excellence/architecture-design.html)
* Exchange members in Daily Scrum.

## Travelers to exploit and break bottlenecks and create skill

Sometimes a product group relies on a couple of experienced technical experts. How can the knowledge of these (scarce) experts be kept available to all teams? They can become travelers. Each Sprint they join a different team, coaching via pairing, workshops, and teaching sessions.

Although travelers are not specifically created for coordination, by joining different teams they create or strengthen a broad network, which is exactly what is needed for informal coordination channels. And they increase the consistency of some knowledge or practice across teams, realizing a coordination goal.

## Leading Team

In some domains, features are monstrously large. When you split these giants into smaller Product Backlog Items, it can require many teams working closely together, each separately on its own PBI, to create a single monster feature.

Another technique for coordinating teams working together on the split items of a big related feature is a leading team. A leading team is just a regular feature team that takes a leading role for the overall giant feature. In addition to doing development work, they are responsible for keeping track of what the other teams are doing and helping them synchronize. In short, they organize cross-team coordination related to the giant in addition to themselves doing development.

Sometimes several teams start implementing the giant at the same time. At other times, the leading team starts alone to focus the early knowledge transfer and simplify the creation of a cohesive design. After a few Sprints, more teams join. In this case the lead team also has a teaching responsibility to help the incoming teams learn what they already know.

