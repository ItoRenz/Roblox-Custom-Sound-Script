# Roblox Custom Sound Script

A customizable sound replacement script for Roblox that allows players to change their jump and walking sounds with a user-friendly GUI.

## 🎵 Features

- **Custom Jump Sounds**: Replace default jump sound with custom audio
- **Multiple Walk Sound Options**:
  - Squidward Walk
  - SpongeBob Walk
  - Mr. Krabs Walk
- **Mobile-Friendly**: Responsive GUI that works on all devices
- **Persistent Settings**: Your preferences save across respawns
- **Smooth Animations**: Professional UI transitions and effects
- **Easy Toggle**: Quick access button with expandable menu
- **Default Sound Override**: Automatically disables default Roblox sounds when custom sounds are active

## 📋 Requirements

- Roblox game environment
- LocalScript execution (client-side)
- Audio asset permissions

## 🚀 Installation

1. Copy the entire script from `sound_script.lua`
2. Paste it into a LocalScript in your Roblox game
3. Place the LocalScript in:
   - `StarterPlayer` > `StarterCharacterScripts`, or
   - `StarterPlayer` > `StarterPlayerScripts`

## 🎮 Usage

### In-Game Controls

1. **Main Button** (👣): Click to open/close the sound menu
2. **UNYAH**: Toggle custom jump sound on/off
3. **SQUID**: Use Squidward walking sound
4. **SPONGEBOB**: Use SpongeBob walking sound
5. **MR. KRAB**: Use Mr. Krabs walking sound
6. **OFF**: Disable all custom sounds (restore default Roblox sounds)

### Button Colors

- **Green**: Active/Enabled
- **Red**: Inactive/Disabled

## 🔧 Customization

### Changing Sound IDs

Locate this section in the script:

```lua
local JUMP_ID = "rbxassetid://115680913237541"
local WALK_ID = "rbxassetid://6929242058"
local SPONGEBOB_WALK_ID = "rbxassetid://5948749731"
local MRKRAB_WALK_ID = "rbxassetid://3426632334"
```

Replace the asset IDs with your own Roblox audio asset IDs.

### Adjusting GUI Position

To change the button position, modify:

```lua
toggleContainer.Position = UDim2.new(0, 10, 0, 10)
```

Change the `10, 10` values to move the button (X offset, Y offset).

### Button Size

To adjust button size:

```lua
toggleContainer.Size = UDim2.new(0, 32, 0, 32)
```

## 🛠️ Technical Details

### Sound Management

- Custom sounds automatically override default Roblox sounds
- Walking sounds loop seamlessly while moving
- Jump sounds play with debounce to prevent spam
- Sounds stop appropriately during jumping/falling states

### State Persistence

The script saves these settings across respawns:
- Jump sound enabled/disabled
- Current walk sound selection
- All sounds enabled/disabled state

### Performance Optimization

- Efficient event handling with proper cleanup
- Smooth animations using TweenService
- Minimal overhead with Heartbeat connection for sound monitoring

## 📝 Code Structure

```
├── Player References
├── Sound IDs Configuration
├── Script Protection
├── Default Sound Management
├── Custom Sound Setup
├── State Variables
├── Event Handlers
│   ├── Jump Handler
│   ├── Walk Handlers
│   └── State Change Handler
├── GUI Creation
│   ├── Toggle Button
│   ├── Menu Panel
│   └── Menu Buttons
├── Button Events
├── Hover Effects
├── Respawn Handler
└── Cleanup Functions
```

## 🐛 Troubleshooting

### Sounds Not Playing

1. Verify audio asset IDs are correct and published
2. Check audio privacy settings (must be public or group-accessible)
3. Ensure script is in correct location (LocalScript in character)

### GUI Not Appearing

1. Verify the script is running on the client
2. Check that PlayerGui is accessible
3. Ensure no other scripts are interfering

### Sounds Continue After Death

This is expected behavior. The script properly handles respawns and reconnects all events.

## 📜 Credits

- **Original Script**: Bangyan © 2025
- **Customization**: ItoRenz00
- **Sound Assets**: Various SpongeBob SquarePants audio sources

## 📄 License

This script is protected by its original author. Please maintain credit headers when sharing or modifying.

## 🤝 Contributing

When contributing improvements:

1. Maintain code formatting and structure
2. Keep credit headers intact
3. Document any new features
4. Test on both desktop and mobile platforms

## ⚠️ Disclaimer

This script is for educational and entertainment purposes. Ensure you have proper permissions for any audio assets used.

## 📞 Support

For issues or questions:
- Check the Troubleshooting section
- Review code comments for implementation details
- Test with default sound IDs first to verify functionality

---

**Version**: 1.0  
**Last Updated**: 2025  
**Compatibility**: Roblox (Current Version)
