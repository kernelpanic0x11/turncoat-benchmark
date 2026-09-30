# Disclosure policy

TURNCOAT is a benchmark, not an exploit release. The distinction matters because
the cases here can reveal real, unpatched weaknesses in real products.

## What is in this repository

- Generic, vendor-agnostic test cases for prompt-injection resistance.
- Scoring rules and methodology.
- Canary tokens that are deliberately fake bait, not real secrets.

## What is not, and will not be, in this repository

- Working exploits targeting a specific unpatched product.
- Writeups of vulnerabilities that are still under coordinated disclosure.
- Any real credential, key, or private infrastructure detail.

## How findings are handled

When running TURNCOAT against a real product reveals a genuine failure:

1. It is reported privately to the vendor first, through their security channel
   (VDP, security advisory, or security contact).
2. It stays private until the vendor ships a fix or the coordinated timeline
   completes.
3. Only then is the specific product named in any public result.

Products that **defended** against the cases, or that have already **shipped a
fix**, may be named immediately. Products that are currently vulnerable are shown
in aggregate only until it is safe for their users.

## Reporting

If you use this corpus and find a real weakness in a product, please practice the
same coordinated disclosure: contact the vendor privately first. Do not file it as
a public issue or PR here.

If you believe a case in this repo itself leaks something it should not (a real
secret, a real vulnerability writeup), please report it privately rather than
opening a public issue.
