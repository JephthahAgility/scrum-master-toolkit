Scrum Master Jira Dashboard Example

Agile Delivery Dashboard

This dashboard provides a practical example of how a Scrum Master can use Jira metrics to monitor Sprint progress, understand workflow, identify impediments, and support continuous improvement.

«Note: The data in this dashboard is illustrative and does not represent confidential company information.»

---

1. Sprint Overview

Sprint: Sprint 24
Sprint Duration: 10 working days
Team: Digital Product Team
Sprint Goal: Deliver and validate prioritized customer-facing features.

Metric| Current Value
Planned Story Points| 76
Completed Story Points| 68
Remaining Story Points| 8
Stories Completed| 14
Stories Remaining| 2
Sprint Progress| 89%
Days Remaining| 1

Scrum Master Observation

The team has completed 68 of 76 planned Story Points. The remaining work should be reviewed with the team to understand whether it can realistically be completed within the Sprint or whether adjustments are required.

---

2. Velocity

Five-Sprint Velocity Trend

Sprint| Completed Story Points
Sprint 20| 72
Sprint 21| 75
Sprint 22| 78
Sprint 23| 74
Sprint 24| 68

Average Velocity

(72 + 75 + 78 + 74 + 68) ÷ 5 = 73.4 Story Points

Scrum Master Observation

The team's five-Sprint average velocity is 73.4 Story Points.

The lower result in Sprint 24 should be discussed in context rather than treated as a performance problem. Possible discussion areas include:

- Team capacity
- Production support
- Dependencies
- Unplanned work
- Scope changes
- Technical complexity

---

3. Cycle Time

Current Cycle Time

Average Cycle Time: 6 days 3 hours

Work Item| Cycle Time
Story A| 4 days
Story B| 5 days
Story C| 7 days
Story D| 8 days
Story E| 6 days

Scrum Master Observation

The Scrum Master can look for work items that take significantly longer than the team's normal delivery pattern.

Questions to explore:

- Was the item blocked?
- Was the story too large?
- Was testing delayed?
- Was there a dependency?
- Were requirements unclear?

---

4. Lead Time

Current Lead Time

Average Lead Time: 6 weeks 1 day

Lead Time measures the elapsed time from the team's defined request/intake point until completion.

Scrum Master Observation

A relatively long Lead Time compared with Cycle Time can indicate that work is spending significant time waiting before active development begins.

The team can investigate:

- Backlog waiting time
- Prioritization delays
- Dependency management
- Approval processes
- Capacity constraints

---

5. Work in Progress (WIP)

Current WIP

Workflow Stage| Items
To Do| 8
In Development| 5
Code Review| 2
QA / Testing| 3
Blocked| 2
Done| 14

Active WIP

5 Development + 2 Code Review + 3 QA + 2 Blocked = 12 active items

Scrum Master Observation

The team should consider whether the amount of active work is creating bottlenecks or context switching.

Potential actions:

- Finish existing work before starting new work.
- Swarm on blocked items.
- Identify QA constraints.
- Review WIP limits.
- Investigate items sitting in the same workflow stage for extended periods.

---

6. Aging Work Items

Current Aging Items

Issue| Status| Age| Potential Discussion
STORY-241| Development| 8 days| Check for blocker
STORY-245| QA| 7 days| Investigate testing delay
STORY-249| Code Review| 5 days| Review PR status

Scrum Master Observation

Aging work items are signals for conversation.

The Scrum Master can ask:

«"What is preventing this item from moving forward?"»

Rather than:

«"Why hasn't this person finished the work?"»

This keeps the focus on the system, workflow, and impediments.

---

7. Sprint Progress

Sprint Burndown Snapshot

Day| Remaining Story Points
Day 1| 76
Day 2| 72
Day 3| 69
Day 4| 61
Day 5| 55
Day 6| 48
Day 7| 37
Day 8| 25
Day 9| 16
Day 10| 8

Scrum Master Observation

The remaining work is decreasing throughout the Sprint.

The Scrum Master should use the Sprint progress information to facilitate conversations about:

- Sprint Goal progress
- Remaining work
- Blockers
- Dependencies
- Scope changes
- Risks to completing the Sprint Goal

---

8. Jira Reports & Dashboard Gadgets

A practical Scrum Master Jira dashboard could include:

Jira Report / Gadget| Purpose
Sprint Burndown| Monitor remaining Sprint work
Velocity Chart| Understand delivery patterns
Control Chart| Review Cycle Time
Cumulative Flow Diagram| Identify workflow bottlenecks
Filter Results| Display blocked or aging items
Created vs Resolved| Understand incoming vs completed work
Sprint Health| Review Sprint progress
Custom Charts| Present selected team metrics

---

9. Example Jira Filters

Blocked Work

project = DIGITAL
AND status = Blocked
ORDER BY updated ASC

In-Progress Work

project = DIGITAL
AND statusCategory = "In Progress"
ORDER BY updated ASC

Aging Work

project = DIGITAL
AND statusCategory = "In Progress"
AND updated <= -5d
ORDER BY updated ASC

Current Sprint

project = DIGITAL
AND sprint in openSprints()
ORDER BY status ASC

«JQL should be adapted to the team's actual Jira project, workflow, field names, and status configuration.»

---

10. Scrum Master Daily Dashboard Review

A Scrum Master could review the dashboard each day by asking:

Sprint Goal

- Are we progressing toward the Sprint Goal?

Blockers

- What is blocked?
- How long has it been blocked?
- Who or what can help remove the impediment?

WIP

- Are we starting more work than we are finishing?

Aging

- Which items have been in progress longer than expected?

Flow

- Where is work accumulating?

Quality

- Are defects or rework affecting Sprint progress?

Delivery

- Are we seeing significant changes in Cycle Time or Throughput?

---

11. Continuous Improvement Actions

Based on the dashboard, the Scrum Master may facilitate improvement actions such as:

Observation: QA items are aging.

Possible discussion: Is there a testing capacity constraint?

Improvement experiment: Swarm on older QA items before starting additional development work.

---

Observation: Cycle Time is increasing.

Possible discussion: Are stories becoming too large or are dependencies increasing?

Improvement experiment: Review story slicing during Backlog Refinement.

---

Observation: WIP is consistently high.

Possible discussion: Are team members starting too many items?

Improvement experiment: Introduce or adjust WIP limits and encourage finishing before starting.

---

12. Key Principle

Jira metrics should help the team inspect, learn, and adapt.

The Scrum Master's role is not to use metrics to rank individual team members.

Instead, metrics can provide visibility into the team's workflow and help the team identify opportunities for continuous improvement.

---

Dashboard Summary

Area| Current Example
Sprint Progress| 89%
Planned Story Points| 76
Completed Story Points| 68
5-Sprint Average Velocity| 73.4 SP
Average Cycle Time| 6 days 3 hours
Average Lead Time| 6 weeks 1 day
Active WIP| 12 items
Aging Items| 3 highlighted
Remaining Work| 8 SP

Portfolio Note:
This dashboard is a simulated example created to demonstrate Scrum Master knowledge of Jira, Agile metrics, workflow management, and continuous improvement. 
