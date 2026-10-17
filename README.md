# Alpha-Gate Lab

**Executable browser companion for `alpha-axis/0.1`**  
**Author:** K. Lunina · Apache-2.0 · vendor-neutral · no telemetry

[Open the specification, corpus, reference verifier, reference-record fixture,
and implementation-run index](https://github.com/KarinLuni/accountability-axis).

Alpha-Gate Lab makes the accountability axis (α) executable in a browser. It
answers the question that a conventional approval control does not answer:
when an AI-mediated action creates an obligation, is a natural person on record
as the party to that obligation?

## Use

Open `index.html` locally or publish this directory as a static site. It has no
server, dependency, external script, network request, or telemetry.

The delivered page necessarily contains the readable JavaScript engine and the
95 embedded base vectors needed for an interactive, self-contained Lab. This
repository intentionally ships the browser page only; it does not include a
separate development, build, or test package.

## Working views

The page uses real tab panels rather than links into one long document.

| Tab | Purpose |
|---|---|
| **Overview** | Business entry point: approval versus accountable-party status, the separate κ and α questions, and links to exact technical evidence. |
| **Try an action** | Composes one action from business questions and shows the decision record. |
| **Check a workflow** | Evaluates plan-stage establishment and the independent κ / α folds of a chain. |
| **Evidence · 95 cases** | Filters and opens the unchanged base test corpus. |
| **Audit records** | Audits a pasted or dropped implementation decision-record file locally. |
| **Rules & limits** | Shows the evidence states, rule coverage, AISVS relation, and stated limits. |

The Overview’s demonstrations only load existing inputs into the same engine;
they are not a second, simplified decision model.

## Integrity checks in the page

At load, the page:

1. executes all 95 embedded base cases;
2. recomputes the SHA-256 hash of the embedded vector files; and
3. compares the records it produces with the released
   `examples/reference-records.json` fixture.

The header reports those checks. The Python reference verifier in the main
repository remains the reference semantics if a difference is ever found.

## Scope

This Lab is a reference artefact, not a product, legal opinion, κ grader, or
claim about a third-party implementation. The audit view assesses records that
are supplied to it; it does not establish that a production runtime enforced
them.

## License

Apache-2.0. See `LICENSE` and `NOTICE`.
