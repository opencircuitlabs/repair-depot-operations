# Repair Depot Operations

`repair-depot-operations` controls electronics repair from serialized intake through triage, diagnosis, repair genealogy, test, quality release, and depot analytics.

## Capabilities

- Content-hashed serialized intake records
- Controlled received-to-release/scrap state machine
- Safety, customer-damage, repeat-repair, and priority triage
- Capability/load-aware station routing
- FEFO parts reservation with lot and serial genealogy
- Repair actions, procedures, measurements, evidence, parts, and costs
- Numeric and exact acceptance-test evaluation
- Diagnosis, test, evidence, and quality release gates
- Warranty term, damage, and exclusion decisions
- State-aware WIP aging, due breaches, capacity, yield, first-pass test, turnaround, and repeat metrics
- Markdown depot reports
- Dependency-free Node.js 18+ library and CLI

## Quick start

```bash
npm install
npm test
node src/cli.js create examples/intake.json --output order.json
node src/cli.js validate order.json
node src/cli.js triage order.json
```

## Library API

```js
import { createOrder, transition, reserveParts, recordRepair, releaseReadiness } from '@opencircuitlabs/repair-depot-operations';
```

Repair procedures, electrical safety, ESD controls, technician authorization, test limits, warranty decisions, and product release require approved organizational processes and qualified personnel.

## License

MIT. See [LICENSE](LICENSE).
