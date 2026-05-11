# FlowLayer

**Local-first orchestration for multi-service development environments.**

FlowLayer helps developers run, observe, and control complex local development stacks without turning every workflow into a miniature Kubernetes reenactment, because apparently launching five services in the right order is still considered a recreational puzzle.

## What FlowLayer is

FlowLayer is a developer tool for managing multi-service local environments.

It is designed for projects where a single `npm run dev` is no longer enough: APIs, workers, databases, queues, frontend apps, background jobs, and other services that need to start in a predictable order and become ready before the rest of the stack continues.

FlowLayer focuses on:

- deterministic service startup
- readiness checks
- real-time logs
- local stack supervision
- explicit JSONC configuration
- a documented WebSocket protocol
- a terminal client for day-to-day operation

## Why it exists

Modern development environments are often distributed systems in disguise.

Developers need to start several services, inspect logs, understand failures, restart components, and keep enough visibility to avoid debugging by folklore and despair.

FlowLayer aims to provide a lightweight local control plane for that workflow.

It is not trying to replace production orchestrators. It is built for the local development loop: fast feedback, clear state, readable logs, and predictable service coordination.

## Core repositories

| Repository | Description |
|---|---|
| [`flowlayer`](https://github.com/FlowLayer/flowlayer) | Public protocol, configuration, documentation, releases, and issue hub |
| [`tui`](https://github.com/FlowLayer/tui) | Official terminal client for observing and controlling FlowLayer sessions |
| [`distribution`](https://github.com/FlowLayer/distribution) | Distribution manifests and installer channel material |

## Main features

- Define services in a JSONC configuration file
- Start services with explicit dependencies and startup waves
- Wait for readiness before unlocking dependent services
- Stream service logs in real time
- Observe service state through a terminal UI
- Use a documented WebSocket protocol for custom clients and integrations
- Keep local orchestration understandable instead of hiding everything behind yet another stack of sacred YAML tablets

## Website

Visit the project website:

https://flowlayer.tech

## Status

FlowLayer is under active development.

The public repositories contain the protocol, documentation, website, terminal client, distribution material, and project-facing resources.

## Philosophy

FlowLayer is built around a simple idea: local development should be observable, predictable, and boring in the best possible way.

A developer should be able to understand what started, what failed, what is ready, and why the stack is blocked without opening six terminals and conducting an archaeological dig through logs.
