# Contributing

Thanks for your interest in improving this Nabi library.

## Development

```sh
nabi test          # tests, in tests/
nabi bench         # benchmarks, in benches/
nabi fmt --check   # formatting
```

Tests live in `tests/` and benchmarks in `benches/`; both reach the package
through `pkg::`. Format before sending a change (`nabi fmt`).

## Generated files

- `tests/snapshots/`: byte-exact SVG and terminal output. After a deliberate
  change to the output, `PLOT_BLESS=1 nabi test` rewrites them; review the
  diff.
- `assets/*.svg`: the README's images, from `nabi run tools/gallery`.
- `src/font/glyphs.nabi`: outlines of the built-in font, from
  `python3 tools/font.py <Geist-Variable.woff2> <pretendard dir>`
  (needs `fonttools` and `brotli`).
- `src/colormap/tables.nabi`: colormap data, from
  `python3 tools/colormaps.py` (reads matplotlib's data modules).

## Changes that affect behavior

Update the README (its examples, and the API table where there is one)
alongside any change in behavior, and add a test for new behavior.

## Submitting

Open a pull request against `main` with `nabi test` and `nabi fmt --check`
passing. By contributing you agree that your work is licensed under both MIT and
Apache-2.0, the project's dual license.

## Sign your work

Nabi uses the [Developer Certificate of Origin 1.1](https://developercertificate.org/)
(DCO) instead of a CLA. By adding a `Signed-off-by` line to a commit you
certify that you wrote the change, or otherwise have the right to submit it
under this repository's license. `git commit -s` adds the line:

```text
Signed-off-by: Your Name <you@example.com>
```

Use your name and an email you can be reached at; the email must be the
commit's author email. The `DCO / Check sign-off` check fails a pull request with an
unsigned commit. To fix it, run `git commit --amend -s` (last commit) or
`git rebase --signoff main` (every commit), then push again. The full text
of the DCO is in the
[organization's CONTRIBUTING.md](https://github.com/nabi-lang/.github/blob/main/CONTRIBUTING.md#developer-certificate-of-origin).
