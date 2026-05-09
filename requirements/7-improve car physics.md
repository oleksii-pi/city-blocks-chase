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
   - Ensure that each car sprite is rendered according to its movement vector and direction, accurately reflecting the speed and direction of movement. When a car moves backward, the car sprite should be rendered accordingly, not reverting itself. There are instances when I hit a car, and the car sprite changes angle very frequently. Instead, each car should have more stable physical stability and should not suddenly change its angle of direction. When a police car performs a turnaround, the physics are also unrealistic. It stays in a single point and suddenly changes direction. Instead, it should have corresponding physics of movement, and the turnaround should look realistic.

Make sure these changes enhance the overall driving experience and realism in the game.
