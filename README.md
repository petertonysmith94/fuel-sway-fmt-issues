# Sway Fmt

Ran into some odd behaviour with forc fmt  with the latest release `0.66.6`. For the most part all looks good, but some files it looks like all the whitespace has been stripped.

This is a minimal reproduction of the issue.

1. Run `forc fmt`

```console
forc fmt
```

2. See results in Git diff

## Example sources

Example 1: https://github.com/FuelLabs/fuels-ts/blob/e5251e230f3cbd3677d556e0e660c86281d48315/apps/docs/sway/liquidity-pool/src/main.sw
Example 2: https://github.com/FuelLabs/fuels-ts/blob/e5251e230f3cbd3677d556e0e660c86281d48315/packages/fuel-gauge/test/fixtures/forc-projects/options/src/main.sw
Example 3: https://github.com/FuelLabs/fuels-ts/blob/e5251e230f3cbd3677d556e0e660c86281d48315/packages/fuel-gauge/test/fixtures/forc-projects/revert-error/src/main.sw
Example 4: https://github.com/FuelLabs/fuels-ts/blob/e5251e230f3cbd3677d556e0e660c86281d48315/packages/fuel-gauge/test/fixtures/forc-projects/script-with-more-configurable/src/main.sw

[Reference commit](https://github.com/FuelLabs/fuels-ts/pull/3617/commits/a83a33e0ab378159f6b2e36858f749329450f0e2#diff-82ed4c3fb1a34871c63a47ee72a68bde66362ef56a7b57c087a49c4f7d233aa0)