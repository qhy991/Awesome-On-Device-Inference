# Contributing

## Scope

This repository indexes work that helps readers design or evaluate on-device LLM inference systems. Favor entries with a clear systems contribution, such as one of these:

- Execution across CPU, GPU, NPU, another accelerator, or storage.
- Scheduling, graph partitioning, compilation, or synchronization.
- Weight, activation, or KV cache movement.
- Low-bit kernels or quantization methods that target device execution.
- Sustained latency, throughput, energy, or thermal characterization.
- An inference engine or runtime used on mobile or edge devices.

Do not add a model solely because it is small. Explain the inference-system property that makes it relevant.

## Evidence requirements

Use the strongest public record available.

| Entry type | Required evidence |
| --- | --- |
| Paper | DOI, publisher page, OpenReview page, or exact arXiv identifier |
| Engine | Canonical source repository or official product documentation |
| Community project | Canonical source repository with the community status stated |
| Benchmark or measurement | Reproducible workload, device, runtime, precision, timing boundary, and source |

Do not copy a benchmark number without its protocol. Do not describe a backend as supported when the only evidence is a roadmap item, an out-of-tree patch, or an unverified social post.

## Entry format

Use the table for the entry's primary bottleneck. Keep the description factual and narrow. Name the mechanism, then name the hardware or phase it affects.

```markdown
| [Exact title](https://canonical.example) | Venue and year | One systems mechanism and its target constraint. | `[NPU]` `[KV]` `[Decode]` |
```

Prefer one entry per contribution. If a paper spans two categories, use its primary contribution as the owner and add a cross-reference from another reading path when that helps navigation.

## Pull request checklist

- The link resolves to the exact work, repository, or documentation page.
- The title matches the canonical source.
- The venue label identifies a peer-reviewed venue only when one exists.
- Hardware and bottleneck tags match the stated mechanism.
- The description avoids unsourced speedups, energy savings, and model-quality claims.
- Existing entries do not already cover the same contribution.

## Corrections

Open an issue or pull request when a link, title, venue, or capability claim is wrong. Include the public evidence for the correction. Capability claims that depend on a vendor runtime should name the runtime and device family in the pull request.
