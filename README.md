# Hide Player Titles Script

A lightweight Roblox script that hides player titles, nametags, and UI elements above player heads. Optimized for both mobile and PC platforms with smooth animations.

## Features

- 🎮 **Cross-Platform Support** - Optimized for both mobile and PC devices
- 👁️ **Toggle Button** - Easy-to-use floating button in the top-right corner
- ✨ **Smooth Animations** - Icon rotation and pulse effects on interaction
- 🔄 **Auto-Update** - Automatically hides titles for new players
- 🎨 **Visual Feedback** - Color-changing button and status indicator
- ⚡ **Lightweight** - Minimal performance impact, no lag
- 📱 **Haptic Feedback** - Mobile vibration support

## What Gets Hidden

- Player nametags
- Health bars
- BillboardGui elements
- SurfaceGui elements
- TextLabel, TextButton, and TextBox in player heads
- All descendant GUI elements

## Installation

1. Open your Roblox game
2. Access **StarterGui** or **StarterPlayerScripts** in Studio
3. Insert a new **LocalScript**
4. Paste the script content
5. Run the game

## Usage

### Toggle Button
- Click the **eye icon** button in the top-right corner to show/hide player titles
- **Green dot** = Titles are visible
- **Red dot** = Titles are hidden

### Visual Indicators
- **Button glows darker** when titles are hidden
- **Icon becomes faded** when titles are hidden
- **Red cross line** appears on the icon when hidden

### Animations
- Icon rotates 360° smoothly when toggling
- Status dot pulses 3 times for visual feedback
- Button scales on hover (PC only)
- Button compresses on click

## Customization

### Button Position
Edit line 18-19 to change button position:
```lua
local buttonPosition = isMobile and UDim2.new(1, -40, 0, 60) or UDim2.new(1, -40, 0, 60)
```

### Button Size
Edit line 15-16:
```lua
local buttonSize = isMobile and UDim2.new(0, 35, 0, 35) or UDim2.new(0, 32, 0, 32)
```

### Animation Duration
Edit line 98:
```lua
animateIconRotation(0.6)  -- Change 0.6 to desired duration in seconds
```

### Colors
Modify RGB values for:
- Button background: Line 26
- Hidden state color: Line 187
- Active state color: Line 184
- Status dot colors: Lines 188-189

## Platform Detection

The script automatically detects the platform:
- **Mobile**: Smaller button, no hover animations, haptic feedback enabled
- **PC**: Standard size, hover animations, keyboard/mouse optimized

## Performance

- ✅ No continuous loops
- ✅ Optimized event connections
- ✅ Minimal memory usage
- ✅ Efficient descendant scanning
- ✅ Non-blocking async operations

## Troubleshooting

### Button not appearing
- Ensure script is placed in StarterGui or StarterPlayerScripts
- Check that ResetOnSpawn is set to false

### Titles not hiding
- Verify all players have characters loaded
- Check for custom scripts that might override GUI visibility
- Ensure SurfaceGui is supported in your game

### Performance issues
- Reduce the number of players in the game
- Check for conflicting scripts
- Monitor script output for errors

## Requirements

- Roblox Studio or Roblox Game
- LocalScript permissions
- Access to Players service

## Script Size

- **Minified**: ~8 KB
- **Full version**: ~12 KB

## Compatibility

- ✅ All Roblox games
- ✅ Custom game frameworks
- ✅ Multiplayer environments
- ✅ Mobile devices
- ✅ PC devices

## License

This script is free to use and modify for personal projects.

## Support

For issues or suggestions, check the script output in the command bar for debug information.

---

**Version**: 2.0  
**Last Updated**: October 2025  
**Status**: Stable
