# Awesome PaaS [![Awesome](https://awesome.re/badge.svg)]

> A curated list of **deployment platforms** — both managed SaaS/PaaS and self-hosted alternatives. Git push (or `docker build`) in, running app out. Covers container-based PaaS, Kubernetes-native platforms, serverless/edge, BYOC (bring-your-own-cloud) tools, backend-as-a-service, and self-hosted control panels you run on your own VPS or cluster. Language/stack agnostic — not tied to any one framework.

## Contents

- [General-purpose PaaS](#general-purpose-paas)
- [Kubernetes-native PaaS](#kubernetes-native-paas)
- [BYOC (bring-your-own-cloud) platforms](#byoc-bring-your-own-cloud-platforms)
- [Preview / ephemeral environments](#preview--ephemeral-environments)
- [Backend-as-a-Service (BaaS)](#backend-as-a-service-baas)
- [Jamstack & frontend hosting](#jamstack--frontend-hosting)
- [Serverless / edge / functions](#serverless--edge--functions)
- [Hyperscaler-native container & serverless services](#hyperscaler-native-container--serverless-services)
- [AI sandboxes & agent infrastructure](#ai-sandboxes--agent-infrastructure)
- [Cloud IDEs & dev workspaces](#cloud-ides--dev-workspaces)
- [Regional / niche / language-specific PaaS](#regional--niche--language-specific-paas)
- [Self-hosted PaaS](#self-hosted-paas)
- [Defunct (historical reference)](#defunct-historical-reference)
- [Decision cheatsheet](#decision-cheatsheet)

---

## General-purpose PaaS

The core "not self-hosted" tier. Connect a repo or push a Dockerfile, get a running, scaled, TLS-terminated app with managed databases alongside it.

- [**Railway**](https://railway.app/) — Fastest setup, cleanest developer experience, one-click Postgres/Redis/Mongo plugins, per-second usage billing. AI-native features (MCP server, agent sandboxes) as of 2026.
- [**Render**](https://render.com/) — The steady, "boring reliable" Heroku successor. Permanent free tier, managed Postgres with point-in-time recovery, background workers, cron jobs.
- [**Fly.io**](https://fly.io/) — Deploys Docker images as Firecracker micro-VMs across 30+ regions with automatic nearest-region routing. CLI-first (`flyctl`), strongest for WebSockets/long-lived connections.
- [**Heroku**](https://www.heroku.com/) — The original PaaS (2007), now Salesforce-owned; effectively in maintenance mode but still relevant for its mature add-on ecosystem.
- [**DigitalOcean App Platform**](https://www.digitalocean.com/products/app-platform) — Git-push or Docker deploys tied to the DigitalOcean ecosystem.
- [**Clever Cloud**](https://www.clever-cloud.com/) — French/EU-based PaaS, controlled/predictable cost model.
- [**Scalingo**](https://scalingo.com) — Another French PaaS, positioned as a European Heroku alternative.
- [**Kuberns**](https://kuberns.com/) — AI agent detects your stack from the repo and auto-configures the deployment workflow.
- [**Back4app Web Deployment**](https://www.back4app.com/web-deployment-platform) — Deploys full-stack web apps from GitHub onto managed, secure infrastructure.
- [**Aptible**](https://aptible.com) — HITRUST R2 certified, compliance-first hosting for digital health teams.
- [**Convox**](https://convox.com) — Multi-cloud PaaS with consistent deployment workflows.
- [**Koyeb**](https://www.koyeb.com) — High-performance infra for APIs, inference, and databases across CPUs, GPUs, and accelerators.
- [**Sevalla**](https://sevalla.com) — Modern application hosting platform from the Kinsta team.
- [**Sliplane.io**](https://sliplane.io) — Fully managed Container-as-a-Service that simplifies Docker hosting.
- [**SnapDeploy**](https://snapdeploy.dev) — Docker container hosting on AWS; free until you need always-on.
- [**Zeabur**](https://zeabur.com) — "AI DevOps engineer" — an agent that runs infrastructure while AI writes the code.
- [**Appliku**](https://appliku.com) — Deploy unlimited apps and databases for one flat monthly price via git push.
- [**apply.build**](https://apply.build) — European PaaS with WAF, vulnerability scanning, metrics, and logs included in every plan.
- [**Genezio**](https://genezio.com) — Full-stack platform with type-safe client/server communication.
- [**Diploi**](https://diploi.com/) — Cloud dev environments with one-click hosting, no manual server config.
- [**Mogenius**](https://mogenius.com) — Cloud-native development platform built on Kubernetes under the hood.
- [**Engine Yard**](https://www.engineyard.com) — Managed cloud platform historically for Ruby on Rails, now broader.
- [**Linode / Akamai Cloud**](https://www.linode.com) — Developer cloud with managed Kubernetes, databases, and compute.
- [**MicroCloud**](https://canonical.com/microcloud) — Canonical's lightweight, automated open-source cloud platform.
- [**InstaPods**](https://instapods.com) — One-command deploys for AI-built apps, very low cost.
- [**Acquia Cloud**](https://www.acquia.com) — Drupal-focused cloud platform for digital experiences (CMS-specific, included for completeness).
- [**fortrabbit**](https://www.fortrabbit.com) — "PHP as a Service" since 2012, EU-based, runs on AWS.
- [**platformOS**](https://platformos.com) — Fully managed PaaS positioned as having no vendor lock-in or hidden fees.
- [**France Nuage**](https://france-nuage.fr) — Sovereign open-source cloud hosted entirely in France.
- [**Flightcontrol**](https://www.flightcontrol.dev) — PaaS that deploys straight into your own AWS account (no black box, no AWS markup).
- [**Vultr**](https://www.vultr.com/) — Developer cloud with high-frequency compute, 32 data centers across 6 continents, one-click app deploys (Supabase, Docker, etc.).
- [**Kinsta**](https://kinsta.com/) — Managed application/database hosting on Google Cloud; strong for Laravel + WordPress shops running mixed stacks.

## Kubernetes-native PaaS

Give you Kubernetes semantics and power without requiring you to operate a cluster yourself.

- [**Northflank**](https://northflank.com/) — Full application lifecycle (CI/CD, managed databases, preview environments, GPU workloads, observability) on managed or your-own clusters.
- [**Qovery**](https://www.qovery.com/) — Provisions Kubernetes clusters inside your own AWS/GCP/Azure/Scaleway account via Terraform, plus a self-service developer portal. Ships a Terraform provider, CLI, API, MCP server, and AI agent skill.
- [**Porter**](https://porter.run) — Heroku-like deploy experience into your own AWS/GCP/Azure account; SOC 2 and HIPAA compliant, handles networking/TLS/autoscaling/CI-CD.
- [**Okteto**](https://okteto.com/) — Real-time code sync into remote Kubernetes namespaces; strong for fast inner-loop dev and per-branch previews.
- [**Cloud 66**](https://www.cloud66.com/) — DevOps automation that deploys to any cloud provider or your own servers, Kubernetes-aware.
- [**Zeet**](https://zeet.co) — Combines CI/CD, Kubernetes management, networking, and observability in one dashboard.
- [**TrueFoundry**](https://truefoundry.com) — Enterprise AI Gateway combining LLM, MCP, and Agent Gateways on top of Kubernetes infra.
- [**Humanitec**](https://humanitec.com/) — Internal Developer Platform aimed at enterprise platform-engineering teams.
- [**Komodor**](https://komodor.com/) — Autonomous AI SRE platform for Kubernetes operations.
- [**Portainer**](https://www.portainer.io/) — GUI-based container/Kubernetes management across on-prem, hybrid, and cloud.

## BYOC (bring-your-own-cloud) platforms

You keep the cloud account and the bill; the platform provides the deployment layer, RBAC, and workflow on top.

- [**Qovery**](https://www.qovery.com/) *(also listed above)* — pure BYOC business model, sells no compute itself.
- [**Porter**](https://porter.run) *(also listed above)* — bills for management only, not compute.
- [**Flightcontrol**](https://www.flightcontrol.dev) *(also listed above)* — deploys directly into your own AWS account.
- [**Ownkube**](https://ownkube.io) — Developer platform inside your own AWS account on k3s/EKS, with named "agents" (Cost, Incident, Scaling, Security) handling ops.
- [**AZIN**](https://azin.run) — Auto-deploys into your own GCP/AWS/Azure account straight from a git push.

## Preview / ephemeral environments

Platforms built specifically around per-PR / per-branch full-stack environments.

- [**Bunnyshell**](https://www.bunnyshell.com/) — Full environment lifecycle (preview, staging, prod, remote dev, AI sandboxes) on your own Kubernetes clusters; multi-stack (Docker Compose, Helm, Terraform).
- [**Release**](https://release.com/) — Vercel-style git-push deploys for full-stack apps, Kubernetes-native ephemeral environments per pull request.
- [**Shipyard**](https://shipyard.build/) — No-code test/preview environments and workflow previews.
- [**Namespace**](https://namespace.so/) — Ephemeral, fully isolated cluster provisioning (BYOC), optimized for fast spin-up via caching/reuse.
- [**Signadot**](https://www.signadot.com/) — Fast ephemeral Kubernetes sandboxes for testing code changes.

## Backend-as-a-Service (BaaS)

Bundled database + auth + storage + realtime, so you skip building a backend entirely. Adjacent to PaaS but frequently shortlisted alongside it for full-stack apps.

- [**Supabase**](https://supabase.com/) — Open-source Firebase alternative built on Postgres: auth, storage, realtime, auto-generated APIs, edge functions, and self-hostable if you want to run it yourself. ~10M+ developers as of mid-2026.
- [**Firebase**](https://firebase.google.com/) — Google's mature BaaS: Firestore (NoSQL), auth, storage, functions, hosting, analytics. Closed-source but battle-tested and deeply integrated with the rest of Google Cloud.
- [**Appwrite**](https://appwrite.io/) — Open-source, self-hostable backend platform with multi-language SDKs, popular for mobile/cross-platform apps.
- [**Nhost**](https://nhost.io/) — Open-source backend on Postgres + Hasura, GraphQL-first with realtime subscriptions.
- [**PocketBase**](https://pocketbase.io/) — Entire backend (DB, auth, file storage, realtime, admin UI) in a single Go binary — trivial to self-host, great for prototypes.
- [**AWS Amplify**](https://aws.amazon.com/amplify) *(also listed under Jamstack)* — Firebase/Supabase-style DX backed by AWS primitives (Cognito, AppSync, S3, Lambda).

## Jamstack & frontend hosting

Static-first and frontend-optimized hosting, increasingly full-stack-capable via functions.

- [**Vercel**](https://vercel.com/) — Best-in-class for Next.js; functions, cron, queues, workflows, storage. Scales to zero, no always-on process model.
- [**Netlify**](https://www.netlify.com) — Framework-neutral frontend hosting, deploy previews, functions. Now also home to the former Gatsby Cloud.
- [**Cloudflare Pages**](https://pages.cloudflare.com/) — Jamstack hosting on Cloudflare's global edge network.
- [**Firebase Hosting**](https://firebase.google.com/products/hosting) — Google's fast, secure web app hosting.
- [**GitHub Pages**](https://pages.github.com/) — Static site hosting directly from a GitHub repository.
- [**GitLab Pages**](https://docs.gitlab.com/ee/user/project/pages/) — Static site hosting integrated into GitLab.
- [**Surge.sh**](https://surge.sh) — Static publishing for frontend developers, one-command deploys.
- [**AWS Amplify**](https://aws.amazon.com/amplify) — Full-stack web/mobile app development platform on AWS.

## Serverless / edge / functions

Function- and edge-first compute, often WebAssembly-based.

- [**Cloudflare Workers**](https://workers.cloudflare.com/) — Serverless code execution on Cloudflare's global edge.
- [**Deno Deploy**](https://deno.com/deploy) — Global edge platform for JS/TS.
- [**Fastly Compute**](https://www.fastly.com/products/edge-compute) — Wasm edge computing on Fastly's global network.
- [**Wasmer Edge**](https://wasmer.io/products/edge) — WebAssembly-based edge platform.
- [**Akamai Functions**](https://www.fermyon.com) (formerly Fermyon Spin) — WebAssembly-based serverless platform, now part of Akamai.
- [**Suborbital e2core**](https://github.com/suborbital/atmo) (formerly Atmo) — Server for sandboxed third-party plugins, powered by WebAssembly.
- [**TinyFunction**](https://www.tinyfunction.com/) — Lightweight function hosting.

## Hyperscaler-native container & serverless services

Not PaaS in the "opinionated dashboard" sense, but the direct managed alternative once you're inside a hyperscaler account.

- [**AWS App Runner**](https://aws.amazon.com/apprunner) — Managed container service deploying directly from source or image.
- [**AWS ECS**](https://aws.amazon.com/ecs) — Amazon's managed container orchestration.
- [**AWS Lambda**](https://aws.amazon.com/lambda/) — Serverless compute, runs code without provisioning servers.
- [**Google Cloud Run**](https://cloud.google.com/run) — Fully managed serverless containers on GCP.
- [**Google Cloud App Engine**](https://cloud.google.com/appengine) — Fully managed serverless platform for web/mobile backends.
- [**Azure App Service**](https://azure.microsoft.com/en-us/products/app-service) — Managed app hosting across languages on Azure.
- [**Azure Functions**](https://docs.microsoft.com/en-us/azure/azure-functions/) — Event-driven, scheduled serverless compute on Azure.
- [**IBM Cloud Code Engine**](https://cloud.ibm.com/codeengine) — Fully managed serverless platform on IBM Cloud.
- [**DigitalOcean Functions**](https://www.digitalocean.com/products/functions) — DigitalOcean's serverless functions platform.

## AI sandboxes & agent infrastructure

Adjacent but increasingly overlapping category — compute platforms purpose-built for running AI-generated code or agent workloads.

- [**E2B**](https://e2b.dev/) — Secure sandboxes for AI agents; widely adopted across large enterprises.
- [**Daytona**](https://www.daytona.io/) — Secure infra for running AI-generated code, ~90ms environment creation.
- [**Modal**](https://modal.com) — Serverless platform for AI and data teams.
- [**Beam Cloud**](https://www.beam.cloud/) — AI infra for sandboxes, inference, and training with fast boot times.
- [**RunPod**](https://www.runpod.io) — GPU cloud for AI training and inference workloads.
- [**Runloop**](https://www.runloop.ai/) — AI agent accelerator with secure code sandboxes and evaluations.
- [**Adaptive**](https://www.adaptive.live/) — Access control plane for human, workload, and AI identities.

## Cloud IDEs & dev workspaces

Browser-based or cloud-hosted development environments — often paired with one-click deploy.

- [**GitHub Codespaces**](https://github.com/features/codespaces) — Instant cloud-powered dev environments from GitHub.
- [**Ona**](https://www.gitpod.io/) (formerly Gitpod) — Orchestrated background AI software engineers in the cloud.
- [**Replit**](https://replit.com/) — Build and deploy apps collaboratively with AI, in-browser.
- [**StackBlitz**](https://stackblitz.com/) — Instant in-browser dev environments powered by WebContainers.
- [**CodeSandbox**](https://codesandbox.io/) — Instant cloud development environments.
- [**AWS Cloud9**](https://aws.amazon.com/cloud9/) — AWS's browser-based IDE.
- [**Coder.com**](https://coder.com/) — Enterprise AI development infrastructure, self-hosted environments.
- [**Eclipse Che**](https://www.eclipse.org/che/) — Kubernetes-native cloud IDE.
- [**CoCalc**](https://cocalc.com/) — Collaborative calculation and data science platform.
- [**Encore**](https://encore.dev/) — Open-source TypeScript backend framework with automated infrastructure provisioning.

## Regional / niche / language-specific PaaS

- [**fortrabbit**](https://www.fortrabbit.com) *(also listed above)* — PHP-specific, Germany-based.
- [**Acquia Cloud**](https://www.acquia.com) *(also listed above)* — Drupal-specific.
- [**France Nuage**](https://france-nuage.fr) *(also listed above)* — France-only data residency.
- [**Scalingo**](https://scalingo.com) *(also listed above)* — France-based.
- [**Clever Cloud**](https://www.clever-cloud.com/) *(also listed above)* — France-based.

## Self-hosted PaaS

You run these yourself, on your own VPS or cluster — the direct alternative to paying a managed PaaS bill. Listed roughly by popularity/adoption within each cluster of similar tools, based on GitHub star counts as of mid-2026 where known.

**The big three (Docker/Compose-based, most widely adopted):**

- [**Coolify**](https://coolify.io/) — The most feature-complete all-rounder and most popular of the three (~57,000+ GitHub stars): 280+ one-click services, Docker Compose support, native multi-server, per-branch preview environments, free self-hosted tier under Apache-2.0. Fast release cadence — pin versions in production.
- [**Dokploy**](https://github.com/dokploy/dokploy) — Fast-rising lightweight challenger (~35,000+ stars): Docker Swarm + Traefik, clean modern UI, native Compose support. Still pre-1.0; some features live in a proprietary module, so check the license split before committing.
- [**Peon**](https://peon.sh/) — Open source self-hosted Docker deployment platform with Git push deploys, Compose, databases, TLS, backups, workspace RBAC, and a built-in Streamable HTTP MCP server for agents. Coolify/Dokploy alternative with project-level permissions.
- [**CapRover**](https://caprover.com/) — The battle-tested veteran, live since 2017 (~13,000–15,000 stars): rock-stable, Docker Swarm-based, 100+ one-click apps, native multi-node clustering. Dated UI, slower release cadence, limited Compose support (uses its own `captain-definition` format instead), no built-in database tooling.

**Also widely used:**

- [**Dokku**](https://dokku.com) — "The smallest PaaS implementation you've ever seen." Heroku-style git push deploys, terminal/CLI-first (no dashboard), supports almost any language via buildpacks.
- [**Kamal**](https://kamal-deploy.org) — Deploy web apps anywhere from bare metal to cloud VMs, by 37signals; the default deploy tool shipped with Rails 8.
- [**Easypanel**](https://easypanel.io) — Modern server control panel for deploying apps and databases; frequently shortlisted alongside Coolify/Dokploy.
- [**Portainer**](https://www.portainer.io/) — GUI-based container/Kubernetes management across on-prem, hybrid, and cloud; more general container-ops tool than a full PaaS, but commonly used the same way.

**Newer / smaller-footprint options:**

- [**Kubero**](https://github.com/kubero-dev/kubero) — Free, self-hosted PaaS running on Kubernetes.
- [**Canine**](https://canine.sh/) — Open-source PaaS for Kubernetes; Heroku simplicity, Kubernetes power.
- [**Uncloud**](https://uncloud.run) — Production self-hosting for Docker Compose apps without Kubernetes complexity.
- [**ZaneOps**](https://zaneops.dev) — Self-hosted, open-source PaaS using Docker Swarm.
- [**Disco**](https://disco.cloud/) — Self-hosted Heroku alternative for teams with many services/environments.
- [**Server Compass**](https://servercompass.app/) — Desktop-app-based deploy tool (not a web dashboard on your server); one-time payment, no subscription.
- [**Temps**](https://temps.sh/) — Bundles deployment with built-in analytics/error-tracking/uptime monitoring in one Rust binary, aiming to remove the extra $150–300/mo of bolted-on observability SaaS the others typically need.
- [**Piku**](https://github.com/piku/piku) — Tiny PaaS; git push deploys to your own servers.
- [**Podi**](https://github.com/coderofsalvation/podi) — ~7kb GitOps utility to turn servers into PaaS platforms via git+ssh.

**Framework/language-specific:**

- [**Hatchbox**](https://www.hatchbox.io) — Cost-effective hosting for Rails/Ruby/Node.js on your own infrastructure; the most Rails-native managed option.
- [**Ploi**](https://ploi.io) — Server management and site deployment tool (Laravel/PHP-first).
- [**Deploynix**](https://deploynix.io/) — Laravel-first managed control plane for your own servers.

**CI/CD, GitOps & Kubernetes delivery tooling (adjacent — not full PaaS, but part of the same self-hosted-deploy toolbox):**

- [**dyrector.io**](https://dyrector.io/) — Self-hosted CI/CD and deployment platform with version management.
- [**Digger**](https://digger.dev/) — Self-hostable Terraform CI/CD, drift detection, PR automation.
- [**Werf**](https://werf.io) — GitOps tool by Flant for delivering apps to Kubernetes.
- [**Skaffold**](https://skaffold.dev/) — Fast, repeatable workflow for Kubernetes development.
- [**Devtron**](https://devtron.ai) — Open-source software delivery workflow for Kubernetes.
- [**Plural**](https://www.plural.sh) — Open-source platform for deploying applications on Kubernetes.
- [**BoltOps**](https://www.boltops.com/) — DevOps-as-a-service.

**Full platform / enterprise-grade:**

- [**Knative**](https://knative.dev/docs/) — Kubernetes-based platform for serverless workloads.
- [**OpenFaaS**](https://www.openfaas.com/) — Serverless functions made simple with Kubernetes.
- [**OpenShift**](https://www.redhat.com/en/technologies/cloud-computing/openshift) — Red Hat's unified application platform for hybrid cloud.
- [**Cloud Foundry**](https://www.cloudfoundry.org/) — Open-source platform for cloud-native application development; long-standing enterprise PaaS.
- [**VMware Tanzu**](https://tanzu.vmware.com) — VMware's enterprise PaaS.
- [**Docker Swarm**](https://docs.docker.com/engine/swarm/) — Docker's built-in container orchestrator; the substrate under CapRover, Dokploy, and ZaneOps.
- [**Kubernetes**](https://kubernetes.io/) — Production-grade container orchestration; the substrate under most of the Kubernetes-native tools above.
- [**Akamai App Platform**](https://otomi.io/) (formerly Otomi) — Kubernetes app platform, now part of Akamai.

**Niche / smaller:**

- [**Linx**](https://linx.software) — Low-code iPaaS for integration, API development, business process automation.
- [**Spacecloud**](https://space-cloud.io/) — Instant realtime APIs for serverless apps.
- [**Spaceship / Shipmate**](https://spaceship.run) — One-click code launcher.

## Defunct (historical reference)

Kept here for context — these shaped the category even though they're no longer operating.

- **dotCloud** — became Docker, Inc.
- **Flynn** — early next-gen open-source PaaS, now unmaintained.
- **Gatsby Cloud** — sunset; folded into Netlify.
- **Glitch** (web hosting) — being phased out.
- **layer0** — rebranded to Edgio, later wound down.
- **Cyclic** — acquired and shut down.
- **Coherence** — site offline.
- **Zimki** — one of the original PaaS offerings (Canon), historical only.

---

## Decision cheatsheet

| Situation | Pick |
|---|---|
| Fastest setup, best all-round DX, small team | Railway |
| "Boring and reliable," free tier, managed Postgres | Render |
| Global low-latency / many regions / WebSockets | Fly.io |
| Full Kubernetes power without running a cluster | Northflank |
| Want K8s deployed into *your own* cloud account (BYOC) | Qovery, Porter, or Flightcontrol |
| Compliance-heavy (HIPAA/SOC2/GDPR), regulated industry | Aptible, or Qovery/Northflank with audit evidence in your own account |
| Next.js / frontend-heavy full-stack JS | Vercel |
| Framework-neutral static + functions | Netlify |
| Already deep in one hyperscaler, want managed containers only | AWS App Runner / Cloud Run / Azure App Service |
| Need per-PR full-stack ephemeral environments at scale | Bunnyshell, Release, or Namespace |
| Running AI-generated code / agent sandboxes | E2B, Daytona, or Modal |
| Want a Postgres backend + auth + storage without writing one | Supabase, Firebase, or Appwrite |
| Want to self-host: best all-rounder | Coolify |
| Want to self-host: lean, modern, Swarm-native | Dokploy |
| Want to self-host: maximum stability, minimal churn | CapRover |
| Want to self-host: pure CLI, no dashboard at all | Dokku |
| Want to self-host: Rails 8 default | Kamal |

---

## Contributing

PRs welcome — keep entries to one line, no affiliate links, and note if a listing is deprecated/maintenance-mode rather than removing it outright (history is useful).

## License

[MIT](LICENSE)
