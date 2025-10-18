# Sound Toggle System for Roblox

A comprehensive sound effects management system for Roblox that allows players to toggle jump and walk sound effects with an elegant, compact UI.

## Features

### 🎵 Sound Effects
- **UNYAH Sound** - Custom jump sound effect with spam protection
- **SQUID Sound** - Walk/footstep sound effect that syncs with movement
- Smooth sound management with proper state handling

### 👣 User Interface
- **Compact Toggle Button** - Minimalist 32x32px (PC) / 36x36px (Mobile) button
- **Pop-up Menu Panel** - Clean menu with UNYAH and SQUID toggles
- **Color-coded Status** - Green (ON) / Red (OFF) visual feedback
- **Responsive Design** - Optimized for both PC and Mobile platforms

### ✨ Animations & Effects
- Logo rotation animation on button click (20° rotation)
- Smooth color transitions with tween animations
- Hover effects on menu buttons (transparency change)
- No gameplay obstruction - fully minimalist design

### 📍 Positioning
- Fixed position at top-left corner (10px padding)
- Menu panel positioned beside the toggle button
- Draggable on PC (when menu is closed)
- Touch-friendly sizing on mobile devices

## Installation

### For Roblox Studio

1. **Open your game** in Roblox Studio
2. **Locate** `StarterPlayer > StarterCharacterScripts` or `StarterPlayer > StarterPlayerScripts`
3. **Insert a new LocalScript**
4. **Paste the entire script** into the LocalScript
5. **Test your game** - The UI should appear at the top-left corner

### Requirements
- Roblox game place
- LocalScript execution environment
- Access to player's PlayerGui

## Usage

### Toggle Button (👣)
- **Click** to open/close the menu panel
- **Animation** - Logo rotates 20° when clicked
- **Color Change** - Highlights when menu is open

### UNYAH Button (Jump Sound)
- **Click** to toggle jump sound ON/OFF
- **Green** = Sound enabled
- **Red** = Sound disabled
- **Affects** only jump actions

### SQUID Button (Walk Sound)
- **Click** to toggle walk sound ON/OFF
- **Green** = Sound enabled
- **Red** = Sound disabled
- **Affects** only walking/movement

## Configuration

### Customize Sound IDs

Edit the ID values in the script:

```lua
local JUMP_ID = "rbxassetid://115680913237541"  -- Change to your jump sound
local WALK_ID = "rbxassetid://6929242058"       -- Change to your walk sound
```

### Adjust Button Position

Modify the position in the script:

```lua
toggleContainer.Position = UDim2.new(0, 10, 0, 10)  -- X: 10px, Y: 10px from top-left
```

### Change Button Size

Adjust sizes for different screen scales:

```lua
-- PC Size
toggleContainer.Size = UDim2.new(0, 32, 0, 32)

-- Mobile Size
toggleContainer.Size = UDim2.new(0, 36, 0, 36)
```

## Technical Details

### Sound Management
- Minimum jump interval: 50ms (spam prevention)
- Walk sound loops automatically while moving
- Sounds stop when jumping or falling
- Auto-resume walk sound after landing

### Platform Detection
```lua
local isMobile = UserInputService.TouchEnabled and not UserInputService.KeyboardEnabled
```

### State Tracking
- `jumpEnabled` - Toggle jump sound status
- `walkEnabled` - Toggle walk sound status
- `isWalking` - Current walking state
- `isJumping` - Current jumping state
- `menuOpen` - Menu panel visibility

## Responsive Breakpoints

### PC (Desktop)
- Button Size: 32x32px
- Button Icon Size: 18
- Menu Size: 86x62px
- Menu Button Height: 22px
- Menu Button Text Size: 9

### Mobile
- Button Size: 36x36px
- Button Icon Size: 20
- Menu Size: 100x72px
- Menu Button Height: 26px
- Menu Button Text Size: 10

## Colors

| Element | Color | RGB |
|---------|-------|-----|
| Toggle Button (Normal) | Blue | (52, 152, 219) |
| Toggle Button (Menu Open) | Green | (46, 204, 113) |
| Menu Background | Dark Gray | (44, 62, 80) |
| Menu Button (ON) | Green | (46, 204, 113) |
| Menu Button (OFF) | Red | (231, 76, 60) |
| Button Background (Hover) | Dark Slate | (52, 73, 94) |

## Events & Callbacks

### Jump Sound
- Triggered on humanoid jump
- Respects jump interval limit
- Stops previous sound before playing new one

### Walk Sound
- Triggered when speed > 2 studs/second
- Only plays on ground (not in air)
- Automatically stops on jump

### Character Respawn
- Cleans up old sounds
- Recreates sound instances
- Reconnects all event handlers
- Closes menu panel

## Browser Storage Restriction

⚠️ **Note**: This script uses in-memory state only. No localStorage or sessionStorage is used as they are not supported in Claude.ai artifacts. For persistent data, implement custom save system.

## Credits

- **Original Concept**: Bangyan © 2025
- **Enhancements**: Sound management & UI optimization
- **Platform Support**: PC & Mobile optimized

## Troubleshooting

### Sounds Not Playing?
1. Check sound IDs are valid
2. Verify audio is enabled in Roblox settings
3. Check humanoid state for Jump/Walk

### UI Not Appearing?
1. Ensure LocalScript is in correct location
2. Check PlayerGui accessibility
3. Verify screen resolution is adequate

### Animation Not Working?
1. Check TweenService availability
2. Verify Enum.EasingStyle is supported
3. Test on supported Roblox client version

## License

This script is provided as-is for use in Roblox games. Maintain credit to original creator.
