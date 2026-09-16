# Contributing

Pull requests are welcome. Add only work you can personally recommend.

## Scope

A code world model is a world model whose state, dynamics, observation process, reward, or constraints are represented or executed, at least in part, as explicit programs. The question is whether code participates in modeling the world, not whether a coding agent wrote the software.

In scope regardless of how the program is written: Python simulators, DSLs and symbolic programs, database-backed environments, physics scripts, executable transition functions over a scene graph, and code dynamics paired with a neural renderer.

Out of scope: general video, embodied, and driving world models; general coding agents; and prompt-to-game generators whose claim is playable software rather than code as dynamics. Point readers to [Awesome World Models](https://github.com/leofan90/Awesome-World-Models) instead of copying those catalogs here.

## Choosing a section

Sections answer one question only: what role does code play with respect to the world. Everything else is a tag, which is what keeps the structure stable as the field moves into robotics, 3D, and continuous physics.

- Experience or trajectories reverse engineered into executable dynamics goes in World Model Induction.
- Rules or a specification that already state the dynamics, compiled into an executable model, goes in World Model Synthesis.
- Program state paired with a neural model that supplies the observations goes in Programmable and Hybrid World Models.
- A newly authored environment used to train or supervise an agent, rather than a model of an existing world, goes in Executable Environment Generation. This section is adjacent, not core.
- Work whose contribution is measuring fidelity, adequacy, or correctness goes in Evaluation, Verification, and Benchmarks, alongside the benchmark resources themselves.

A paper appears once, under its primary role, and carries tags for the rest. PatchWorld induces a program and repairs it against counterexamples, so it is filed under induction and tagged `counterexample-repair`. Do not add sections for provenance, update regime, observability, or application domain.

Self-evolving world models do not have their own section yet. Every candidate so far contributes an induction method whose update loop is one component, so a section would duplicate induction rather than stand beside it. When two or more papers treat continual revision of the world model as the contribution itself, propose the split in an issue first.

## Tags

Use the vocabulary listed in the README's Tags section, four to six per entry, ordered representation, update, observability, modality, usage, domain. Omit an axis rather than guess at it. A new tag needs an issue and at least two papers that would carry it, otherwise the vocabulary stops being comparable across entries.

## Paper entries

Edit [README.md](README.md). Place new papers at the top of the matching section. Use this format, and omit links that do not exist:

```markdown
- **ShortName**: "Full Paper Title", *Venue, Month Year*. [[Paper](https://arxiv.org/abs/xxxx.xxxxx)] [[Code](https://github.com/org/repo)] [[Website](https://project.page/)] `tag` `tag`
```

Prefer the arXiv abstract page over a PDF. Keep venue italic and match the punctuation and link labels already used in the same section.

## Resource entries

Models, datasets, benchmarks, and related lists use a short name, a dash, and a one-sentence description, and carry no tags. When the resource was released with a paper, name that paper and its date so entries can be dated like the paper sections:

```markdown
- **ShortName** - One-sentence description. *From SourcePaper, Month Year*. [[HF](https://huggingface.co/org/name)]
```

Omit the source clause only for standalone resources that have no accompanying paper, such as another curated list.

## Pull requests

1. Search the README first so the entry is not a duplicate.
2. Add the item in reverse chronological order within its section.
3. Keep formatting consistent with neighboring entries.
4. Do not add empty sections, emoji section icons, or CI badges.
