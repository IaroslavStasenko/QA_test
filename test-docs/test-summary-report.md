# DemoShop Test Summary Report

## Execution Summary

| Metric | Result |
|---|---:|
| Total test cases | 16 |
| Passed | 13 |
| Failed | 3 |
| Blocked | 0 |
| Pass rate | 81.25% |
| Open defects | 3 |

## Defect Summary

| Defect | Severity | Priority | Related test | Status |
|---|---|---|---|---|
| BUG-001 — Invalid login email accepted | Medium | Medium | TC-003 | Open |
| BUG-002 — Cart total not updated after quantity change | High | High | TC-008 | Open |
| BUG-003 — Duplicate order on double click | Critical | High | TC-015 | Open |

## Assessment

The basic login, catalogue and most cart/checkout flows behave as expected in the fictional test scenario. However, the current build should **not be considered ready for a production-style release** because BUG-003 affects transaction integrity and BUG-002 can display an incorrect cart total.

BUG-001 should also be corrected, but it is less urgent than the transaction-related defects.

## Recommended Next Steps

1. Fix duplicate-order handling and verify backend idempotency.
2. Fix cart recalculation after quantity changes.
3. Correct email validation and retest both client- and server-side behaviour.
4. Run focused regression tests around cart and checkout.
5. Re-execute failed test cases and update defect status.

## Regression Focus

After fixes, regression should cover:

- Add/remove cart operations
- Quantity boundaries
- Cart and checkout total consistency
- Single and repeated order submission
- Checkout validation
- Order confirmation and reference generation

> All results are part of a synthetic QA portfolio exercise based on fictional requirements.
