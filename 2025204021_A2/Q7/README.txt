Q7 - Bowling Alley Game (Three.js)
===================================

OBJECTIVE:
Implement a 3D bowling alley game using Three.js with proper bowling rules including:
- Strike and spare detection
- 10-frame scoring system with bonus balls
- Realistic physics and collision detection
- Interactive controls for power, direction, and spin
- Sound effects and camera system
- Achievement tracking

FILES:
- bowling_game.html - Complete 3D bowling game implementation

GAME FEATURES:

1. 3D GRAPHICS (THREE.JS)
   - Realistic bowling lane with procedurally generated wood texture
   - 3D bowling ball with finger holes and rotation physics
   - 10 bowling pins with proper positioning (triangular formation)
   - Enhanced lighting: ambient, directional, and 2 spotlights
   - Shadow mapping for depth perception
   - Fog effect for atmosphere
   - Red and white striped pin design with neck detail
   - Direction arrows painted on lane
   - Gold/blue frame highlighting for strikes/spares

2. PHYSICS ENGINE
   - Ball velocity and angular velocity
   - **Spin mechanics**: adjustable spin (-50 to +50) affects ball curve
   - Friction simulation (ball slows down naturally)
   - Collision detection (ball-to-pin and pin-to-pin)
   - **Pin wobble**: pins wobble before falling for suspense
   - Pin knockdown animations with rotation
   - Boundary detection (gutters/walls)
   - Chain reaction physics (pins knocking other pins)
   - Refined collision thresholds (ball: 0.55, pin-to-pin: 0.45)

3. GAME CONTROLS
   - Power slider (20-100%) with green→yellow→red gradient
   - **Spin slider (-50 to +50)** for ball curve control
   - Direction buttons (LEFT/RIGHT)
   - Visual power indicator
   - BOWL button to throw
   - NEW GAME button to reset
   - **🔊/🔇 Sound toggle** button
   - **📷 Camera follow mode** toggle

4. SOUND EFFECTS (WEB AUDIO API)
   - Bowl sound when throwing the ball
   - Pin collision sounds (volume based on impact)
   - **Strike celebration**: 3-tone ascending sequence
   - **Spare sound effect**: single high tone
   - Sound toggle to enable/disable all audio
   - All sounds generated procedurally (no external files)

5. CAMERA SYSTEM
   - Default: overhead view (0, 8, -18)
   - **Follow mode**: camera dynamically tracks ball down lane
   - Smooth transitions between positions
   - Toggle with 📷 button during gameplay
   - Automatic return to starting position after throw

6. BOWLING RULES IMPLEMENTED
   ✓ 10 frames per game
   ✓ 2 balls per frame (except 10th frame)
   ✓ Strike detection (all pins on first ball)
   ✓ Spare detection (all pins with two balls)
   ✓ Open frame detection
   ✓ 10th frame bonus rules:
     - Strike: 2 bonus balls
     - Spare: 1 bonus ball
     - Pins reset after strike/spare in 10th frame
   ✓ Proper scoring with strike/spare bonuses:
     - Strike: 10 + next 2 balls
     - Spare: 10 + next 1 ball
     - Open: sum of pins knocked down

7. SCORING DISPLAY
   - Visual scorecard with 10 frames
   - Individual throw display (-, 1-9, X, /)
   - **Color-coded notation**: gold "X" for strikes, blue "/" for spares
   - Cumulative frame scores
   - Total score tracker
   - Current frame and ball indicators
   - Active frame highlighting
   - **Live counters**: strike/spare badges in scoreboard
   - Strike/spare notation:
     - "X" for strikes (gold)
     - "/" for spares (blue)
     - "-" for gutter balls
     - Numbers for pin counts

8. ACHIEVEMENT SYSTEM
   Final score determines achievement message:
   - 300 points: "🏆 PERFECT GAME!"
   - 250-299: "⭐ AMAZING PERFORMANCE!"
   - 200-249: "🔥 EXCELLENT GAME!"
   - 150-199: "👏 GREAT JOB!"
   - 100-149: "👍 GOOD GAME!"
   - Below 100: "🎳 KEEP PRACTICING!"

9. GAME FLOW
   - Automatic frame progression
   - Pin reset between frames
   - Ball return after each throw
   - Visual instructions update in real-time
   - Game over screen with comprehensive statistics
   - Final score display with achievement message
   - Stats grid: total score, strikes, spares, open frames

10. VISUAL POLISH
    - Clean, modern UI matching Q3-Q6 theme
    - Color-coded buttons with gradient effects
    - Primary blue, success green, danger red, purple spin control
    - Smooth animations
    - Responsive layout
    - Glass-morphism effects on UI panels
    - Dark gradient background
    - Professional typography
    - Enhanced shadows and atmosphere

CONTROLS:
1. **Adjust power** using the slider (20-100%)
2. **Adjust spin** using the spin slider (-50 to +50)
   - Negative values = left curve
   - Positive values = right curve
3. **Set direction** using LEFT/RIGHT buttons (fine adjustment)
4. **Toggle sound** with 🔊/🔇 button
5. **Toggle camera** with 📷 button (follow ball mode)
6. Click "🎳 BOWL" to throw the ball
7. Watch the physics simulation
8. Pins are automatically counted after ball stops
9. Game progresses through 10 frames automatically

SCORING EXAMPLES:
Frame 1: Strike (X) → 10 + next 2 balls
Frame 2: 7, 3 (spare /) → 10 + next 1 ball
Frame 3: 5, 2 (open) → 7 points
Frame 10: Special rules for bonus balls

GAME STATISTICS:
- Total score (max 300)
- Number of strikes
- Number of spares
- Number of open frames
- Achievement based on final score

TECHNICAL IMPLEMENTATION:
- Three.js r159 (loaded from CDN)
- Web Audio API for sound effects
- Pure JavaScript (no external physics engine)
- Custom collision detection algorithm
- Distance-based pin knockdown with wobble
- Velocity transfer between objects
- Real-time score calculation
- Frame state management
- 10th frame special handling
- Procedural wood texture generation
- Dynamic camera positioning

PHYSICS DETAILS:
- Ball radius: 0.35 units
- Pin height: 1.2 units
- Lane dimensions: 4×40 units
- Collision threshold: 0.55 units (ball-pin)
- Pin-to-pin collision: 0.45 units
- Friction coefficient: 0.98 (z-axis), 0.99 (x-axis)
- **Spin effect**: lateral force applied continuously during roll
- Angular velocity linked to linear velocity
- Pin wobble threshold: 0.6 units (triggers wobble before fall)
- Wobble damping: gradual stabilization or collapse

CAMERA SETUP:
- Perspective camera (60° FOV)
- Default position: (0, 8, -18)
- Looking at: (0, 0, 10)
- **Follow mode**: lerp-based tracking behind ball
- Smooth transitions with 0.1 interpolation factor

LIGHTING:
- Ambient light (0.4 intensity)
- Directional light with shadows (0.6 intensity, from above-right)
- Spotlight 1: focused on pins (0.8 intensity, gold color)
- Spotlight 2: focused on ball start (0.5 intensity, white)
- Shadow map resolution: 2048×2048

SOUND DESIGN:
- Bowl sound: 200Hz oscillator, 0.3s duration
- Pin collision: 300Hz + random variation, impact-based volume
- Strike celebration: 440Hz → 554Hz → 659Hz sequence
- Spare sound: 523Hz, 0.2s duration
- All sounds use OscillatorNode with gain envelope

BROWSER COMPATIBILITY:
- Chrome, Firefox, Safari, Edge (modern versions)
- Requires WebGL support
- Requires Web Audio API support
- Responsive design (auto-resizes on window resize)

GAMEPLAY NOTES:
- Higher power = faster ball = more pins knocked down
- **Spin creates curved ball path** (hook shots possible)
- Direction affects ball starting angle
- Ball can bounce off gutters (with reduced velocity)
- Pins wobble realistically before falling
- Pins can knock down other pins (chain reactions)
- Realistic pin fall animations
- 1-second delay after ball stops before counting pins
- Sound effects enhance immersion

RULES COMPLIANCE:
✓ Goal: Knock down all 10 pins
✓ Frame structure: 2 balls per frame (standard frames)
✓ Strike: All pins with first ball
✓ Spare: All pins with second ball
✓ 10 frames per game
✓ 10th frame bonus balls (strike = 2 extra, spare = 1 extra)
✓ Open frame tracking
✓ Proper scoring with bonuses
✓ Foul line marked (visual only, not enforced in this version)

ADVANCED FEATURES IMPLEMENTED:
✓ Sound effects with toggle control
✓ Ball spin mechanics
✓ Camera follow mode
✓ Achievement system
✓ Pin wobble physics
✓ Procedural textures
✓ Enhanced lighting
✓ Live statistics display
✓ Color-coded scoring notation

FUTURE ENHANCEMENTS (Not Implemented):
- Multiplayer mode (Traditional Singles/Unified Doubles/Team)
- 3-game average calculation
- Foul line enforcement
- Player statistics tracking across games
- Ball customization (color, weight)
- Different lane conditions (oil patterns)
- Replay system
- Touch controls for mobile
- Leaderboard system

USAGE:
1. Open bowling_game.html in a modern web browser
2. Wait for Three.js scene to load
3. Use controls to set power, spin, and direction
4. Enable sound effects if desired (🔊 button)
5. Try follow camera mode for different perspective (📷 button)
6. Bowl the ball and enjoy the physics simulation
7. Watch for pin wobbles and chain reactions
8. Listen for strike/spare celebration sounds
9. Complete all 10 frames to see final score and achievement
10. Click "Play Again" to start a new game

NOTE:
This is an enhanced bowling simulation with realistic physics, sound effects, and
advanced controls. The spin system allows for hook shots, and the camera system
provides multiple viewing angles. Physics are balanced for playability while
maintaining realism. The game emphasizes fun, visual appeal, proper rule
implementation, and immersive audio-visual feedback.

SPIN CONTROL TIPS:
- Start with 0 spin (center) to learn basic mechanics
- Negative spin (-20 to -50): ball curves left (for left-handed hook)
- Positive spin (+20 to +50): ball curves right (for right-handed hook)
- Combine spin with direction for complex shot angles
- Higher power amplifies spin effect
- Master spin control to hit corner pins and get more strikes!
