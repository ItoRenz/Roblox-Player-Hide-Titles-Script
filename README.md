# 👁️ Roblox Hide Player Titles Script

A lightweight and elegant Roblox script that allows you to hide all player overhead elements (names, titles, billboards, health bars) with a simple toggle button.

## ✨ Features

- **🎯 Complete Hiding** - Hides all overhead elements:
  - Player display names & usernames
  - Health bars
  - Custom titles and badges
  - BillboardGui elements
  - SurfaceGui elements
  - All TextLabels above player heads

- **📱 Platform Optimized**
  - Automatic detection of Mobile vs PC
  - Different UI sizes for optimal touch/mouse experience
  - Haptic feedback for mobile devices
  - Smooth hover animations on PC

- **🎨 Modern UI Design**
  - Sleek eye icon with smooth animations
  - Visual status indicator (green dot = visible, red = hidden)
  - Shadow effects and rounded corners
  - Responsive click/touch animations

- **⚡ Performance Optimized**
  - Error handling with pcall() wrappers
  - Efficient object tracking
  - No memory leaks
  - Automatic cleanup

- **🔄 Dynamic Updates**
  - Automatically applies to players who join mid-game
  - Monitors new GUI elements added during gameplay
  - Persists through character respawns

## 🚀 Installation

### Method 1: Roblox Studio (Recommended)

1. Open your Roblox game in Roblox Studio
2. Navigate to **StarterGui** in the Explorer window
3. Insert a new **LocalScript**
4. Copy and paste the entire script code
5. Rename the script to "HideTitlesScript" (optional)
6. Test in Play mode!

### Method 2: StarterPlayerScripts

1. Open Roblox Studio
2. Navigate to **StarterPlayer** → **StarterPlayerScripts**
3. Insert a new **LocalScript**
4. Paste the script code
5. Done!

## 📖 Usage

### In-Game Controls

- **Click/Tap** the eye icon in the top-right corner to toggle visibility
- **Green dot** = All player titles visible
- **Red dot** = All player titles hidden
- **Red slash** over eye = Hidden mode active

### Platform-Specific Behavior

**PC:**
- Button size: 45x45 pixels
- Hover animation on mouse-over
- Expands to 50x50 on hover

**Mobile:**
- Button size: 50x50 pixels (larger for touch)
- Haptic feedback on toggle
- No hover effects

## 🎮 Compatible With

- ✅ All Roblox games
- ✅ Mobile devices (iOS/Android)
- ✅ PC (Windows/Mac)
- ✅ Xbox (with gamepad)
- ✅ VR platforms
- ✅ Custom character models
- ✅ All display name/title systems

## 🛠️ Technical Details

### Script Type
- **LocalScript** (Client-side only)

### Services Used
- Players Service
- UserInputService
- HapticService (mobile only)

### Features
- Automatic platform detection
- Error handling with pcall()
- Dynamic GUI monitoring
- Object state preservation for proper restore

## 🐛 Troubleshooting

### Script not working?
1. Make sure the script is a **LocalScript**, not a regular Script
2. Verify it's placed in **StarterGui** or **StarterPlayerScripts**
3. Check the Output window for error messages
4. Ensure FilteringEnabled is on (default in all modern games)

### Button not appearing?
1. Check if another GUI is blocking it
2. Try repositioning the button in the script
3. Verify ResetOnSpawn is set to false

### Some elements not hiding?
- The script hides most common overhead elements
- Some custom implementations may require script modifications
- Check if elements are parented to Head or Character

## 📝 Customization

### Change Button Position

```lua
-- Find this line (around line 24):
local buttonPosition = isMobile and UDim2.new(1, -70, 0, 15) or UDim2.new(1, -65, 0, 15)

-- Modify the values:
-- UDim2.new(X_Scale, X_Offset, Y_Scale, Y_Offset)
-- Example for top-left: UDim2.new(0, 15, 0, 15)
```

### Change Button Size

```lua
-- Find this line (around line 23):
local buttonSize = isMobile and UDim2.new(0, 50, 0, 50) or UDim2.new(0, 45, 0, 45)

-- Adjust the pixel values (last two numbers)
```

### Change Colors

```lua
-- Button background (line 33):
toggleButton.BackgroundColor3 = Color3.fromRGB(45, 45, 50)

-- Hidden mode color (line 158):
toggleButton.BackgroundColor3 = Color3.fromRGB(70, 40, 40)

-- Status indicator colors (lines 161-162, 165-166)
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is free to use and modify for your Roblox games.

## ⚠️ Disclaimer

This script is intended for legitimate gameplay purposes. Please respect the game developers' intentions and other players' experiences. Do not use this to gain unfair advantages or violate game rules.

## 🌟 Credits

Created with ❤️ for the Roblox community

## 📞 Support

If you encounter any issues or have questions:
1. Check the Troubleshooting section above
2. Review the Output window for error messages
3. Open an issue on GitHub with detailed information

---

**Enjoy cleaner gameplay!** 👁️✨
