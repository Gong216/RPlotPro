# R Plot Pro

<p align="center">
  <img src="https://raw.githubusercontent.com/ofurkancoban/RPlotPro/refs/heads/main/assets/icon.png" width="250" alt="R Plot Pro Logo">
</p>

<p align="center">
  <strong>Professional R plot visualization for VS Code</strong><br>
  The ultimate R visualization experience for VS Code. High-performance, real-time, and designed for professionals who demand the best of RStudio and Positron.
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=ofurkancoban.r-plot-pro"><img src="https://img.shields.io/visual-studio-marketplace/v/ofurkancoban.r-plot-pro?style=flat-square&label=VS%20Code%20Marketplace&logo=visual-studio-code" alt="VS Code Marketplace"></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=ofurkancoban.r-plot-pro"><img src="https://img.shields.io/visual-studio-marketplace/d/ofurkancoban.r-plot-pro?style=flat-square" alt="Downloads"></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=ofurkancoban.r-plot-pro"><img src="https://img.shields.io/visual-studio-marketplace/r/ofurkancoban.r-plot-pro?style=flat-square" alt="Rating"></a>
</p>

---

## 🎯 Why R Plot Pro?

Tired of switching between VS Code and RStudio just to see your plots? **R Plot Pro** brings the **familiar RStudio Plots pane** and **Positron's modern plotting experience** directly into VS Code.

### Just Like RStudio & Positron:
- ✅ **Side panel plot viewer** - opens in the right sidebar, just like RStudio
- ✅ **Automatic plot capture** - every plot you create appears instantly
- ✅ **Plot history navigation** - browse through all your plots with arrows
- ✅ **Familiar workflow** - works exactly like you're used to in RStudio
- ✅ **Modern UI** - Positron-inspired design with smooth animations

**No more context switching!** Work in VS Code with the plotting power of RStudio and the elegance of Positron.

---

## ✨ Features

### 🎨 **Real-Time Visualization**
View your R plots **instantly** as they're generated in the terminal. No manual refresh needed.

### 📊 **Advanced Plot Gallery**
- **Thumbnail view** with timestamp and metadata
- **Drag-and-drop** plot reordering
- **Favorites system** to mark important plots
- **Filter** to show only favorited plots
- **Notes** for documenting your analysis

### 🎯 **Interactive Navigation**
- Navigate plots with **arrow keys** or navigation buttons
- **Fullscreen mode** for detailed inspection
- **Smooth transitions** between plots
- Auto-scroll active plot into view

### 🎛️ **Flexible Layouts**
- **Auto-sizing** - plots adapt to window size
- **Aspect ratio control** - square, landscape, portrait, or fill
- **Zoom controls** - 50% to 200% with fit-to-screen option
- **Sidebar toggle** for maximum plot space

### 💾 **Export & Organization**
- **Drag plots** directly to desktop/finder to save
- **Notes** on each plot for documentation
- **Plot history** - keeps last 200 plots
- **Memory optimized** - automatic cleanup

### 🎭 **Beautiful UI**
- **Dark mode** support (auto-detects VS Code theme)
- **Smooth animations** and transitions
- **Modern design** with glassmorphism effects
- **Responsive** interface

---

## 🚀 Getting Started

### Installation

1. **Install from Marketplace:**
   ```
   ext install ofurkancoban.r-plot-pro
   ```

2. **Or install manually:**
   - Download the `.vsix` file
   - Run: `code --install-extension r-plot-pro-0.0.1.vsix`

### First Use

1. **Open an R file** in VS Code
2. **Run R code** in the integrated terminal
3. **Plot viewer opens automatically** in the **right sidebar panel** when you create your first plot
4. The viewer stays open and updates in real-time as you create more plots
5. **Start plotting!** 🎉

> **💡 Tip:** The plot viewer appears as a sidebar panel (like RStudio's Plots pane), keeping your code visible while you explore visualizations. You can drag it to any position or open it manually with `View > Open View > R Plot Viewer`.

---

## 📖 Usage

### Basic Workflow

```r
# Create a plot - viewer opens automatically
plot(mtcars$mpg, mtcars$hp, 
     main = "MPG vs HP",
     xlab = "Miles Per Gallon",
     ylab = "Horsepower")

# ggplot2 also supported
library(ggplot2)
ggplot(mtcars, aes(x = mpg, y = hp)) +
  geom_point(color = "steelblue", size = 3) +
  theme_minimal()
```

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + →` | Next plot |
| `Cmd/Ctrl + ←` | Previous plot |
| `Space` | Toggle fullscreen |
| `Esc` | Exit fullscreen |

### UI Controls

**Top Toolbar:**
- **Navigation** - Previous/Next plot buttons
- **Zoom** - 50%, 75%, 100%, 150%, 200%, Fit
- **Layout** - Aspect ratio control (auto, square, landscape, portrait, fill)
- **Clear All** - Remove all plots

**Plot Thumbnail Actions:**
- **Click** - View plot
- **Star icon** - Mark as favorite
- **Note icon** - Add/edit note
- **Delete icon** - Remove plot
- **Drag** - Reorder or export

---

## 🔧 Requirements

- **VS Code** 1.85.0 or higher
- **R** 4.0.0 or higher


---

## 📋 Features in Detail

### Plot Memory Management
- Automatically keeps last **200 plots**
- Oldest plots removed when limit reached
- Optimized memory usage (~100MB for 200 plots)

### Export Options
- **Drag-and-drop** to desktop (saves as PNG)
- High-resolution output
- Preserves aspect ratio

### Notes & Documentation
- Add notes to any plot
- Notes saved in VS Code state
- Perfect for documenting analysis steps

### Favorites
- Star important plots
- Filter view to show only favorites
- Never lose track of key visualizations

---

## 🎯 Use Cases

### Data Exploration
Quickly iterate through different visualizations while keeping a history of all attempts.

### Presentation Prep
Mark your best plots as favorites, add notes, and easily export for slides.

### Collaborative Analysis
Document your plotting process with notes for team members.

### Teaching
Show students the progression of plot improvements with before/after comparisons.

---

## ⚙️ Extension Settings

This extension works out of the box with no configuration needed. Advanced users can modify:

- Plot server port (default: auto-assigned)
- Maximum plots to keep (default: 200)
- Auto-open viewer (default: true)

---

## 🐛 Known Issues

- Plots created in background R sessions may not appear (must use VS Code terminal)
- Very large plots (>10MB) may render slowly
- Some R graphics devices may not be captured

---

## 🔄 Release Notes

### 0.0.1 - Initial Release

**Features:**
- Real-time plot visualization
- Advanced plot gallery with thumbnails
- Favorites and notes system
- Drag-and-drop export
- Multiple zoom and aspect ratio options
- Dark mode support

**Bug Fixes:**
- Fixed WebSocket timing issues
- Improved error handling
- Optimized resize events

---

## 🙏 Support

If you find R Plot Pro useful, consider supporting its development!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/ofurkanco)

---

## 📝 License

MIT License - feel free to use in your projects!

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

**Enjoy plotting!** 📊✨
