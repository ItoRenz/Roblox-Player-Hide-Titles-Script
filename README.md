# 👁️ Hide Player Titles Script

A Roblox LocalScript that allows players to toggle the visibility of overhead titles, nametags, and GUI elements for all players in the game.

## 🎯 Features

- **Toggle Visibility**: Hide/show all player titles, nametags, and overhead GUIs with a single click
- **Cross-Platform**: Optimized for both mobile and PC devices
- **Smooth Animations**: Eye-catching icon rotations and button animations
- **Visual Feedback**: Status indicator dot and cross-line overlay
- **Haptic Feedback**: Mobile devices get haptic feedback on toggle (if supported)
- **Automatic Detection**: Automatically applies to new players joining the game
- **Persistent State**: Maintains visibility state across character respawns

## 📦 Installation

1. Open your Roblox game in Roblox Studio
2. Navigate to `StarterGui` or `StarterPlayerScripts` in the Explorer
3. Insert a new `LocalScript`
4. Copy and paste the script code into the LocalScript
5. Save and test in-game

## 🎮 Usage

Once installed, a toggle button will appear in the top-right corner of the screen:

- **Click/Tap** the eye icon to toggle visibility
- **Green dot** = Titles visible
- **Red dot** = Titles hidden
- **Cross line** appears when titles are hidden

### Button Position

The button is positioned 60 pixels from the top-right corner to avoid overlapping with other UI elements.

### What Gets Hidden

When activated, the script hides:
- Default Roblox nametags
- Health bars
- BillboardGuis attached to characters
- SurfaceGuis on character heads
- TextLabels, TextButtons, and TextBoxes in character heads

## 🔧 Configuration

You can customize the script by modifying the `CONFIG` table:

```lua
local CONFIG = {
    BUTTON_SIZE_MOBILE = UDim2.new(0, 35, 0, 35),
    BUTTON_SIZE_PC = UDim2.new(0, 32, 0, 32),
    BUTTON_POSITION = UDim2.new(1, -40, 0, 60), -- X offset, Y offset
    CORNER_RADIUS = UDim.new(0, 8),
    ANIMATION_DURATION = 0.6,
    PULSE_COUNT = 3,
    PULSE_DURATION = 0.15
}
```

### Color Customization

Modify the `COLORS` table to change the appearance:

```lua
local COLORS = {
    DEFAULT_BG = Color3.fromRGB(45, 45, 50),
    HIDDEN_BG = Color3.fromRGB(70, 40, 40),
    ACTIVE_DOT = Color3.fromRGB(80, 255, 120),
    INACTIVE_DOT = Color3.fromRGB(255, 80, 80),
    CROSS_LINE = Color3.fromRGB(255, 80, 80),
    SHADOW = Color3.fromRGB(0, 0, 0)
}
```

## 📱 Platform Support

- ✅ **PC**: Full support with hover animations
- ✅ **Mobile**: Touch-optimized with haptic feedback
- ✅ **Tablet**: Automatically detected and optimized

## ⚙️ Technical Details

### Services Used
- `Players` - Player management
- `UserInputService` - Platform detection
- `RunService` - Animation rendering

### Performance
- Minimal memory footprint
- Efficient state management
- Safe pcall error handling
- No memory leaks

### Compatibility
- Works with all Roblox games
- Compatible with custom character models
- Handles dynamic GUI additions

## 🐛 Troubleshooting

**Button not appearing?**
- Ensure the script is placed in `StarterGui` or `StarterPlayerScripts`
- Check that it's a `LocalScript`, not a regular Script

**Some GUIs still showing?**
- The script targets standard GUI types; custom implementations may require modification
- Check if GUIs are parented to the character's Head

**Animation lag on mobile?**
- Reduce `ANIMATION_DURATION` in the CONFIG table
- Decrease `PULSE_COUNT` for fewer pulse animations

## 📝 License

This script is free to use and modify for any Roblox project.

## 👤 Author

**ItoRenz00**

## 🤝 Contributing

Feel free to fork, modify, and submit improvements!

### Suggested Improvements
- Add keyboard shortcut support
- Include customizable hotkey settings
- Add GUI scale options
- Implement fade transitions
- Add sound effects toggle

## 📋 Changelog

### Version 1.0.0 (Current)
- Initial release
- Cross-platform support
- Animated toggle button
- Automatic player detection
- Status indicator system

## ⚠️ Notes

- This script only affects the local client's view
- Other players will still see titles normally
- Some game-specific GUIs may require additional handling
- Respects Roblox's default humanoid display settings

---

**Made with ❤️ for the Roblox community**
