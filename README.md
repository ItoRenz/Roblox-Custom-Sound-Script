# Roblox Custom Sound Script

A comprehensive Roblox Lua script that allows players to customize their character's jump and footstep sounds with an intuitive GUI menu system.

## Features

✨ **Custom Sound Selection**
- Jump sound customization (UNYAH button)
- Multiple walk sound options:
  - SQUID (Default Squid sound)
  - SPONGEBOB (SpongeBob walk sound)
  - MR. KRAB (Mr. Krabs walk sound)

🎵 **Smart Sound Management**
- Toggle custom sounds on/off with the OFF button
- Default character sounds automatically activate when custom sounds are disabled
- Toggle individual jump sound independently
- Smooth fade-in/out transitions between custom and default sounds

💾 **Persistent Settings**
- All settings are saved and restored after respawn or death
- Selected walk sound persists across character deaths
- Button states remain unchanged

🎮 **User-Friendly Interface**
- Clean, responsive menu panel
- Color-coded buttons (Green = Active, Red = Inactive)
- Smooth tween animations and hover effects
- Mobile and PC compatible
- Non-draggable button on PC for stability

⚙️ **Optimized Performance**
- Efficient event handling
- Proper cleanup on character death
- Memory-safe sound management
- No performance impact on gameplay

## Installation

1. **Create a LocalScript** in `StarterPlayer > StarterCharacterScripts` or `StarterPlayer > StarterPlayerScripts`
2. **Copy the entire script** from the source code
3. **Paste it into the LocalScript**
4. **Play the game** and enjoy!

## How to Use

### Main Toggle Button 👣
- Click the footstep button in the top-left corner to open/close the menu panel
- Button color changes to green when menu is open

### Menu Options

**UNYAH Button** - Toggle jump sound on/off
- Green = Jump sound enabled
- Red = Jump sound disabled (default sound will play)

**SQUID Button** - Select Squid walk sound
- Green = Currently active
- Red = Inactive

**SPONGEBOB Button** - Select SpongeBob walk sound
- Green = Currently active
- Red = Inactive

**MR. KRAB Button** - Select Mr. Krabs walk sound
- Green = Currently active
- Red = Inactive

**OFF Button** - Toggle all custom sounds
- Green = All custom sounds OFF (default sounds active)
- Red = All custom sounds ON (custom sounds active)
- When OFF is active, other buttons are disabled for better control

## Sound IDs

| Sound | ID |
|-------|-----|
| Jump | `rbxassetid://115680913237541` |
| Squid Walk | `rbxassetid://6929242058` |
| SpongeBob Walk | `rbxassetid://5948749731` |
| Mr. Krabs Walk | `rbxassetid://3426632334` |

## Customization

To add your own sounds, modify the sound ID variables at the top of the script:

```lua
local JUMP_ID = "rbxassetid://YOUR_JUMP_SOUND_ID"
local WALK_ID = "rbxassetid://YOUR_WALK_SOUND_ID"
local SPONGEBOB_WALK_ID = "rbxassetid://YOUR_SOUND_ID"
local MRKRAB_WALK_ID = "rbxassetid://YOUR_SOUND_ID"
```

Then create corresponding buttons following the existing button creation pattern.

## Credits

- **Original Creator**: Bangyan
- **Custom by**: ItoRenz00

## License

This script is protected by Bangyan. Please maintain proper attribution if you modify or redistribute this script.

## Support

If you encounter any issues:
1. Ensure the script is placed in the correct location
2. Check that all sound IDs are valid
3. Make sure your game has sound enabled
4. Verify the script has proper permissions

## Version History

**v1.0** (Current)
- Initial release with full feature set
- 4 walk sound options
- Persistent settings
- Mobile and PC support
