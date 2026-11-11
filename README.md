# CAJAL Tool for OpenCode

> Add scientific paper generation to your OpenCode workflow. Local, free, MIT.

<!-- impact-note:start -->
<sub><strong>Efficiency and practical value.</strong> The OpenCode adapter packages paper, abstract, methods, reference and review commands into an existing development workflow. Reusing these commands can reduce repeated prompt assembly when documenting code and research, with local model execution available through the documented backend. The <a href="#usage">command interface</a> supports drafting convenience; generated results and citations must be checked against actual evidence.</sub>
<!-- impact-note:end -->

## What This Tool Does

Extends OpenCode with a `/paper` slash command that generates publication-ready scientific papers via local LLM.

## Why CAJAL + OpenCode?

OpenCode is the **fastest-growing open-source coding agent** (148K ⭐). Researchers using OpenCode can now:
1. Generate papers from their codebase analysis
2. Create AGENTS.md documentation with academic rigor
3. Export research findings as structured papers
4. All local, zero API cost

## Installation

```bash
# 1. Install CAJAL
pip install cajal-p2pclaw

# 2. Add to OpenCode tools
git clone https://github.com/Agnuxo1/cajal-opencode-tool.git ~/.opencode/tools/cajal-papers

# 3. Register in opencode config
opencode tools add cajal-papers

# 4. Create Ollama model
ollama create cajal -f https://raw.githubusercontent.com/Agnuxo1/CAJAL/main/integrations/ollama/Modelfile
```

## Usage

Inside any OpenCode session:

```
/paper "Quantum error correction with surface codes"
```

Generates a complete paper with real citations.

Commands:
- `/paper abstract "Your topic"` — 150-250 words
- `/paper methods "Your methodology"` — Reproducible methods section
- `/paper refs "Your topic" 10` — 10 relevant references with DOIs
- `/paper review file.md` — Peer review with scores

## Configuration

Add to `AGENTS.md` in your project:

```markdown
## CAJAL Paper Generator
- Tool: `cajal-papers`
- Model: `cajal` (Ollama)
- Default references: 8
- Format: markdown
```

## Integration with OpenCode Zen

If using OpenCode Zen (recommended models):
- CAJAL works with any Zen model via Ollama bridge
- Zero additional cost
- Papers stay local even with Zen remote sessions

## License

MIT — Gift economy. Not a product.

---

**Created by:** [P2PCLAW Research Network](https://p2pclaw.com)  
**GitHub:** [Agnuxo1/CAJAL](https://github.com/Agnuxo1/CAJAL)
