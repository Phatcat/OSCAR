# Meta Audit: Systematic Metadata Removal, Attribution Laundering, and License Instability (2016 to 2026)

**Project:** cMaNGOS (Classic/TBC/WotLK)  
**Primary Actors:** killerwife (Maintainer), cyberium (Project Leadership)  
**Subject:** Analysis of Recurring GPLv2/GPLv3 Compliance Failures

---

## Executive Summary
This document synthesizes incident reports and license audits into a single record of project governance. The evidence demonstrates that cMaNGOS leadership has moved beyond isolated error into a **Systematic Standard Operating Procedure (SOP)**. Over a ten-year period, high-value community contributions have been intentionally decoupled from original authorship metadata to centralize credit within a closed circle of maintainers. Furthermore, the project has engaged in unauthorized license versioning and expressed a documented apathy toward legal compliance, viewing the GPL as a cosmetic suggestion rather than a binding legal constraint.

## The "Stall, Steal, and Smother" Workflow
The audit of Incident Reports #193, #334, and #520 identifies a consistent three stage execution pattern utilized by the primary actors:

* **Functional Stagnation:** A contributor submits a high value Pull Request (PR). The PR is either ignored for years, publicly questioned on utility, or withheld for political reasons, despite having technical approval.
* **Metadata Extraction:** The maintainer (**killerwife**) manually re-types, ports, or re-injects the logic into a new commit or a Work-in-Progress (WIP) branch. This creates a clean history that erases the original contributor's Git ledger.
* **Administrative Shielding:** When the metadata removal is identified, project leadership (**cyberium**) provides administrative cover. Tactics include claiming a different source, citing personal copy exceptions for public branches, or using administrative power to silence dissent.

## Comparative Audit of Systematic Violations

| Incident | Primary Tactic | Maintainer Action (killerwife) | Leadership Defense (cyberium) |
| :--- | :--- | :--- | :--- |
| **PR #193 (2016)** | **Source Diversion** | Re-implemented 2FA logic under a single commit, stripping 11 original commits. | Claimed code came from TrinityCore; threatened to ban the contributor for reporting the issue. |
| **PR #334 (2018)** | **Political Stalling** | Stalled an approved SQL refactor for 9 months before re-committing identical logic. | Explicitly cited political reasons for withholding the merge of the original PR. |
| **PR #520 (2026)** | **Manual Re-typing** | Re-typed 14 commits of PetAI logic into a WIP branch under his own name. | Admitted history is repeating but claimed no distribution occurred on the public branch. |

## License Instability and Governance Apathy
Analysis of repository history between 2017 and 2019 reveals a pattern of unauthorized "License Flip-Flopping."

* **Unauthorized Downgrade:** Leadership executed a downgrade from GPLv3 back to GPLv2. Legally, code contributed under GPLv3 cannot be reverted to GPLv2 without explicit permission from every contributor during that window.
* **The Dependency Paradox:** Leadership justified the downgrade by citing third party code compatibility. However, the dependencies in question were already licensed under "GPLv2 or later," which explicitly allows those dependencies to be used within a GPLv3 project. By "downgrading" to comply with the dependency, leadership actually chose to violate the primary project license to solve a non-existent legal conflict.
* **Legal Fog:** In 2019, it was documented ([Issue #1825](https://github.com/cmangos/issues/issues/1825)) that the project's NEWS.md, README, and LICENSE files were in direct conflict, referencing non-existent files (e.g., COPYING) and stating incorrect license versions. This creates a state of Legal Fog where contributors and users cannot verify the actual terms of distribution.

### Documented Admissions of Non-Compliance
* **The "Nobody Will Sue" Defense (cyberium, 2017):** "i dont care much about license because i personally consider everyone can/are already doing what they want with an open-source software that no authors will engage any legal proceeding."
* **The "Holiday Priority" Dismissal (xfurry, 2017):** "Guys, I think there are more important topics to take care of, other than licenses (for example summer holiday)... I don't think that any of the authors will actually care if you change one open source license with another open source license (I personally don't)."

---

## Analysis of Project Governance
The recurring nature of these events involving the same maintainer and the same leadership indicates a willful bypass of **GPLv2 Sections 1 and 2**. 

* **The "History Repeating" Admission:** In 2026, leadership stated that the conflict felt like history repeating itself. While intended as a commentary on the persistence of the whistleblower, the statement functions as a de facto acknowledgment of the project's recurring friction regarding GPL compliance. It confirms that leadership is aware this specific issue has been a point of contention for a decade, yet the internal workflow has not been adjusted to prevent it.
* **The Strategic Contradiction:** In 2026, leadership attempted to minimize the removal of metadata as a non-critical issue on a WIP branch. This contradicts their 2017 admission (PR #193) where they explicitly stated that failing to merge a contributor's PR was a mistake and that the proper technical path was to preserve the original authorship. This demonstrates that the project's current non-compliance is a choice made with full prior knowledge of the legal requirements.
* **The Metadata Fallacy:** The project has actively promoted the technical error that Git metadata is not a legal record. By establishing this procedural precedent, they treat community research as raw material to be harvested rather than protected intellectual property.
* **License as Suggestion:** The combination of unauthorized license versioning and the "nobody cares" model creates a hostile environment for intellectual property. If leadership does not respect the license version itself, they cannot be expected to respect the authorship metadata requirements (GPLv2 Sections 1 & 2) that protect individual contributors.
* **Power Imbalance:** The use of Strategic Delays forces contributors into a Fix it Later trap, where they are pressured to accept the theft of their metadata simply to see their technical work finally integrated after years of stagnation.

## Conclusion
The cMaNGOS project, under the direction of **killerwife** and **cyberium**, has established a decade long record of **Attribution Laundering**. By systematically stripping the work of original Git authorship, the project has falsified the historical record of its own development. These actions constitute a willful, ongoing breach of the GPLv2 license, intended to consolidate the technical legacy of the project within its primary leadership. This environment provides the necessary cover for the systemic bypass of the attribution requirements; if leadership does not respect the license version itself, they cannot be expected to respect the authorship metadata that protects individual contributors.
