# 👁️ Hide Player Titles Script

A lightweight and optimized Roblox script that allows you to toggle the visibility of player titles, nametags, and overhead GUIs with a single click. Perfect for screenshots, videos, or immersive gameplay.

## ✨ Features

- **One-Click Toggle** - Simple eye icon button to show/hide all player titles
- **Cross-Platform** - Optimized for both Mobile and PC
- **Hides Everything** - Removes:
  - Custom player titles and tags
  - Billboard GUIs above heads
  - Default nametags and health bars
  - Surface GUIs on character heads
- **Smooth Animations** - Polished button interactions with hover and click effects
- **Status Indicator** - Visual dot showing current visibility state
- **Haptic Feedback** - Vibration feedback on mobile devices
- **Persistent** - Automatically applies to new players joining the game
- **Lightweight** - Minimal performance impact

## 🎮 Preview

The toggle button appears in the **top-right corner** of your screen:
- **Green dot** = Titles visible 👁️
- **Red dot** = Titles hidden 👁️ with slash

## 📦 Installation

### Method 1: StarterGui (Recommended)
1. Open Roblox Studio
2. Navigate to `StarterGui`
3. Insert a new `LocalScript`
4. Copy and paste the entire script code
5. Save and test in-game

### Method 2: StarterPlayerScripts
1. Open Roblox Studio
2. Navigate to `StarterPlayer` → `StarterPlayerScripts`
3. Insert a new `LocalScript`
4. Copy and paste the entire script code
5. Save and test in-game

## 🎯 Usage

1. **Launch the game** - The eye icon button will appear in the top-right corner
2. **Click the button** to toggle title visibility:
   - First click: Hides all player titles
   - Second click: Shows all player titles again
3. **Status indicator** changes color based on state:
   - 🟢 Green = Visible
   - 🔴 Red = Hidden

### Mobile Users
- Tap the eye icon to toggle
- Button is slightly larger for easier touch interaction
- Haptic feedback confirms your action

### PC Users
- Click the eye icon to toggle
- Hover over the button for a subtle size animation
- Smooth transitions for better UX

## ⚙️ Customization

You can easily customize the button position by modifying line 20:

```lua
-- Current position (60 pixels from top)
local buttonPosition = isMobile and UDim2.new(1, -40, 0, 60) or UDim2.new(1, -40, 0, 60)

-- Examples:
-- Higher position: UDim2.new(1, -40, 0, 20)
-- Lower position: UDim2.new(1, -40, 0, 100)
-- Left side: UDim2.new(0, 10, 0, 60)
```

### Color Customization

Change button colors by modifying these lines:

```lua
-- Default state (line 25)
toggleButton.BackgroundColor3 = Color3.fromRGB(45, 45, 50)

-- Hidden state (line 156)
toggleButton.BackgroundColor3 = Color3.fromRGB(70, 40, 40)

-- Status dot colors (lines 97 & 160)
statusDot.BackgroundColor3 = Color3.fromRGB(80, 255, 120) -- Green
statusDot.BackgroundColor3 = Color3.fromRGB(255, 80, 80)  -- Red
```

## 🔧 Technical Details

### What Gets Hidden
- `BillboardGui` elements
- `SurfaceGui` elements on character heads
- `TextLabel`, `TextButton`, `TextBox` inside Head
- `Humanoid.DisplayDistanceType` (nametags & health bars)

### Compatibility
- ✅ Roblox PC Client
- ✅ Roblox Mobile (iOS/Android)
- ✅ Works with most custom title systems
- ✅ Compatible with FilteringEnabled games

### Performance
- Minimal CPU usage
- Uses `pcall()` for error handling
- Efficient event listeners
- No memory leaks

## 🐛 Troubleshooting

**Button doesn't appear:**
- Make sure the script is a `LocalScript`
- Check it's placed in `StarterGui` or `StarterPlayerScripts`
- Look for errors in the output console

**Some titles still showing:**
- Some custom title systems may use unique methods
- The script covers most common implementations
- Contact the developer for specific game support

**Button position overlaps with other UI:**
- Adjust the `buttonPosition` variable (line 20)
- Move it to a different corner or location

## 📝 Changelog

### Version 1.1
- Lowered button position from 10px to 60px from top
- Improved mobile touch target size
- Added haptic feedback for mobile

### Version 1.0
- Initial release
- Basic show/hide functionality
- Cross-platform support

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues) if you want to contribute.

## 👤 Author

Created with ❤️ for the Roblox community

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

**Note:** This script only affects the local player's view. Other players will still see all titles normally. This is a client-side visual enhancement only.
