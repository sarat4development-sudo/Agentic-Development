# Agentic Development — AWS cloud engineering refresh

Hands-on curriculum for someone returning to cloud engineering: **real AWS projects** plus **agentic workflows** (Cursor and similar tools) for infrastructure and delivery.

## Approach

1. **Learn by shipping** — Each week centers on a concrete outcome (running app, real DNS, real cluster), not a long reading list. Theory shows up when it unblocks the build.
2. **Agents draft; you decide** — Use Cursor (chat or agent mode) to generate Terraform, Docker, and pipeline YAML. Treat output as a proposal: read diffs, run `terraform plan`, and verify in the console or CLI before anything touches shared environments.
3. **Tight scope per session** — One objective at a time (e.g. “VPC + EKS only”) keeps context small and reduces mistakes across long agent runs.
4. **Same habits as production** — No secrets in git, least-privilege IAM, remote state for Terraform when you move past solo experiments, and CI that plans or builds before apply/push.
5. **Cross-cutting skills** — The [agentic development crash course](agentic-development-crash-course.md) is the playbook for prompting, grounding, and risk — use it alongside every week.

## Reference

| Document | Purpose |
|----------|---------|
| [Agentic development crash course](agentic-development-crash-course.md) | How to work with AI agents: scope, verification, security, and day-to-day habits. |

## Curriculum

| Week | Link | Focus |
|------|------|--------|
| 1 | [week1.md](week1.md) | Scholar Path Web UI on AWS: Cursor and GitHub setup, AWS CLI, Docker, Kubernetes (e.g. EKS), load balancer, Route 53, Terraform; stretch: GitHub Actions, env config for the cluster. |
| 2 | *Coming soon* | — |
| 3 | *Coming soon* | — |

Additional weeks will be added here as markdown files at the repo root (e.g. `week2.md`, `week3.md`) following the same pattern.
