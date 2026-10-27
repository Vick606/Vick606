<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0f172a&height=180&section=header&text=Victor%20K.&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=40&desc=AI%20Security%20%C2%B7%20Evaluation%20%C2%B7%20Red-Teaming&descAlignY=62&descSize=16" alt="Victor K. | AI security, evaluation, and red-teaming" width="100%"/>

</div>

### Hi, I'm Victor

AI security and evaluation engineer. I build open-source tools that measure how AI systems fail, then make those failures harder to repeat. My route into this field ran through hands-on model evaluation and red-teaming, so I design detectors against real failure cases and publish the misses next to the hits.

Open to contract work in AI evaluation, red-teaming, and AI security tooling.

### Featured projects

| Project | What it does |
| --- | --- |
| **[Subcanopy Guard](https://github.com/Vick606/subcanopy-guard)** | Context-aware scanner for indirect prompt injection in agent tool outputs. Pure Python, zero runtime dependencies, `pip install subcanopy-guard`. |
| **[Subcanopy Gateway](https://github.com/Vick606/subcanopy-gateway)** | HTTP gateway for Subcanopy Guard. Scans prompts and tool outputs, stores scan history, and searches known attack patterns. |
| **[verirust](https://github.com/Vick606/verirust)** | Rust CLI that compiles and verifies code submissions, returning a deterministic ACCEPTED or REJECTED verdict for RLVR training pipelines. |
| **[sid-ea-findings-lab](https://github.com/Vick606/sid-ea-findings-lab)** | Structured findings for LLM agent and RAG vulnerabilities. Every scenario ships vulnerable, fixed, and hard-negative variants with traces, deterministic tests, and Semgrep rules. |
| **[RepoProbe](https://github.com/Vick606/repo-probe)** | Clones a Python repo, detects its test setup, runs the tests in Docker, and emits a structured JSON report. v0.1.0, 22 unit tests, verified on pallets/click. |
| **[issue-scout](https://github.com/Vick606/issue-scout)** | Curates GitHub issues into a versioned dataset for evaluating LLM bug-fixing. |

### Subcanopy Guard, with the caveats

On AgentDojo v1 it catches 86.5% of 629 attacks buried in tool output, at a 5.2% false positive rate (p50 0.88 ms). On the broader PromptWall set it catches 47.0% with zero false positives, which is the better guide to how well it generalizes. Known weak spots are documented in the repo.

```bash
pip install subcanopy-guard
scg scan --source tool_output response.json
```

```python
from subcanopy_guard import ContextScanner

scanner = ContextScanner(source="tool_output")
result = scanner.scan(tool_response)
if result.severity in ("HIGH", "CRITICAL"):
    ...  # block or review
```

Requires Python 3.14+.

### Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=py,rust,ts,docker,git,linux,githubactions&theme=dark" alt="Python, Rust, TypeScript, Docker, Git, Linux, GitHub Actions" />

</div>

### Focus for 2026

Subcanopy Guard v0.5.0 (streaming scanner and framework integrations), plus wider OWASP LLM Top 10 coverage.

### Reach me

<div align="center">

<a href="https://www.linkedin.com/in/victor-koech-b69407136/">
  <img src="https://img.shields.io/badge/LinkedIn-victor--koech-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" />
</a>
<a href="https://pypi.org/project/subcanopy-guard/">
  <img src="https://img.shields.io/badge/PyPI-subcanopy--guard-3776AB?style=flat-square&logo=pypi&logoColor=white" alt="PyPI" />
</a>
<a href="mailto:vickoch20@gmail.com">
  <img src="https://img.shields.io/badge/Email-get%20in%20touch-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
</a>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0f172a&height=100&section=footer" alt="" width="100%"/>
