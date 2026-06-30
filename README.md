agents-stack-decision

An interactive decision aid for choosing how to architect an AI agent. It turns the framework from Paolo Perrone's article "The AI Agents Stack (2026 Edition)" into a tool you can click through: answer a few questions about what you are building, and it points you at the specific layers that matter, the architecture underneath, and the honest trade-offs at each one.

Live version: https://jramnath.github.io/agents-stack-decision/

Why this exists

The core idea in the article is that a tool-calling chatbot and a multi-agent research system share almost no infrastructure, so the expensive mistake is half-building all six layers of the stack instead of investing in the ones your specific agent needs. This tool makes that decision concrete rather than something you hold in your head while reading.

How it works

The experience is three connected steps.


Decide your path. Answer three questions about state, control flow, and coordination. The tool routes you to one of four archetypes: stateless tool caller, multistep workflow, agent that learns, or multi-agent system.
The four archetypes. Each archetype shows its recommended stack, which of the six layers are core versus optional versus skippable, and the part that is actually hard to build. A collapsible matrix compares all four at a glance.
Layer deep-dive. Each of the six layers (models, protocols and tools, memory, frameworks, eval, guardrails) is scored on three axes (how much state you manage, how much vendor lock-in you take on, and how large the demo-to-production gap is), with strengths, watch-outs, the author's "honest take," and the open problems.


Running it locally

The whole thing is a single self-contained HTML file with no build step, no dependencies, and no external scripts. To run it offline, download index.html and open it in any modern browser.

Sources and attribution

This is an unofficial interactive companion. All concepts, structure, and the quoted "honest takes" belong to Paolo Perrone. Please read the original first:


Paolo Perrone, "The AI Agents Stack (2026 Edition)", The AI Engineer.


Supporting data woven into the layer deep-dives comes from:


Endor Labs on MCP security exposure
LangChain, State of Agent Engineering on the observability-versus-eval gap
OWASP MCP Top 10
Letta, The AI agents stack for the 2024 baseline this update is measured against


A note on reuse

The visualization code here is mine to share, but the underlying framework and content are Paolo's. Treat this as a companion to his work, keep the attribution intact, and read the source article.
