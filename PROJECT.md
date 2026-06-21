# NeuronLine

NeuronLine is a TypeScript workspace for privacy-first, browser-local online
learning and real-time user behavior prediction. It owns the core learning
engine, predictor modules, demo application, package metadata, and product
documentation for local personalization use cases.

## Lifecycle

- State: `active`
- Layer: `foundation`
- Machine manifest: [`.doctrine/project.json`](./.doctrine/project.json)

## Goals

- Provide lightweight online-learning primitives for real-time, local,
  privacy-preserving personalization.
- Keep core learners, predictor modules, demos, tests, and package exports
  modular and tree-shakeable.
- Support experimentation with bandits, A/B testing, recommendations, and
  browser-local prediction without moving consumer product data out of the
  browser.

## Non-Goals

- This repository does not own consumer product recommendation policy,
  analytics collection policy, user consent, or production experimentation
  governance.
- This repository does not own server-side ML platforms, centralized user
  profile storage, or cross-product data pipelines.
- This repository does not own enterprise doctrine, manifest schema, rollout
  planning, org rulesets, or shared CI policy.

## Boundary

The repository owns NeuronLine package source, workspace structure, demo app,
tests, documentation, and package-level APIs. Product teams consuming
NeuronLine own their own recommendation policy, consent flow, analytics
contracts, and production experiment governance.

## Public Surfaces

- Workspace package metadata: `package.json`
- Core package metadata and exports: `packages/core/package.json`
- Predictor package metadata and exports: `packages/predictors/package.json`
- Product README: `README.md`
- Improvement notes: `IMPROVEMENTS.md`
- Demo app: `apps/demo/`
- Human project orientation: `PROJECT.md`
- Machine-readable project manifest: `.doctrine/project.json`

## Delivery

- CI model: `none`
- Required contexts: none declared
- Deploy/release path: no package publish, demo deploy, or release workflow is
  declared in this repository.
- Production proof: package build/test/typecheck, bundle size, browser-local
  privacy proof, package readback, and demo smoke evidence are not yet declared
  as a durable release gate.
- Recovery class: `source-revertable`

Adoption is baseline only. The current gaps are tracked in
`.doctrine/project.json`.
