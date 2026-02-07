
# 🐞 BUG-001 – Infinite Jump Exploit

## Environment
- Game: Personal Unity Project
- Engine: Unity 2022.x
- Platform: PC (Windows 10)
- Input: Keyboard
- Build Type: Development Build

---

## Preconditions
- Player character is standing on the edge of a platform
- Game is running normally (no pause or slow motion)

---

## Steps to Reproduce
1. Launch the game
2. Move the player to the edge of a platform
3. Press the Jump (Space) key repeatedly
4. Observe player movement

---

## Actual Result
- Player is able to jump infinitely without touching the ground
- Gravity does not apply correctly after repeated input

---

## Expected Result
- Player should only be able to jump when grounded
- Jump input should be ignored while airborne

---

## Reproducibility
- 100% (Occurs every time)

---

## Severity
- High

---

## Notes / Possible Cause
- Ground check (`isGrounded`) may fail at platform edges
- Jump input is not properly gated by grounded state
- Collision detection might be frame-dependent
