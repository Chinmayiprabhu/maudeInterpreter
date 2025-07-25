# PAOL Interpreter

A Maude interpreter for PAOL (Privacy-Aware Active Object Language) with privacy enforcement.

## Files

- `Interprter-PAOL.maude` - Main PAOL interpreter
- `workingconf.maude` - Hospital management example (non-violating)
- `violation-example.maude` - Marketing violation example (violating)
- `test-hygienic.maude` - Test hygienic program
- `test-violation-example.maude` - Test violation program

- `OUTPUT-ANALYSIS.md` - Output analysis

## Examples

### Non-Violating Example (Hospital)
Hospital management system with proper consent:
```bash
../Maude-3.5-macos-x86_64/maude test-hygienic.maude
```

### Violating Example (Marketing)
Marketing tries to access data without consent:
```bash
../Maude-3.5-macos-x86_64/maude test-violation-example.maude
```

## Privacy Enforcement

The interpreter enforces privacy through:
- Tag-based access control
- User consent management
- Purpose-based restrictions
- Runtime privacy checks

## Test Results

| Example | Type | Status | Result |
|---------|------|--------|--------|
| Hospital | Non-Violating | PASS | Runs successfully |
| Marketing | Violating | PASS | Blocked by privacy |

The interpreter correctly handles both examples with proper privacy enforcement.
