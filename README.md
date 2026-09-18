# TorinAI Unified Cognitive Substrate

**A persistent cognitive substrate: one shared state, a set of interacting faculties, and a governance
boundary that decides what becomes authoritative.**

Stefan Ragland, Dominion Labs Research & Development. Published 18 March 2025.

- Paper (PDF): [`paper/unified-substrate.pdf`](paper/unified-substrate.pdf)
- Paper (web): <https://dmnlabs.org/research/unified-substrate/>
- Contact: research@dmnlabs.org

## What this document is

The architecture overview. Rather than treating intelligence as the output of a single model invocation,
the substrate organises cognition as faculties operating over one shared persistent state: reasoning
changes beliefs, experience produces learning, learning produces operators and knowledge, competence
shapes exploration, goals drive planning and action, action is independently re-observed, and epistemic
governance controls when an internally generated conclusion may become authoritative or executable.

No component consults a language model. The one module that once could, a teaching policy that proposed
candidate lessons for the substrate to test, has been removed along with every model entry point, so the
property is structural rather than a matter of configuration.

## Where each mechanism stands

Each faculty is studied on its own, with its data, in a companion paper. Every study was re-run against
the live substrate in September 2026.

| Faculty | Result | Paper and data |
|---|---|---|
| Learning | 14/14 held-out cases; competence localised to the induced rules by a causal ablation | [model-free-rule-induction](https://github.com/DominionLabsInc/model-free-rule-induction) |
| Reasoning | 37/37 correct on the questions it answered, 13 honest abstentions | [reasoned-vs-believed](https://github.com/DominionLabsInc/reasoned-vs-believed) |
| Knowledge and competence | 16/16 checks; a declarative gap registered with competence unmoved at 0.500 | [knowledge-and-competence](https://github.com/DominionLabsInc/knowledge-and-competence) |
| Execution | 27/27 checks; a pursuit closed once, from the re-observed world | [grounded-task-completion](https://github.com/DominionLabsInc/grounded-task-completion) |
| Governance | a false rule refused authority; contamination 0 at every derivation depth | [systemic-epistemic-governance](https://github.com/DominionLabsInc/systemic-epistemic-governance) |
| Perception | 30/30 things admitted with their measured features; 0 false namings | [structure-before-meaning](https://github.com/DominionLabsInc/structure-before-meaning), [perceive-induce-name](https://github.com/DominionLabsInc/perceive-induce-name) |

`data/scale.json` records the counts quoted in section 14, measured 18 September 2026.

## Citation

```bibtex
@techreport{ragland2025substrate,
  title       = {TorinAI Unified Cognitive Substrate},
  author      = {Ragland, Stefan},
  institution = {Dominion Labs},
  year        = {2025},
  month       = {3},
  url         = {https://dmnlabs.org/research/unified-substrate/}
}
```

## License

The paper is released under [Creative Commons Attribution 4.0](LICENSE). Please cite it if you use it.
