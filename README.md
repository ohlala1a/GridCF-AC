# GridCF-AC

GridCF-AC is a controlled-variation dataset for AC power-flow restoration on PEGASE89, accompanying CoRe-Grid.

It contains **207 parent scenarios, 230 physical states and 490 task contexts**. Variants cover operator wording, verification budgets, fresh or stale tool evidence, and reactive-load changes.

| Split | Parents | States | Contexts |
|---|---:|---:|---:|
| Train | 160 | 174 | 284 |
| Validation | 17 | 22 | 78 |
| Test | 30 | 34 | 128 |

- `data/tasks.jsonl`: task specifications, language, evidence and budgets.
- `data/states/`: network JSON, scenario cards, initial candidate catalogues and metadata.
- `data/parents.jsonl`, `data/splits/`: lineage and task partitions.
- `validation/witnesses/`: offline repair sequences; do not expose them to evaluated agents.
- `protocol.json`, `statistics.json`: scoring settings and dataset counts.

Resolve data paths from the repository root. Networks use pandapower 3.4.0 JSON. Legal controls must be recomputed after each state change. Success requires AC convergence and full native feasibility, including the 0.9–1.1 p.u. voltage envelope. This is a data-only release.

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Sources and required attributions are in [NOTICE.md](NOTICE.md).
