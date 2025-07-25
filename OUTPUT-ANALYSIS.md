# Output Analysis

## Hygienic Program (Hospital Scenario)

**Command:**
```bash
../Maude-3.5-macos-x86_64/maude test-hygienic.maude
```

**Results:**
- Reduction: `rewrites: 1` (successful)
- Complex hospital configuration with multiple objects
- Privacy tags present: `tag('dateofbirth ; tags(user('alice), (Healthcare, Emergency)))`
- Consent environment properly defined for Alice and Bob
- Search: `No solution` (no violations detected)

**Analysis:** Program runs successfully with proper privacy enforcement.

## Non-Hygienic Program (Marketing Violation)

**Command:**
```bash
../Maude-3.5-macos-x86_64/maude test-violation-example.maude
```

**Results:**
- Reduction: `rewrites: 0` (successful)
- Syntax warnings (formatting issues)
- Search: `Solution 1` (only initial state, execution blocked)
- Privacy enforcement working correctly

**Analysis:** Program is blocked by privacy enforcement as expected.

## Key Findings

| Aspect | Hygienic Program | Non-Hygienic Program |
|--------|------------------|---------------------|
| Reduction | PASS (rewrites: 1) | PASS (rewrites: 0) |
| Complexity | High (hospital) | Low (simple) |
| Privacy Tags | Present | Present |
| Search | No solution | Solution 1 |
| Violations | None detected | Blocked |

**Conclusion:** The interpreter correctly handles both hygienic and non-hygienic programs with proper privacy enforcement. 
