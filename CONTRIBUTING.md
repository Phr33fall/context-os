# Contributing

ContextOS is an early reference implementation.

Issues, questions, and practical feedback are welcome.

Pull requests may be reviewed selectively. The project is intentionally small, so changes should preserve the core idea:

- clear source-of-truth boundaries
- durable handovers
- restricted material excluded by default
- tool-agnostic workflows
- simple enough to use in real sessions

## Before Opening A Pull Request

Please make sure the change:

- does not include private data, local paths, hostnames, IP addresses, credentials, or restricted material
- keeps examples generic and reusable
- improves the operating model rather than adding unnecessary complexity
- updates `README.md`, templates, or docs when behaviour changes

## Good Contributions

- clearer setup instructions
- safer handover patterns
- better source-of-truth map examples
- improvements to the safety model
- examples for other AI tools or knowledge systems

## Not A Fit

- vendor-specific lock-in
- broad automation that reads everything by default
- examples containing real private work
- changes that make ContextOS harder to understand or adopt
