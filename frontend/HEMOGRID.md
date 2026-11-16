<div align="center">

# HemoGrid

### The closest blood bank is not always the right one.

**🏆 Overall First Place · Terumo BCT Africa Hackathon 2026**

**Emergency blood request and dispatch · Team Relay · One project, two codebases**

**[Launch live demo](https://hemogrid-eight.vercel.app/login)** · **[Watch demo video](https://www.tella.tv/video/hemogrid-emergency-blood-dispatch-dt1odmiq)** · **[Pitch slides](https://docs.google.com/presentation/d/1E3NaYlyrvygwXysVymFKq4qBNCi22wb428WnZNdBTfE/edit)**

**[Frontend source](https://github.com/Grolds-Code/hemo-grid-frontend)** · **[Backend and evaluation source](https://github.com/Grolds-Code/hemo-grid-backend)** · **[Original Team Relay project](https://github.com/Team-Relay)**

**No registration required for the synthetic demonstration.** Select Hospital, Blood bank or Platform admin; the demo credentials are prefilled.

<a href="https://hemogrid-eight.vercel.app/login">
  <img src="https://raw.githubusercontent.com/Grolds-Code/hemo-grid-frontend/main/public/judges/mission-control.png" width="920" alt="HemoGrid coordinator workspace with critical requests and dispatch decision evidence" />
</a>

<sub>Screenshot of the hosted synthetic demonstration, not live clinical data.</sub>

</div>

---

## One project. Two connected codebases.

HemoGrid is an emergency blood-dispatch prototype developed by **Team Relay**. It helps hospital staff identify suppliers using recorded inventory, configured blood-group and quarantine checks, and estimated routes. A coordinator can compare shared-stock plans across competing urgent requests, while blood-bank staff retain control of acceptance, reservation and fulfilment.

| Repository | What it contains |
| --- | --- |
| **[Frontend · Grolds-Code/hemo-grid-frontend](https://github.com/Grolds-Code/hemo-grid-frontend)** | Next.js/React user experience, hospital, blood-bank and coordinator workspaces, API integration, browser tests and demonstration guide |
| **[Backend · Grolds-Code/hemo-grid-backend](https://github.com/Grolds-Code/hemo-grid-backend)** | Spring Boot API, PostgreSQL state transitions, stock reservations, quarantine safeguards, advisory joint planner, reproducible evaluation and tests |

These are **personal forks of Team Relay's original repositories**, preserved with their Git histories. Together, they form **one HemoGrid project**, not two separate products.

## What the prototype demonstrates

- **Hospital officer:** create a synthetic request, examine eligible suppliers and select one for staff approval.
- **Network coordinator:** compare allocation proposals across **2–5** urgent red-cell requests sharing limited available stock; the plan is a preview and does not reserve units.
- **Blood-bank officer:** accept or decline a request, revalidate stock, reserve units, and move an accepted request through preparation, transit and delivery.
- **Safeguards:** role-based authorization, transactional inventory reservations, quarantined or unavailable stock handling, and tested fallback when the joint planner fails.

A hosted synthetic workflow completed **create → select → accept/reserve → prepare → in transit → delivered**, with inventory reconciled after delivery. [Review the original hosted test record](https://github.com/Team-Relay/hemo-grid-frontend/actions/runs/42952475072).

## Evaluation evidence, with limits

In a controlled evaluation of **1,072 synthetic red-cell requests**, a distance-only nearest-site choice failed at least one configured eligibility check for **749** requests. Both HemoGrid and a nearest-eligible baseline produced eligible full-quantity proposals for **1,044 of 1,072** requests. Under one five-request scarcity scenario, HemoGrid completed **150 of 214** batches versus **146 of 214** for the sequential nearest-eligible baseline.

These are **synthetic software evaluations**, not clinical accuracy, measured delivery times, patient outcomes or deployment validation. The planner is deterministic and advisory. Actual medical compatibility, crossmatching and dispatch decisions require authorized professionals and independent validation.

[Read the full evaluation methods, baselines and limitations](https://github.com/Grolds-Code/hemo-grid-backend#ai-and-data).

## Engineering and team credit

HemoGrid was developed collaboratively by **Team Relay**:

| Contributor | Contributions |
| --- | --- |
| **Grold Otieno** | Dispatch planning and integration, inventory and concurrency safeguards, reproducible evaluation, automated testing and frontend workflows |
| **Dennis Ikechukwu Okwuchukwu** | Project concept and team leadership, full-stack and systems engineering, product implementation and final presentation |
| **Mubarak Zubair** | Product management and clinical-data analysis |

This is a **personal project showcase**, not a claim of exclusive ownership. Original repositories: [frontend](https://github.com/Team-Relay/hemo-grid-frontend) and [backend](https://github.com/Team-Relay/hemo-grid-backend).

## Explore the project

**[Open the live demo](https://hemogrid-eight.vercel.app/login)** · **[Start with the judging guide](https://github.com/Grolds-Code/hemo-grid-frontend/blob/main/docs/JUDGE_START_HERE.md)** · **[Read the frontend README](https://github.com/Grolds-Code/hemo-grid-frontend#readme)** · **[Read the backend README](https://github.com/Grolds-Code/hemo-grid-backend#readme)**

<sub>Prototype based on synthetic Kenyan network data. Not for clinical use. No live patient data, certified interoperability, observed deliveries or clinical outcome claims.</sub>
