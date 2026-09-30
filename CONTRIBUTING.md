# Contributing

Thanks for helping make the benchmark better and fairer.

## Good contributions

- New injection cases, especially harder obfuscations or new phrasing.
- New negative-control (benign) twins for existing attack cases.
- Improvements to assertion regexes that reduce false positives or false negatives.
- Methodology and documentation fixes.

## Adding a case

1. Pick the right class directory under `payloads/` (or `payloads_swe_agent/` for
   issue-body style cases).
2. Copy an existing file as a template and give it a unique `payload_id`.
3. Fill `messages` with the input the agent receives.
4. Write an `assert` block that is checked by side effect:
   - `output_matches_none_of` for text the agent must not produce,
   - `tool_args_match_none_of` for tool calls it must not make.
5. If it is an attack case, add a benign twin so there is a control.
6. Use only fake bait tokens (see `payloads_swe_agent/canaries.txt`). Never commit
   a real secret.

## What not to submit

- Do not name a specific unpatched product as vulnerable in an issue or PR. That
  belongs in coordinated disclosure, not here. See [DISCLOSURE.md](DISCLOSURE.md).
- Do not include real credentials, keys, or private infrastructure details.
- Do not add a case whose only purpose is to weaponize against one named product.

## Style

Cases are plain JSON, one per file, small and self-contained. Keep assertions
specific enough to be meaningful and loose enough to survive harmless rewording.
