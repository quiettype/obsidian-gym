---
date_created: 2025-11-02
---

# Suggested Changes for Obsidian Gym

## Display Improvements
1. **Volume Calculation Display**: Round volume numbers in the Performed Exercises table
   - Current: Shows unnecessary decimal places (e.g., "28.799999999999997 kg×reps")
   - Proposed: Round to 1 decimal place (e.g., "28.8 kg×reps")
   - Implementation: Added toFixed(1) to volume calculation
   - Location: In workout.js, renderPerformed method
   - Status: ✅ Implemented

## Bug Fixes
1. **Tag Handling**: Improved tag handling compatibility
   - Current: Code assumes tags include # prefix
   - Issue: Some code paths receive tags without # prefix
   - Fix: Remove # prefix assumption, handle both formats
   - Implementation: Strip # from tags before comparison
   - Status: ✅ Implemented

## Process for Changes
1. Test current functionality thoroughly first
2. Document any issues found
3. Implement changes after verification of stable operation