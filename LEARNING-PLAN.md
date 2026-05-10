# Focused learning plan (AWS · Docker / Kubernetes · Observability)

Aligned with your goals in `DETAILS-NEEDED-FILLED.md`. Use alongside `interview-prep/MONTH-PLAN.md` in this workspace.

## Principles

- One **small runnable project** per pillar beats passive video courses.
- Stay in **Free Tier** or explicit budget caps for AWS.

---

## AWS (4–6 weeks, part-time)

| Week | Focus | Hands-on |
|------|--------|----------|
| 1 | IAM users vs roles, MFA, CLI `aws configure`, regions | Create a role for CLI; no long-lived keys on your laptop if you can avoid it |
| 2 | VPC: subnets (public/private), route tables, IGW, NAT concept | Draw your VPC; optional: Terraform or console-only VPC |
| 3 | EC2 + security groups + SSH/bastion pattern | Launch Linux, tighten SGs, practice `ssm` session if you adopt SSM |
| 4 | S3, IAM policies for least privilege, encryption basics | Static site or log bucket with bucket policy exercise |
| 5 | RDS or Dynamo at “read the docs + one lab” level | Understand backups, parameter groups at high level |
| 6 | Capstone | **One** end-to-end app: e.g. small API on EC2 or Lambda + API Gateway + CloudWatch logs |

**Certs (optional):** AWS Certified Cloud Practitioner first if you want a credential; **Solutions Architect Associate** when you are comfortable with VPC + IAM + core services.

**Official:** [AWS Skill Builder](https://skillbuilder.aws/) and service FAQs.

---

## Docker (2–3 weeks)

1. Dockerfile instructions, layers, `.dockerignore`, **non-root** user.
2. **Multi-stage** builds for smaller images.
3. Compose: two services (app + DB or app + cache), networks, volumes.
4. Push to a registry; tag strategy (`:git-sha`).

**Capstone:** Containerize a tiny Python or Node API you own; CI job that builds and scans the image (Trivy or GitHub’s supply chain features).

---

## Kubernetes (4–6 weeks, after Docker)

1. Pods, Deployments, Services, ConfigMaps, Secrets, probes.
2. `kubectl` debugging: `describe`, logs, events, port-forward.
3. Resources: requests/limits; Namespaces; basic NetworkPolicy reading.
4. Helm: install chart, override values, **read** what it creates.

**Environment:** minikube, kind, or Killercoda Kubernetes playgrounds.

**Capstone:** Deploy your containerized API with a Service and health checks; document failure modes in a short `troubleshooting.md`.

---

## Observability — Prometheus + Grafana (3–4 weeks)

**Why this pair:** Widely asked in interviews, self-hostable locally, strong mental model (metrics → rules → alerts → dashboards).

1. **Metrics model:** counters vs gauges vs histograms; labels and **cardinality** discipline.
2. Prometheus: scrape config, `up`, basic PromQL (`rate`, `histogram_quantile` later).
3. Grafana: datasource, dashboards as code (JSON in repo optional).
4. Alerting: Alertmanager basics; **when not to page**.

**Capstone:** Docker Compose with app + Prometheus + Grafana; three dashboards you would actually look at during an incident rehearsal.

---

## Weekly time box (example)

- **8–10 hours/week:** 2 blocks × 2h deep work + 1h review notes + 1h hands-on lab.

Track progress in `interview-prep/TOPICS-CHECKLIST.md`.
