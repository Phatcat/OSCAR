# Incident Report: Implementation of time-based one-time password & fixed PIN authentication (PR #193)

**Project:** cMaNGOS  
**Affected Authors:** Chaosvex / TrinityCore  
**Original Work:** [Pull Request #193](https://github.com/cmangos/mangos-classic/pull/193) (11 commits, Sep 2016)  
**Related Work:** [Pull Request #191](https://github.com/cmangos/mangos-classic/pull/191) (Sep, 2016) / [TrinityCore Commit ba22bae](https://github.com/TrinityCore/TrinityCore/commit/ba22baebbd1394cc69366d7a19d879da43885430) (Aug, 2013)  
**Infringing Commit:** [Commit 4b10465](https://github.com/cmangos/mangos-classic/commit/4b10465) (Nov, 2017)

## Overview
This entry documents the process of functional stagnation and subsequent reintegration. In 2016, chaosvex provided a full implementation of Two-Factor Authentication (TOTP/PIN). Project leadership publicly questioned the utility of the feature to justify withholding the merge of the PR, only for the same logic to be re-injected into the core, albeit in an admittedly worse form, under maintainer authorship.

## Technical Evidence
* **Logic Duplication:** Commit `4b10465` utilizes the exact architectural structure changes (e.g., core-handling logic), database schema extensions, and the RFC 6238 TOTP implementation.
* **Metadata Removal:** The 11 original commits, containing the iterative development, bug fixes, and review history, were discarded. The feature was merged as a "clean" maintainer commit, erasing the names of the developers who reverse-engineered the system.
* **Strategic Delays:** The work remained in a pending state for over 18 months. During this period of documented stagnation, the logic was manually ported to the master branch under maintainer metadata. The original PR was eventually closed by the author in 2018 after the functional duplication in the core rendered the contribution redundant.

## Statements of Intent (Direct Quotes from the implementation on an adjacent repo before backporting;)

https://github.com/cmangos/mangos-wotlk/commit/12ce14f2c399741d67e5f68425032a21240b708f

### 1. Admission of "Mistake" and Attribution Failure (cyberium)
> "For me its a mistake and its on discussion to avoid same error in future. Btw in this code there is only part of Chaosvex code. So proper commit order had to be, merge his PR (or crypt part of it) then add Laizerox code (authentificator)."

* **Analysis:** Leadership admitted that the proper legal and technical path was to merge the original PR. By choosing not to do so, they knowingly distributed a derivative work without original authorship metadata.

### 2. Contradictory Attribution Claims (cyberium)
> "Yes after reviewing those code its easy to see that the code is not from Chaosvex PR (his code is better than this commit btw). Only 2 included files are the same... This code come from trinity..."

* **Analysis:** After initially admitting the code belonged to Chaosvex, leadership pivoted to claiming the work was sourced from another project (TrinityCore, from which the proper authors weren't attributed either) to avoid the attribution requirement. This contradiction obscures the true provenance of the code, as neither original source (Chaosvex or TrinityCore) was credited in the resulting commit.

### 3. Hostile Silencing of Dissent (cyberium)
> "We don't care much about your opinion, you already expressed yourself a bit too much here. So try to be more constructive or we don't need anymore any of your reaction here."

* **Analysis:** When confronted with the evidence of plagiarism, leadership utilized their administrative power to threaten a ban ("be my guest") against the contributor pointing out the license violation and attribution removal. This creates a culture where pointing out non-compliance is treated as a bannable offense.

## Compliance Conflict
Under **GPLv2 Sections 1 and 2**, the legal right to distribute a derivative work requires a clear record of authorship. By dismissing a contributor's work, acknowledging it was used, then pivoting to claim it came from elsewhere to avoid credit, the project has committed a willful breach of the license. The use of administrative threats to silence reports of this non-compliance further demonstrates a systematic bypass of the attribution requirements.
