# Incident Report: Remove faction duplicate (PR #334)

**Project:** cMaNGOS  
**Affected Author:** Phatcat  
**Original Work:** [Pull Request #334](https://github.com/cmangos/mangos-classic/pull/334) (1 commit, Mar 2018)  
**Infringing Commit:** [Commit b72c094](https://github.com/cmangos/mangos-classic/commit/b72c094) (Dec 2018)

## Overview
This entry documents the "Stall and Steal" tactic. In March 2018, a contributor proposed a structural database refactor to remove redundant faction columns (`FactionHorde`/`FactionAlliance`) based on reverse-engineering sniffs. Despite immediate approval from other members, the PR was ignored for nine months, only to be closed by a maintainer who implemented the exact same structural changes under their own name.

## Technical Evidence
* **Logic Duplication:** The infringing commit `b72c094` performs the exact schema migration proposed in PR #334: dropping `FactionHorde` and renaming `FactionAlliance` to `Faction`.
* **SQL Parity:** As seen in the comparison of `z2719_01_mangos_creature_template_fixup.sql` (Contributor) and `z2729_01_mangos_creature_template_faction_removal.sql` (Maintainer), the SQL commands are functionally identical, utilizing the same `ALTER TABLE` logic to achieve the refactor.
* **Metadata Removal:** The contributor's commit history, which included the research and justification for the change, was discarded. The maintainer credited themselves for the architectural shift.

## Statements of Intent (Direct Quotes)

### 1. Maintainer Approval and "Political" Avoidance (killerwife - Mar 5, 2018)
> "FactionAlliance/FactionHorde needs to be nuked... My approval, but for political reasons I am staying away from further discussion."

* **Analysis:** The maintainer explicitly approved the logic on day one but refused to merge it, citing "political reasons." This established a period of artificial stagnation despite technical consensus.

### 2. Strategic Silence and Closing (Dec 10, 2018)
> "Closed by b72c094"

* **Analysis:** After 280 days of inactivity, the maintainer closed the contributor's PR not by merging it, but by referencing their own commit. This is a classic example of "Attribution Laundering," where a maintainer waits for a PR to lose visibility before re-implementing the work to claim authorship.

## Compliance Conflict
Under **GPLv2 Sections 1 and 2**, the legal right to distribute a derivative work requires a clear record of authorship. By intentionally stalling a contributor’s approved refactor for nine months and then re-implementing it to bypass the Git ledger, project leadership has falsified the record of who originated the architectural change. This practice treats community research and development as "public domain" material for maintainers to harvest.
