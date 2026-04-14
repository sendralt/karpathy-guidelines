# Karpathy Guidelines — Agent Zero Plugin

An [Agent Zero](https://github.com/frdel/agent-zero) plugin that automatically injects [Andrej Karpathy's](https://x.com/karpathy/status/2015883857489522876) behavioral coding guidelines into every conversation to reduce common LLM coding mistakes.

## What It Does

When enabled, this plugin auto-injects four key behavioral guidelines into the system prompt:

1. **Think Before Coding** — State assumptions, surface tradeoffs, ask when unclear
2. **Simplicity First** — Minimum code, no speculative features or unnecessary abstractions
3. **Surgical Changes** — Only touch what's necessary, match existing style
4. **Goal-Driven Execution** — Define verifiable success criteria, loop until verified

## Installation

1. Clone this repo into your Agent Zero plugins directory:
   ```bash
   git clone https://github.com/sendralt/karpathy-guidelines /path/to/agent-zero/usr/plugins/karpathy-guidelines
   ```
2. Go to **Agent Zero Web UI → Settings → Plugins**
3. Find **Karpathy Guidelines** and toggle it on

## Plugin Structure

```
karpathy-guidelines/
├── plugin.yaml          # Plugin metadata and config
├── hooks.py             # Install/uninstall lifecycle hooks
├── prompts/
│   └── default.md       # Auto-injected guidelines
└── README.md
```

## License

MIT
