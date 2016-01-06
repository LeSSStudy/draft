---
layout: mechanics
title: Introduction to LeSS
order: 5
---
(this is chapter 2 of the [forthcoming book "Large-Scale Scrum: More with LeSS" ISBN 9780321985712](http://www.amazon.com/Large-Scale-Scrum-More-Craig-Larman/dp/0321985710))

<div class="chapter_quote"><p>
Two economists are walking down the street. One sees a paper. “Is that a $100 bill?”
<br/>
“No.” his friend replies, “If it were a $100 bill, someone would have picked it up already.”
</p></div>

## One-Team Scrum

In a nutshell... Scrum is an empirical process control development framework in which a cross-functional self-managing team develops a product in an iterative incremental manner. At the end of each (on average) two-week *Sprint* a completely ‘done’ *potentially shippable product increment* (for short, *shippable increment*) is delivered, and possibly shipped. A single *Product Owner* is responsible for maximizing product value, prioritizing *items* (features) in the *Product Backlog*, and adaptively deciding the goal of each Sprint based on frequent inspection. A *Team* of about seven is responsible for delivering the Sprint goal, and they have or learn all required skills. There are no special job titles and no single-specialized sub-teams. A *ScrumMaster* educates about Scrum and how to derive value with it, and coaches the Product Owner, Team, and organization to apply it. There is no project manager, team lead, or other role in Scrum. A Sprint starts with *Sprint Planning*, and ends with a *Sprint Review* and *Sprint Retrospective* to inspect and adapt, respectively, about the product and processes.

*Empirical process control* requires transparency, which is created through short-cycle iterative development of shippable increments. It emphasizes continuous learning, inspection, and adaptation about both product and processes. It is based on recognizing that in product R&D things are too complex and dynamic for detailed, formulaic, and “one size fits all” organization and process recipes.

In the *Scrum Guide* and *Scrum Primer*, Scrum is described for one team.

## LeSS

Large-Scale Scrum (LeSS) is Scrum applied to many teams working together on one product. Why LeSS? Similar to one-team Scrum...

> For large groups, LeSS hits a sweet-spot balance between defined concrete elements and empirical process control.

And just like one-team Scrum, LeSS is (1) lightweight, (2) simple to understand, and (3) difficult to master—due to essential complexity.

### Background

In 2002, when Craig wrote *Agile & Iterative Development*, many ‘knew’ that agile development was for small groups. However, we became interested in—and got increasing requests—to apply Scrum to very large and multisite product development. So, since 2005 Craig and Bas have teamed up to work with clients to scale up Scrum. Today, the two LeSS frameworks (basic LeSS and LeSS Huge) have been adopted in big product groups worldwide in disparate domains, including:

* telecom-equipment creators such as Ericsson & Nokia Networks
* investment and retail banks such as JPMorgan and BAML
* trading-system creators such as ION Trading
* gaming site creators such as bwin
* offshore outsourcers such as Valtech India

To quantify ‘large’, as of this writing, at the top end we are involved in a LeSS Huge adoption in a product group of about 2500 people, 10 developments sites, tens of millions of lines of C++, with custom hardware.

What’s an industry-median LeSS product group size? Perhaps three to five teams in one or two sites.

Based on our experiences, in 2008 and 2010, we published two volumes on scaling agile development with the LeSS frameworks:

1. *Scaling Lean & Agile Development: Thinking and Organizational Tools for Large-Scale Scrum*, that explains the thinking, leadership, and organizational design changes.
2. *Practices for Scaling Lean & Agile Development: Large, Multisite & Offshore Product Development with Large-Scale Scrum*, that explains concrete advice for scaling Scrum, including in product management, architecture, planning, multisite, offshore, and contracts.

This is the third book in the LeSS series, a prequel and primer. It summarizes rather than replaces the others. If you want, um… more LeSS details, read the first two volumes or the website less.works.

### LeSS Principles and Themes

<figure>
  <img src="/img/principles.png" alt="principles.png">
  <figcaption>Figure 2.1 LeSS principles</figcaption>
</figure>

**Large-Scale Scrum is Scrum**—It is not “new and improved Scrum.” Rather, LeSS is about figuring out how to apply the principles, elements, and purpose of Scrum in a large-scale context.

**Empirical process control**—Inspection and adaptation of the product, processes, organizational design, and practices to craft a situational appropriate organization based on Scrum, rather than following a detailed formula. And empirical process control requires and creates…

**Transparency**—Based on tangible ‘done’ items, short cycles, working together, common definitions, and driving out fear in the workplace.

**More with less**—(1) In empirical process control: more learning with less defined processes. (2) In lean thinking: more value with less waste and overhead. (3) In scaling, less roles, artifacts, and special groups.

**Whole-product focus**—One Product Backlog, one Product Owner, one potentially shippable product increment, one Sprint—regardless if there are 3 or 33 teams. Customers want the product, not a part.

**Customer-centric**—Identify value and waste in the eyes of the paying customer. Reduce the cycle time from their perspective. Increase feedback loops with real customers. Everyone understands how their work today directly relates to and benefits paying customers.

**Continuous improvement towards perfection**—Create and deliver a product all the time, with no cost and no defects, that utterly delights customers, improves the environment, and makes lives better. Do humble and radical improvement experiments each Sprint towards that.

**Systems thinking**—See, understand, and optimize the whole system (not parts), and use causal-loop modeling to explore system dynamics. Avoid the local and sub-optimizations of focusing on the ‘efficiency’ or ‘productivity’ of individuals and individual teams. Customers care about the overall concept-to-cash cycle time and flow, not individual steps.

**Lean thinking**—Create an organizational system whose foundation is managers-as-teachers who apply and teach systems thinking and lean thinking, manage to improve, and who practice Go See at gemba. Add the two pillars of respect for people and continuous improvement. All towards the goal of perfection.

**Queuing theory**—Understand how systems with queues behave in the R&D domain, and apply those insights to managing queue sizes, work-in-progress limits, multitasking, work packages, and variability.

### Two Frameworks: LeSS & LeSS Huge

Large-Scale Scrum has two frameworks:

* **LeSS**: 2–‘8’ Teams.
* **LeSS Huge**: ‘8+’ Teams, up to a few thousand people per product.

The word ‘LeSS’ is overloaded to mean both Large-Scale Scrum in general, and the smaller basic LeSS framework. We find this convenient.

**LeSS Framework**—The (basic) LeSS framework is for one overall Product Owner (PO) and two to ‘eight’ teams. There is one overall real **Product** Owner (who truly “owns the product”) for one real shippable product, who manages one Product Backlog worked on by all the teams in one Sprint, optimizing for the whole product.

‘Eight’ is not a magic number for choosing between LeSS and LeSS Huge. The tipping point is situational. At some point, (1) the single overall PO can no longer grasp an overview of the entire product, (2) the PO cannot balance an external and internal focus, and (3) the Product Backlog is so large that it becomes difficult for one person to work with.

When the group *tips*, time to change. Perhaps to LeSS Huge, but try first to get smaller and simpler, not *huger*.

The remainder of this major section explains the smaller **LeSS framework**; the **LeSS Huge framework** is covered later.

### LeSS Framework Elements

The (smaller) LeSS framework elements are essentially the same as one-team Scrum:

**Roles**—one overall Product Owner, two to ‘eight’ Teams, ScrumMasters.

**Artifacts**—There is one potentially shippable product increment, one Product Backlog, and a separate Sprint Backlog for each Team.

**Events**—There is one Sprint for the whole product; it includes all teams and ends in one potentially shippable product increment. Event details are explained in the upcoming LeSS *stories*, and in separate chapters.

<figure>
  <img src="/img/framework/less-framework.png" alt="less-framework.png">
  <figcaption>Figure 2.2 LeSS framework</figcaption>
</figure>

In addition to these elements, LeSS includes:

**Rules**—Things the group should follow and do, such as Sprint Planning One and Two, and one Product Backlog for the shippable product. There are LeSS rules related to roles, artifacts, and events.

The few simple LeSS rules balance the low ‘prescriptive-ness’ required for empirical process control and the need especially for new adopters for some specific direction to know *what and how* when starting. And then be able to truly create transparency with LeSS. “More specific when starting” reflects the *introductory*-level learning needs recognized in several learning models. The jazz trumpeter and teacher Clark Terry neatly summed up the learning progression: Imitate, Assimilate, Innovate. Some know this as *Shu-Ha-Ri* (follow, detach, transcend) in Akido.

**Guides**—Advice to try, based on the experience of LeSS adopters, such as how to coordinate across teams during the Sprint. May or may not be appropriate, and are areas for continuous improvement experiments.

How to grasp the LeSS elements in practice? We’ll tell some stories...

### LeSS Story: Flow of Teams & Events

> This story emphasizes the flow of *people and teams* going through events in a LeSS Sprint. A later story emphasizes the flow of customer features through events.

On a crisp and sunny London morning, Dave walks into the distinctive ‘Gherkin’ building in the financial heart of The City. He takes the lift up to the 17th floor, and heads into the room where his team works—Team Trade, who collectively know quite a lot about trading European bonds. Devi’s already there, but not the rest of the crew. “Good morning!” she greets Dave. “Just a reminder: We’re the team representatives this Sprint and Sprint Planning One starts in 10 minutes.” “Right,” says Dave, “I’m gonna grab an espresso and meet you in the big room.”

#### Sprint Planning One

A few minutes later Dave settles down into a chair in the big room. Devi and a few other developers came in right behind Dave, and now there’s quorum—there’s 10 team representatives from the five teams who work on their flagship product for trading bonds and managing position risk. Sam, the ScrumMaster of teams Trade and Margin, is already there. He’s planning to observe, and coach as needed. The group is starting their 4th two-week Sprint using LeSS, and it’s time for a common timeboxed two-hour Sprint Planning One.

Paolo walks in and says “Hi!” to the group. He’s the Product Owner and also the lead Product Manager. Two other Product Managers are already sitting at a table. Paolo lays out 22 ordered cards on a table, and says, “Here’s my offer for this Sprint. In addition to many Brazilian market features, some of the items are for new auditor reports for USA bond derivatives.”

<figure>
  <img src="/img/framework/sprint-planning-one-sketch.jpg" alt="sprint-planning-one-sketch.jpg">
</figure>

Sam reminds the group, “Don’t let all the highest-priority items be taken by one team. Try to distribute them across most of the teams.”

Dave and Devi walk over to the table (along with the other representatives) and they pick two cards for items related to European bonds that their team did the detailed Product Backlog refinement on over the last few Sprints. They pick a third item related to general order management that most of the teams understand quite well. A minute later, Dakota from Team Margin, on scanning Team Trade’s cards, asks Dave and Devi, “Can we do your order management feature? We did something similar last Sprint. We can swap with you for this new very straightforward report we picked up.” They agree.

After about five minutes, all the team representatives have chosen a total of 18 cards, leaving 4 relatively low-priority ones on the table. Paolo looks them over, picks one up, and says, “This one here is pretty important to me this Sprint. Let’s find a way to swap it with one of the items you’ve already chosen.”

After that’s resolved, it’s time for each team to craft a Sprint Goal and to clear up remaining questions—there’s always questions, even though these items were clarified in Product Backlog refinement in prior Sprints. In parallel, Dave, Devi, and the others write questions for their chosen items on flip-chart papers. Paolo and the two other Product Managers split up and visit different people, answering questions. After about 45 minutes, all lingering questions have been answered that could be answered.

Then Sam announces, “A reminder: The last thing we need to talk about together is *coordination.*” Don from Team Margin points out that one of the European bond items involves shared work with two items from Team Margin. Dave suggests, “Let’s hold our SP-two meetings together,” and Don agrees.

#### Sprint Planning Two

After a break, each team holds their own Sprint Planning Two, which is most often identical as in one-Team Scrum. But in this story...

Teams Trade and Margin hold a multi-team Sprint Planning Two: their individual meetings together in the big room, working at separate tables. They discover large design questions about their related items. Some of these questions they quickly answer with discussion and sketching on a whiteboard, but a few complex ones are deferred. For those, they agree to hold a *multi-team* Design Workshop after Sprint Planning. The teams recognize that may change some planning assumptions.

Shortly after Sprint Planning, a representative from each team updates the one common Product Backlog (a Google spreadsheet) with their team’s forecast of items they will do for the Sprint.

#### Multiteam Design Workshop

After another break, Dave and Devi from Team Trade, and a few people from Team Margin hold a timeboxed one-hour multi-team Design Workshop. Around a large whiteboard they do agile modeling until they have some clarity and agreement on a common design approach and shared technical work. Fortunately, the conclusions don’t seriously impact their existing Sprint plans, but they feel uncomfortable with their process, recognizing they could have predicted needing to resolve these big design questions earlier.

#### Overall Retrospective

On the second day of the Sprint, Sam and the other ScrumMasters, the Product Owner Paolo, a site manager named Mary, and one representative from each of the other teams, all get together for a 90-minute overall Retrospective related to the last Sprint. (They couldn’t hold an overall Retrospective at the end of the Sprint, because it finished with the regular team-level Retrospectives.) They focus on a system-wide issue and improvement: how to coordinate, share information, and solve problems across the entire group during the Sprint? Previously they have tried Scrum-of-Scrum meetings and didn’t find them very effective. Sam explains the technique of Open Space, and they agree to try that this Sprint.

#### Day 4 Coordination (coordinating in an example LeSS day)

In LeSS, each Team holds a Daily Scrum as usual. But to support coordination between Teams Trade and Margin, Devi joins Team Margin’s Daily Scrum. Conversely, Don joins Team Trade’s.

As agreed in the overall Retrospective, Dave and Devi join a group-wide 45-minute *Open Space* meeting for Sprint coordination with the team representatives. Sam acts as facilitator to teach the group.

Don is this year’s coordinator for the Test community of practice (CoP). He gets together for a half hour with a representative from each team so they can hear Dakota’s proposal related to their automated acceptance testing tool. It’s enthusiastically agreed, and Dakota volunteers her feature team to do the actual work next Sprint.

Dave is a member of the Architecture CoP. There’s no meeting this Sprint, but he wants to hold a half-day spike in the next Sprint for exploratory group programming with a new technology. He posts his idea to other members on their CoP collaboration tool.

The build and continuous integration (CI) system seems to have a weird bug. This Sprint Team Trade is responsible for it, and it’s one of Devi’s secondary specialties so she volunteers to fix it and asks Dave to pair up with her to help him learn more about it.

Later, Devi heads over to one of the Product Managers and asks if she’s free for a few minutes to look at the first item the team has finished. The Product Manager is free, so they play with it, and Devi leaves with a few minor improvements for the team to do.

Late in the day Dave is coding the second item, with the rest of Team Trade. He checks in a stable micro-change to the head of the trunk after each 10-minute TDD cycle, to integrate continuously with his team and product group. He glances over to their big visible red-green screen and sees that the CI system is passing all the tests for the entire group.

#### Overall PBR

On the fifth day, Dave and Devi join a group-wide *overall Product Backlog refinement (PBR)* workshop, with representatives from each team, the Product Owner, and the two other Product Managers. The group splits some big items, does some lightweight analysis, and estimates.

#### Team PBR

On the sixth day, Team Trade holds their team PBR workshop, which all team members attend together. Sometimes each team will hold their team PBR separately, but in this story...

From the recent Overall PBR session, Dave and Devi know that the theme of their team-level PBR session is new USA regulatory requirements, and also that two other teams frequently work in this area. Therefore, the three teams decide to hold a *multi-team* PBR workshop in the same big room, with two Product Managers and a lawyer from the Legal Department who has met recently with the regulators. The teams do rotation analysis, and some other diverge-merge workshop patterns.

#### Sprint Review

Finally, it’s the last day and time for a two-hour *Sprint Review*! There is just one overall product-level Review together. Because there are five teams and many items to inspect...

The group starts with a ‘diverging’ one-hour bazaar-style Review, with many laptops set up in the room, each showing different sets of items. The Product Owner, other Product Managers, and few sales people are inspecting different items in parallel. Some team members stay by their laptops to collect feedback, and others visit items that interest them.

After an hour, the group ‘merge’ into the second phase of the Review. First, using a laptop and projector, Paolo shows the Product Backlog spreadsheet, and marks which of the originally forecast items met ‘done’. Then he summarizes feedback about the items he was closely inspecting, and asks the other Product Managers and sales people to do likewise. Paolo displays and discusses 3 critical items with the entire group. Next, he confirms he wants to actually release the product now, to a subset of traders in a beta-test program. Finally, Paolo explains his probable direction for the next Sprint.

#### Team Retrospectives

After a break, Team Trade hold their team-level *Sprint Retrospective*. They decide that holding a multi-team Design Workshop after Sprint Planning (rather than before) was not very good. In the next Sprint they decide to hold an early Design Workshop for some strongly-related complex items, so that the teams can speculate about a common design, and identify likely shared-work opportunities. In the next overall Retrospective, they will suggest to identify and discuss strongly-related items during PBR.

#### The End

The Sprint is over. Sam invites the entire team to join Dave and him at the Belgian-beer pub down the street to celebrate Dave’s birthday.

### LeSS Story: Flow of Features & Events

> This story emphasizes the flow of *customer features* through events, versus the prior *people & teams* story.

Ariel is so looking forward to settling in for a luxurious business-class flight on Virgin Atlantic back to London, after this meeting wraps up. She beams her 1000-watt smile to the USA financial regulator, shakes hands, and catches a taxi to JFK.

After the weekend, she’s sitting with Paolo (the Product Owner and lead Product Manager) in his office, and admires the view from the Gherkin out over London. Ariel, a product manager who specializes in regulatory requirements, summarizes on some paper cards the new rule areas that are going to impact their product, and what existing clients she thinks are going to want certain requirements first. Paolo points to the five cards, and asks, “So this covers all the work, right?” Ariel smiles and says, “This is regulatory, Paolo. It’s never finished or clear.” Paolo asks, “Can you put these in the Product Backlog for me, unordered at the bottom for now?” “Sure.”

<figure>
  <img src="/img/framework/product-owner-support-sketch.jpg" alt="product-owner-support-sketch.jpg">
</figure>

A week later Paolo tells Ariel, “Soon, I want to start delivering one of the regulatory areas, for bond derivatives. In the next Sprint’s PBR workshops, I’m going to ask the teams to focus on refining those requirements. You’re the expert, so please be at overall PBR, and at whatever team PBRs they want you. That will be the 24th and 25th this month. Also, set up a wiki page with links to the new reg docs, to share with the teams.” “Sure,” says Ariel, “…and the page is already set up.”

#### Overall PBR

On the 24th Ariel walks into the big room for a half-day overall PBR workshop. Paolo is already there, along with Peter (the other product manager), and 10 team members from the five teams. Paolo kicks off, “We’ve got a large body of work around USA reg and derivs. In a couple of Sprints I want to start delivering the features because of a regulatory deadline end of fiscal year. We’ll know better after some refinement and estimation, but I wouldn’t be surprised if it involves three or more of the teams for implementation.”

The group organizes into a semi-circle of chairs around a big whiteboard, with Ariel at the board. On the left side she writes “regs for bond derivatives.” Then, in conversation with the group, she sketches a branching tree of smaller requirements, splitting, explaining, and answering questions. After 30 minutes, the original requirement has split into 16 smaller children items.

After a break, the group creates 16 cards for the new items. They pick seven of the items that Paolo and Ariel think are especially critical but also unclear (some of the requirements are clear and straightforward reports for auditors).

Using the specification-by-example technique that Sam (a ScrumMaster) taught them, the group discusses and creates one example for each of the seven critical but unclear items. After an hour and a half, the group has their examples and better shared understanding.

Following another short break, all the team members together speed-estimate the 16 new items, using planning poker and relative-size points, base-lining the points against some of the existing estimated items in the Product Backlog.

About half of the items are estimated as doable in one-third of a Sprint or less, by a team. That’s the group’s guideline for maximum size. The rest are bigger, and will need further splitting in a later PBR workshop.

Paolo looks over all 16 cards and with Ariel they remove some that are relatively low priority. Pointing to the remaining items Paolo says, “I’m gonna want those soon. Please focus on getting them ready.”

At the end of the workshop, the team members look over the items and decide that three of the five teams should focus on them: two teams that have previously worked USA bonds, and Team Trade, since upcoming European regulations are expected to be similar.

#### Multiteam PBR and Team PBR

The next day, Team Trade and the two USA teams (TooBigToFail and NotDerivative) hold full-day Team PBR workshops. They have 12 regulatory items to get ready as soon as possible. Since so many of them are related, they decide to hold a multi-team PBR workshop together in the big room. Product Managers Ariel and Peter join, but not Paolo.

The group does *rotation* work to refine the items: Each team starts refining a different item at a separate work area in the room, each with a whiteboard and projector. Ariel is with Team Trade and they start refining a regulatory report. Peter is with Team TooBigToFail, clarifying a position risk requirement. Team NotDerivative works alone.

After 30 minutes, a timer goes *ding*! Team Trade walks over to the TooBigToFail area, Team TooBigToFail walks over to NotDerivative’s area, and Team NotDerivative heads for Team Trade’s area. Ariel and Peter don’t move, and one of Team NotDerivative’s members also stays behind to explain things to the incoming team. The timer is restarted, the stay-behind people explain the current results, and then the teams carry on with refinement.

Throughout the day, as different regulatory requirements become clear—or are left with hanging questions that will have be explored later—new ones are introduced at a work area. Some of the bigger items are split into two or three new smaller ones.

Twice during the day the teams stop their analysis work, and do some estimation, which they do separately and in parallel for different items, once again all base-lining against some of items and estimates already in the Product Backlog.

#### The Next Day

The morning after the PBR workshop, Peter (who often helps Paolo with this):

* updates the Product Backlog with the new split items derived from the original one, and deletes the original
* adds links to the new wiki page of item details, created yesterday in the PBR workshop
* records the latest estimates, and records which of the items are deemed ready by the teams

Later in the day, Ariel and Peter meet with Paolo to review the Product Backlog changes, answer Paolo’s questions, and do reordering.

Paolo highlights the new and ready items for regulator audit reports and moves them near the top of the ordering; he decides he wants to get them done next Sprint because quickly getting reports to the auditors takes a lot of pressure off. A couple of items he now realizes are much less important than he and Ariel thought, and he moves them quite low—it could be months before he returns to them.

#### Sprint Planning One

Paolo lays out 22 ordered cards on a table, and says, “Here’s my offer for this Sprint. In addition to many Brazilian market features, some of the items are for new auditor reports for USA bond derivatives.”

## LeSS Huge

### Requirement Areas

With 1000 or even just 100 people on one product, divide-and-conquer is unavoidable. Traditional large-scale development divides into:

* single-function groups (analysis group, test group, ...)
* architectural-component groups (UI-layer group, server-side group, data-access component group, ...)

This organization yields slow inflexible development with (1) high levels of waste (inventory, work-in-progress, handoff, information scatter, ...), (2) long-delayed ROI, (3) complex planning and coordination, (4) more overhead management, and (5) weak feedback and learning. And it is organized ‘inward’ around single-skills and architecture, rather than ‘outward’ around customer value.

But in the **LeSS Huge** framework, when above ‘8’ teams, you don’t divide by function or architecture; you divide around *major areas of customer concerns* called **requirement areas**. This reflects the *customer-centric* LeSS principle.

For example, in one *Securities* product (to trade and manage securities), some major areas of customer requirements—requirement areas—are:

* trade processing (from trade capture to settlement)
* asset servicing (e.g. handling a stock split, dividends)
* new market onboarding (e.g. Brazil)

Conceptually in the one Product Backlog, a “requirement area” attribute is added, and each item is classified into one and only one area:

| Order    | Item   | Requirement Area      | ...  |
|:---------------------:|:------------------------:|
| 1        | B      | market onboarding     |      |
| 2        | C      | trade processing      |      |
| 3        | D      | asset servicing       |      |
| 4        | F      | market onboarding     |      |
| ...      |
{: .grid_table_with_header}

Then people can focus on one **Area Product Backlog** (conceptually, a view onto one Product Backlog), such as the *market onboarding* area:

| Order    | Item   | Requirement Area      | ...  |
|:---------------------:|:------------------------:|
| 1        | B      | market onboarding     |      |
| 4        | F      | market onboarding     |      |
{: .grid_table_with_header}

### Area Product Owners and Teams

In LeSS Huge one new role is introduced. Each requirement area has an **Area Product Owner** that specializes in one requirement area and focuses on their Area Product Backlog. And, *several*—never just one—feature teams serve that Area Product Owner and likewise specialize in that requirement area.

So, for example, the *Securities* product has:

* one overall Product Owner and two (one per area) Area Product Owners, each supported by other Product Managers
* the (largest) *trade processing* requirement area has six teams
* and four teams in each other requirement area

Does a requirement area always have the same fixed set of teams? No. Slowly over time, as an area changes in importance, teams join or depart—mostly likely from or to another existing area.

### LeSS Huge Framework Elements

In brief, in LeSS Huge each requirement area works as a (smaller framework) LeSS implementation, each working in parallel in one overall Sprint. Variations reflecting transitional periods in gigantic groups are discussed in the *Adoption and Organize by Customer Value* chapters.

**Roles**—Same as LeSS, except: two or more **Area Product Owners**, and ‘four’ to ‘eight’ Teams in *each requirement area*. The *one* Product Owner (who focuses on overall product optimization) and the several Area Product Owners form the **Product Owner Team**. There are usually other supporting product managers in very large product groups.

A requirement area normally has at least four teams. Exceptions?

* An early transitional situation when the group is incrementally growing a new area that is fully expected to ultimate have four or more teams. Then, start small and simple with one team.
* When re-balancing teams from an area with a decreasing demand to one with an increasing demand; an area could go from four to three teams. Ultimately, merge two reduced small areas back into a new larger area.

Why at least ‘four’ teams? What’s the problem with small areas? Many tiny areas reduce visibility into overall Product Backlog priorities, increase coordination complexity, and create teams that are too narrowly specialized that lack the flexibility (agility) to take on the emerging highest-value items.

**Artifacts**—Same as LeSS, except: a requirement area column in the one Product Backlog, and consequently an **Area Product Backlog** view for each requirement area.

**Events**—There is still only one common Sprint for the product; it includes all the teams and ends in a common potentially shippable product increment. From the viewpoint of one team working in one area, LeSS Huge looks like LeSS regarding events. Other event details are illustrated in the upcoming story.

As with LeSS, there are **rules** and **guides** for LeSS Huge, which are introduced in the following story, and fleshed out in upcoming chapters.

### LeSS Huge Story

Peter hears a new voice in the hallway, and bounds out of his office to warmly welcome Ariel to her new job. As a mid-level Operations manager in the *Securities* division of the large trading company, and overall Product Owner for their internal Securities system, he’s also responsible for finding and retaining talent for his Product Owner Team. And he thinks Ariel is a fantastic find as her expertise is exactly what is required for dealing with some new huge requirements.

During the recent job interview—when Ariel was a product manager specializing in regulatory issues at a company that made a system for trading bonds—Peter had laid out the situation. “Ariel, after the last crash, the regulators are coming down hard and they require us to be compliant with Dodd-Frank. Right now, we don’t know what it exactly means or how it will impact our system. You got incredible knowledge of this space, and a great professional network with the regulators. I would love it if you would join our group and help us figure out how to deal with this.”

#### A Big Surprise

A few days later...

Peter welcomes Ariel, Rob, and Krishna into his office. Rob is Area Product Owner for market onboarding, and Krishna is a ScrumMaster from the trade processing area.

Peter says, “As you know, Dodd-Frank is coming, and it’s huge. What you don’t know is that this morning the regulators called us and they want us to take action now. I’d been working under the assumption we could start next year. So we’re going to have to adapt, big time.”

“I don’t think anyone is clear what it means in detail—even the regulators. And we don’t know how it will impact our system and how much work this is going to take, other than, a lot! But now Ariel’s joined us and she has a better understanding of this than anyone, although she’s totally new to our systems. So, how can we help her start tackling this mountain of work?”

Rob, Krishna and Peter discuss different approaches. Rob asks, “You guys know about the Dyslexic Zombies, right?” Krishna and Peter nod. Everyone knows about them—and it isn’t just their name. The Dyslexic Zombies have probably the broadest experience of all the teams. They’ve been around for years and they were a true pain in the ass when they adopted LeSS. The team contained two former members of their now-abandoned architecture group and a couple of people who had been working on the system for over fifteen years. Those four’s resistance to the LeSS adoption was legendary as they were afraid they’d lose their “system perspective.” To their surprise, the opposite happened! Because of their deep knowledge they continuously get tough items to develop, they regularly participate as expert-teachers in current-architecture-learning workshops with newcomers, and Tom—one of the former PowerPoint architects—is now leading the architecture CoP. When fed enough beer, he’ll admit that working closer with code and tests has actually increased his real understanding of the system.

Rob continues, “If any team can quickly help Ariel get a better understanding of the size and impact of Dodd-Frank, it’ll be the Zombies. And they led the work on Sarbanes-Oxley a few years ago. Tomorrow is their refinement meeting. They are just about wrapped up on a new feature. Why don’t we re-direct the meeting to include them in a discussion on Dodd-Frank, and soon after, get them to focus full-time on it? Ariel, are you available?”

Ariel nods and they agree to meet the next day with the Zombies.

<figure>
  <img src="/img/framework/zombies.png" alt="zombies.png">
</figure>

#### Refining with Zombies

Next day at the refinement meeting with the Zombies, Ariel explains the situation, “You’ve probably all heard about Dodd-Frank. But here’s the surprise: We’ve just been told by the regulators that they want to us to take action ‘now’ and demonstrate significant compliance by the end of the year. Otherwise they might restrict our trading.”

The Zombies are visibly surprised. They had heard rumors but didn’t expected such a rush! Tom says, “OK Ariel, give us a quick summary of what this means. And how is it different from Sarbanes-Oxley?”

Ariel picks up a pen and starts sketching on a whiteboard. After about 45 minutes, she is finished with the overview and the Zombies looked a little stunned. “End of the year, they said?” says Tom. “If the whole group started today, it wouldn’t get finished. This is huge!”

<figure>
  <img src="/img/framework/sharing-sketch.jpg" alt="sharing-sketch.jpg">
</figure>

He takes a pen and at the whiteboard starts a rough sketch of their system, talking with the other Zombies about the impact it might have. He says, “Ariel, let’s also use this as a chance to help you understand the system better. Ask away.” Ariel says, “Can you hold on for a sec? Let me start a video recording to help me remember this.”

Simon, a grizzled veteran in the team, says, “We’d better start on some real development soon and learn more as we go because otherwise we’ll end up analyzing forever. I’ve seen this story before.”

Alexandru, their ScrumMaster, says, “Reminds me… Tom DeMarco once said that the reason for every failed project is that it started too late.” Everyone laughs. He continues, “Good, let’s spend the rest of the session to find one clear area and ‘take a bite’ out of Dodd-Frank. We’ll put the big and smaller parts into our Area Product Backlog.”

Later, Ariel tells Peter what they did in the refinement meeting and their recommendation for where to start. She knows that Peter and the rest of the Product Owner Team will decide the next step.

#### Creating a New Requirement Area

The next day, Ariel, Peter, and rest of the Product Owner Team meet. Ariel shares a summary of the scope as she understands it now. Peter sighs and says, “This is even bigger than I expected. And the regulators have the power to shut us down now. I don’t think i need to explain the business case for keeping them happy enough so we can keep trading.”

“OK!” he says suddenly and decisively. “We’ll need a new area for this. Ariel, I know you are new to us, but do you think you would be able to handle the Area Product Owner responsibility for this?” Ariel nods.

Peter continues, “Rob do you think the Zombies could work on this? And we’ll need them to learn more Dodd-Frank and figure out the impact on our system before we can add more teams to this.” Rob says, “I don’t think we’ve got any choice.”

Peter says, “OK Ariel, so now we’ve got a few items in Rob’s Area Backlog, the one huge item I think you called “remainder of Dodd-Frank” and the smaller items which the team and you split off of it. I want you to get Rob to show you how to set up a new area in the Product Backlog and move the items over to it.” Ariel smiles and says, “Alexandru from the Zombies calls the smaller ones our first bite.”

Peter smiles back and says, “The next Sprint is in three days. Let’s move the Zombies into your area and get started on this monster. Probably in a couple of Sprints we’ll move another team to your new area. Ladies and gentlemen, everyone please think about which team would be suitable? Now, let’s end this meeting and do something!”

#### Sprint Planning in the New Requirement Area

Each of the requirement areas holds their own Sprint Planning meetings, all more or less in parallel. In Ariel’s new area, she starts her Sprint Planning by introducing two unfamiliar faces to the Zombies. She says, “Gillian and Zak have been in contact with the regulators regularly and will help us flesh this thing out. They’ve agreed to help us now in Planning, during our PBR sessions, and as much as they can spare daily during upcoming Sprints.”

She continues, “Here’s my plan of attack for the next two Sprints. First, together we need to learn more about Dodd-Frank, and also split it into some major and manageable pieces so we can start to clear the fog and get a better sense of priorities.”

“Second, we’re going to implement the smaller bite we’ve already taken, starting this Sprint. That’ll give us better information about the real work. And we’ll have some concrete visible progress.”

“Third, we’re going to prepare for more teams to join our area.”

Tom takes over from Ariel and shares with his team, “Let me explain that, cuz I represented our team in the POT meeting. To start with, it’s just us. We’re gonna take the lead on early implementation, and getting the big picture of the item, and understanding the overall impact on our architecture.”

Simon interrupts, “Like a tiger team working on a new product?” “Yes, like that,” says Tom. “Think of Dodd-Frank support as a new product that needs to be integrated into the rest of the product. But we’re in a hurry, so in a few Sprints another team will join us and shortly after, probably two more teams. We keep developing too, but we’ll be the leading team which means we’ll need to bring the other teams up to speed and make sure we keep the overall product in mind.”

Simon says, “It’s starting to sound to me like we’re gonna become the architecture and project management team.” Tom laughs, “No. I’m done with that. We’re still a normal team, but besides development we focus on mentoring and teaching the new teams and keep an eye on the overall system integrity. But let’s be clear: team coordination and management is still the responsibility of each team.”

#### The First Sprint in the New Requirement Area

The first Sprint is unusual in that they spend almost half of their time in refinement together with Gillian and Zak, and only half in developing.

But the discussion and the learning from coding pays off. Slowly but surely they start to split Dodd-Frank apart—at least the parts that any of them can understand. It seems no one knows all that it means.

While implementing the small item they had bitten off first, much of the time is together at whiteboards to discuss the overall design implications on the system. They move frequently back and forth between the code and the wall.

#### Sprint Review in the New Requirement Area

The overall Securities product group works together in one Sprint, with one final shippable product increment. But each of the requirement areas holds their own Sprint Review, all more or less in parallel.

In Ariel’s area, during their Review, she inspects and uses the one ‘done’ item that the Zombies have managed to complete and integrate into the overall product. They had original forecast two items, but Ariel is impressed that they even got one done, given how fast this new work was thrown at them.

#### The Second Sprint

In the second Sprint they’re able to make slightly better progress on items, though they once again spend almost half of their time in refinement together with Gillian and Zak.

In the middle of the Sprint they hold a multi-team PBR session with the second team that is soon planned to join the area, teaching them about Dodd-Frank. And they hold a multi-team Design Workshop to start to introduce the incoming team to what they’ve changed so far, and their speculation for the upcoming items.

The Zombies know how big the work is and very much look forward to getting more help.

#### Product Owner Team Meeting

A few Sprints later...

It’s time once more for the per-Sprint Product Owner Team meeting. They use it to align and coordinate between the different Area Product Owners, and for Peter to provide overall guidance.

The Area Product Owners each share in turn their situation and upcoming goals. When it’s her turn, Ariel says, “To none of our surprise, the progress is little and the surprises are big. But the velocity is starting to pick up as the fog clears and the teams and I are getting our heads around the work. Gillian and Zak have been tremendous.”

Ravi, the asset servicing Area Product Owner, comments on some close item relationships he now sees between their areas. Ariel makes a note in the item’s wiki page, and agrees to meet with Ravi and some team representatives later.

Peter says, “Ariel, about our upcoming Sprint. What’s your goals?” …

####  Adding a Third Team

A few Sprints later...

At the Product Owner Team coordination meeting, Peter says, “As you know, Ariel’s area still only has two teams. I know that Ravi would like to keep his four teams in asset servicing, but Dodd-Frank is just too important to me this year. So we’re going to move one team from Ravi’s area into Ariel’s. Ravi, please ask for a volunteer team from your group and let me and Ariel know.”

## Multisite

### Dispersed versus Multisite Teams

If the entire tiny development group is eight people in three countries, there is a single *dispersed* ‘team’. (We don’t recommend that; we’re defining terms.) But when your single product group is 50 or 500 people, dispersed teams are not necessary; each team can easily be co-located literally at the same table. However, some teams may be in different sites, so that the product group has *multisite teams*.

### LeSS Huge Story when Multisite

Ariel is the Area Product Owner for a new requirement area in a Securities trading system. The new area started with just one team, for focus and simplicity. But Peter, the overall Product Owner, predicted from the start that it would eventually need at least four teams, given how big the work was. After a few Sprints, a second team was added; the original team, the Dyslexic Zombies, acted as mentors for the second.

A few Sprints later, Ariel’s area gets a third team. But unlike her first two teams that are based in London with her, her third new team, *HouseDraculesti*, is based in Cluj Romania, at a major development site for the company.

Peter knows that multisite teams are a new situation for Ariel, and he invites her to a meeting. He says, “Hi Ariel. I wanted to share some multisite advice. First, get your ScrumMaster to talk with Sita and also ask her to coach some of your events. She’s a ScrumMaster in the asset servicing area. They’ve been multisite for almost two years, and she’ll have a lot of suggestions.”

“Second, plan for you and the entire Zombies team to spend a Sprint in Cluj as soon as possible. Work really close with them, all in one room. The Cluj team could come here to London, but you want to send a strong signal that they are important, in their site. Try to avoid making them feel that London is more important than Cluj for your group. And you’ll want to visit there regularly. Next, ...”

#### Multisite Sprint Planning Part One

Several Sprints later...

Ariel walks into the room. There’s a computer projector attached to a Mac laptop, displaying via Google Hangouts video a room in Cluj. The two representatives from the team at that site are sitting and waiting. All the team representatives have tablets or laptops with them.

Ariel says, “Welcome to Sprint Planning. Let’s get started. My offer of items this Sprint are highlighted in the Google Spreadsheet. Can you all see it? Good. Please enter your team names beside the items you want.”

That done, the group enters a Q&A phase to wrap up lingering questions about the items—there’s always more questions. The London representatives tape up some flip chart papers and start writing questions. The Cluj representatives enter their questions in separate sheets of a Google Spreadsheet. Ariel spends some time at the different paper flip charts, discussing answers and sketching on the paper. And she spends some time at the spreadsheet, typing in answers for the Cluj team, while also talking with them face to face via the Hangouts video session.

After about 30 minutes all the questions have been resolved, and Ariel asks everyone to sit down. She says, “Now that we’ve spent some time apart, let’s converge. Is there anything you’ve learned that you want to share with the other team reps, to help our alignment or coordination?”

Fifteen minutes later Ariel says, “Done! I’ll hang out here in the corner while you have your coordination discussion and prepare for Part Two.”

#### Multisite Overall PBR

People are coming in to the workshop room in London. Two computer projectors are set up. One shows a Hangouts video session of the workshop room in Cluj. The other displays a browser on Ariel’s computer.

Ariel says, “Let’s get started. I want to focus on splitting some of our current split items even smaller.”

Using a mind-mapping browser-based graphics tool, she starts to create some branches, while discussing with the group.

Afterwards, they use a Google Spreadsheet to discuss a single example for each of the new split items, so that the representatives at both sites get a lightweight but concrete understanding of the details.

Later, the group does estimation of the new items, using especially big “planning poker” cards that can be easily seen via Hangouts and the cameras, as displayed on the computer projectors.

#### Multisite Interactions and Tools

As the above story sketch shows, “face to face” interaction is still possible in a multisite team context—and it’s vital! Modern and free collaboration tools can be used similarly in a Sprint Review, overall Retrospective, and so forth.

## Onwards

**Whole product focus**—These stories give a feel for applying LeSS in the context of a Sprint and its events. Not emphasized but central to all the stories is the LeSS principle of whole product focus—all the teams together creating one common potentially shippable product increment delivered at the end of one common Sprint. That’s really important.

**Organizations and fake Scrum**—Also important is the organizational design that enables all this.

> Scaled Scrum is not a special scaled framework
> that happens to include “Scrum for each team”

> Scaled Scrum is Scrum scaled.

It’s easy to create “fake Large-Scale Scrum” groups that are going through the apparent motions of Scrum, but when you scratch below the surface you’ll see the situation is largely the same as the old status quo, but with new Scrum or agile terms pasted on top. So large groups end up with:

* the “analysis Scrum team” writing the user stories
* the “UX Scrum team” delivering the wireframe UX stories
* the “architecture Scrum team” making up PowerPoint stories
* many “programming Scrum teams” each with their own team-level so-called “Product Backlog”
* the “testing Scrum team”

...all working towards the command to “deliver the project by the end date; let us know when it’s all done” and directed by a project manager fake ScrumMaster.

That just sucks.

So, since real Large-Scale Scrum starts with *changing the organization rather than changing Scrum*, the next few chapters focus on LeSS organizational design and its adoption.

