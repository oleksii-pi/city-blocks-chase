### Improvements to Car Physics:

1. **Movement Constraints**:
   - Cars should not be able to move at a speed of 0. Movement is only possible when the car has a positive speed.

2. **Realistic Speed Limits**:
   - The maximum speed for player-controlled cars should be set to 100 (this value should be configurable).
   - The maximum speed for police cars should be set to 80 (this value should also be configurable).
   - The speed for regular cars should be set to 50 (configurable as well).

3. **Chasing Behavior Fix**:
   - Address the issue where police cars often turn around at intersections while chasing the player. The turning should be smooth and follow realistic physics rather than abrupt changes.

4. **Sprite Rendering**:
   - Ensure that each car sprite is rendered according to its movement vector and direction, reflecting the direction and speed of movement accurately. When car moves back, car sprit should be rendered accordingly, not reverting itself.

Make sure these changes enhance the overall driving experience and realism in the game.
