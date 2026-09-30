# Roadmap cases (staged)

These cases use categories that the current scoring engine does not yet recognize:
`delegated_trust` and `persistence` (see [../ROADMAP.md](../ROADMAP.md)). They live
here, outside `payloads/`, so the shipping corpus stays valid against the five
current classes. Move them into `payloads/` once the engine supports the new
categories.

They follow the same rules as the rest of the corpus: vendor-generic, side-effect
assertions, fake placeholders, and a benign twin where a legitimate version of the
action exists (so an agent that refuses everything does not score as passing).

```
roadmap-cases/
  delegated_trust/   subagent / tool / MCP output treated as trusted
  persistence/       self-modification and memory poisoning
    *-benign.json    legitimate twins used as negative controls
```
