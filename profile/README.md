# Borge Labs

Borge Labs is an independent Norwegian AI systems lab and product studio. We
build source-grounded products and the supervised delivery systems used to
make them.

## Products

- [Politikkradar](https://politikkradar.no) makes Norwegian political
  information easier to follow with visible sources and provenance.
- [Ordrett](https://ordrett.app) provides Norwegian-first transcription for
  meetings, interviews, lectures, and other spoken material.
- [Kontert](https://kontert.no) is self-hosted, AI-assisted bookkeeping for
  Norwegian party branches, associations, and sole proprietorships, now in
  early access.

## Open-source research

- [AI Dev Team](https://github.com/Borge-Labs/ai-dev-team) is a self-hosted
  runtime for supervised coding agents, with isolated workspaces,
  runner-observed verification, review artifacts, cost tracking, and human
  decision points - with published benchmarks, negative results included.
- [AI Team](https://github.com/Borge-Labs/ai-team) is a Slack-native framework
  for configurable AI teammates with scoped memory, tools, and a supervised
  handoff to coding workflows, in daily internal use.
- [claude-second-opinion-mcp](https://github.com/Borge-Labs/claude-second-opinion-mcp)
  provides bounded, non-blocking cross-model reviews over MCP, published on
  [npm](https://www.npmjs.com/package/claude-second-opinion-mcp).

These are working research releases used inside Borge Labs, published so others
can inspect, learn from, and fork them. They are not supported products and do
not come with a roadmap or response-time commitment.

## How the code here gets written

By AI agents, deliberately: frontier models plan, review and take the hard
judgment calls, while cheaper API models and local open-weight models running
on our own GPUs (llama.cpp, vLLM on a bare-metal Kubernetes fleet) implement
the lighter tiers. Changes pass cross-model review and land only through
human-owned specification and merge gates. The operating model, honest
limitations included, is written up in
[the supervised delivery loop note](https://borge-labs.no/notes/supervised-multi-agent-delivery/).

Our operating loop is simple:

> Need → context → plan → isolated implementation → tests and evidence →
> review → human decision → learning

Learn more at [borge-labs.no](https://borge-labs.no).
