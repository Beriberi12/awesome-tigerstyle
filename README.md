# Awesome TigerStyle [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources, tools, and examples for TigerStyle — a coding philosophy focused on safety, performance, and developer experience.

TigerStyle is a rigorous software engineering philosophy pioneered by [TigerBeetle](https://tigerbeetle.com/), the high-performance financial transactions database. It emphasizes writing code that is correct by construction, efficient by design, and a joy to maintain.

## Contents

- [Core Principles](#core-principles)
- [Official Resources](#official-resources)
- [Talks & Videos](#talks--videos)
- [Articles & Blog Posts](#articles--blog-posts)
- [Community Discussions](#community-discussions)
- [Related Projects](#related-projects)
- [Zig Resources](#zig-resources)
- [Foundational Reading](#foundational-reading)
- [Tools & Linters](#tools--linters)
- [Contributing](#contributing)

## Core Principles

TigerStyle prioritizes three design goals, in order:

1. **Safety** — Code that works correctly in all situations, crashes on programmer errors (assertions), and reduces the risk of bugs.
2. **Performance** — Efficient use of resources (network, disk, memory, CPU) through mechanical sympathy and back-of-the-envelope reasoning.
3. **Developer Experience** — Readable, maintainable code with excellent naming, clear structure, and minimal cognitive load.

### Key Tenets

- **Zero Technical Debt** — Do it right the first time; the second time may never come.
- **Zero Dependencies** — Minimize supply chain risk and maximize control.
- **Assertions Everywhere** — Assert preconditions, postconditions, and invariants. Minimum two assertions per function.
- **Pair Assertions** — For every property, assert it in at least two different code paths.
- **Put a Limit on Everything** — All loops, queues, and buffers have fixed upper bounds.
- **No Dynamic Allocation** — All memory statically allocated at startup.
- **Simple Control Flow** — No recursion, minimal abstractions, explicit is better than implicit.
- **Back-of-the-Envelope First** — Sketch performance before implementation.
- **Simulation Testing** — Use deterministic simulation and fuzzing as the final line of defense.

## Official Resources

- [TigerStyle Guide](https://github.com/tigerbeetle/tigerbeetle/blob/main/docs/TIGER_STYLE.md) — The original and authoritative TigerStyle document from TigerBeetle.
- [tigerstyle.dev](https://tigerstyle.dev/) — Community website distilling TigerStyle principles for broader audiences.
- [TigerBeetle GitHub](https://github.com/tigerbeetle/tigerbeetle) — The reference implementation of TigerStyle in a production system.
- [TigerBeetle Blog](https://tigerbeetle.com/blog/) — Engineering blog with deep dives on TigerStyle practices.
- [TigerBeetle Slack](https://slack.tigerbeetle.com/invite) — Community chat for TigerStyle discussions.

## Talks & Videos

- [TigerStyle! (Or How To Design Safer Systems in Less Time)](https://www.youtube.com/watch?v=w3WYdYyjek4) — Joran Dirk Greef's keynote at Systems Distributed '23. The definitive introduction to TigerStyle.
- [Zig SHOWTIME: TigerBeetle](https://youtu.be/BH2jvJ74npM?t=1958) — Deep dive into control plane vs data plane separation and batching strategies.
- [TigerBeetle Release Pipeline (Behind the Scenes!)](https://www.youtube.com/watch?v=eFTQzhfO6nc) — How TigerStyle principles apply to release engineering.
- [Building TigerBeetle](https://www.youtube.com/watch?v=sC1B3d9C_sI) — Technical overview of building a financial database with TigerStyle.

## Articles & Blog Posts

### From TigerBeetle

- [It Takes Two to Contract](https://tigerbeetle.com/blog/2023-12-27-it-takes-two-to-contract) — The philosophy behind pair assertions.
- [Synadia and TigerBeetle Pledge $512,000 to Zig](https://tigerbeetle.com/blog/2025-10-25-synadia-and-tigerbeetle-pledge-512k-to-the-zig-software-foundation/) — Why Zig aligns with TigerStyle philosophy.

### Community Articles

- [The Tiger Style](https://backend.how/posts/the-tiger-style/) — Backend.how's comprehensive breakdown of TigerStyle.
- [Tiger Style!](https://ratfactor.com/cards/tiger-style) — Ratfactor's take on the "stay away from keyboard" principle.
- [TigerStyle! in Bun/TypeScript](https://coreydemarse.com/posts/tigerstyle-typescript.html) — Applying TigerStyle principles outside of Zig.

## Community Discussions

- [TigerBeetle coding style guide – Lobsters](https://lobste.rs/s/w1rq9r/tigerbeetle_coding_style_guide) — Community discussion on assertions and safety nets.
- [TigerStyle! (How To Design Safer Systems) – Lobsters](https://lobste.rs/s/paq79n/tigerstyle_how_design_safer_systems_less) — Discussion on TigerStyle vs Go philosophy.
- [Tiger Style: Coding philosophy – Hacker News](https://news.ycombinator.com/item?id=46075628) — HN discussion on function length limits and modularity.

## Related Projects

### Projects Following TigerStyle

- [TigerBeetle](https://github.com/tigerbeetle/tigerbeetle) — High-performance financial transactions database. The canonical TigerStyle codebase.
- [simonklee/tigerstyle](https://github.com/simonklee/tigerstyle) — Community TigerStyle resources and examples.

### Projects with Similar Philosophies

- [SQLite](https://sqlite.org/) — Zero external dependencies, extensive testing, long-term stability.
- [SerenityOS](https://github.com/SerenityOS/serenity) — No third-party dependencies, everything from scratch.
- [Redox OS](https://www.redox-os.org/) — Microkernel OS in Rust with safety-first design.

## Zig Resources

TigerStyle is deeply intertwined with the Zig programming language. These resources help understand why.

- [Zig Language](https://ziglang.org/) — Official Zig website.
- [Zig Style Guide](https://ziglang.org/documentation/master/#Style-Guide) — Official Zig style conventions.
- [Why Zig?](https://ziglang.org/learn/why-zig-over-c-cpp/) — Zig's design philosophy aligns with TigerStyle.
- [Zig's Hidden Control Flow](https://isaacfreund.com/blog/2022-05/) — Why "abstractions are never zero cost."
- [Zig Software Foundation](https://ziglang.org/zsf/) — Supporting the Zig ecosystem.

## Foundational Reading

These works influenced TigerStyle or share its philosophy.

### Papers & Guidelines

- [NASA's Power of Ten Rules](https://spinroot.com/gerard/pdf/P10.pdf) — Gerard J. Holzmann's rules for safety-critical code. *Foundational to TigerStyle.*
- [The Mythical Man-Month](https://en.wikipedia.org/wiki/The_Mythical_Man-Month) — Brooks on "throwing one away" and design simplicity.
- [Out of the Tar Pit](http://curtclifton.net/papers/MosesEtAl06.pdf) — Complexity management in software systems.

### Books

- [Let Over Lambda](https://letoverlambda.com/) — "Style is necessary only where understanding is missing."
- [A Philosophy of Software Design](https://www.amazon.com/Philosophy-Software-Design-John-Ousterhout/dp/1732102201) — John Ousterhout on deep modules and complexity.
- [The Art of Unix Programming](http://www.catb.org/esr/writings/taoup/html/) — Simplicity, clarity, and the Unix philosophy.

### Quotes That Capture TigerStyle

> "Simplicity and elegance are unpopular because they require hard work and discipline to achieve." — Edsger Dijkstra

> "The design is not just what it looks like and feels like. The design is how it works." — Steve Jobs

> "The right tool for the job is often the tool you are already using—adding new tools has a higher cost than many people appreciate." — John Carmack

## Tools & Linters

### For Zig

- [zig fmt](https://ziglang.org/documentation/master/#zig-fmt) — Zig's built-in formatter.
- [ZLS](https://github.com/zigtools/zls) — Zig Language Server for IDE integration.

### General Static Analysis

- [Infer](https://fbinfer.com/) — Static analyzer for finding bugs in code.
- [Coverity](https://scan.coverity.com/) — Static analysis for open source projects.

### Assertion Libraries

- Consider language-specific assertion libraries that support:
  - Compile-time assertions
  - Pre/postcondition contracts
  - Invariant checking

## Style Guidelines Summary

| Aspect | TigerStyle Recommendation |
|--------|--------------------------|
| **Line length** | Hard limit of 100 columns |
| **Indentation** | 4 spaces |
| **Function length** | Ideally under 70 lines |
| **Assertions** | Minimum 2 per function |
| **Naming** | `snake_case`, no abbreviations |
| **Units in names** | Put last, e.g., `latency_ms_max` |
| **Dependencies** | Zero (apart from language toolchain) |
| **Memory allocation** | Static only, no runtime allocation |
| **Control flow** | Simple, explicit, no recursion |

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related rights to this work.
