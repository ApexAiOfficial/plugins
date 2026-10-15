# ApexAiOfficial fork of openai/plugins

This fork is the ApexAI workstation's authoritative source for the components it
uses from [openai/plugins](https://github.com/openai/plugins). Architecture, provenance and runbooks:
ApexAiOfficial/agent-skills-platform (private).

## Branches

| Branch | Meaning | Who moves it |
|---|---|---|
| `main` | Untouched mirror of upstream `main`. Never commit here. | `scripts/upstream-sync` (fast-forward only) |
| `apex/dev` | ApexAI changes on top of upstream. Upstream is merged in here first. | ApexAI maintainers |
| `apex/stable` | Reviewed, known-good revision that runtimes pin to. | `scripts/promote` (fast-forward + `apex-stable-*` tag) |

## ApexAI changes

Marketplace renamed so Claude Code / Codex accept it from a non-upstream source
(upstream names are reserved for the upstream organisation):

| Manifest | Upstream name | ApexAI name |
|---|---|---|
| `.agents/plugins/marketplace.json` | `openai-curated` | `apex-openai-plugins` |
| `.agents/plugins/api_marketplace.json` | `openai-api-curated` | `apex-openai-api-plugins` |

Plugin and skill names are unchanged. Each component keeps its own upstream license
and terms; see the component's LICENSE file.
