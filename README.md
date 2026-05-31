# 2025-TC
Github repo for the paper submitted at IEEE Transactions on Computers.

## Upstream contributions

The following fixes were authored by [@jacopobellosi](https://github.com/jacopobellosi) and merged into the paper's official repository ([paper-codes/2025-TC](https://github.com/paper-codes/2025-TC)) via [PR #1](https://github.com/paper-codes/2025-TC/pull/1):

- **FIX symmetric reflection A/B** — both reflections inside the QPE `compute()` block now act on the full coin register instead of half of it.
- **FIX index out of range in walk loops** — prevents `IndexError` when `k <= 2` or `n-k <= 2` by using the actual allocation sizes.
- **MOD len_s minimum from 1 to 2** — prevents a degenerate QPE register when the spectral gap formula yields `len_s <= 1`.

All the subroutines are part of the `qat-utils` repo, available [here](https://github.com/tigerjack/qat-utils).

To run the code, you should install `myqlm`, availabel [here](https://myqlm.github.io/).

You can run all the tests for the given quantum routines using

```shell
REVERSIBLE_ON=1 pytest -s
```
