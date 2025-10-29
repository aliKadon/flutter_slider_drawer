## [0.1.3] - Bug Fixes and Improvements

### 🐞 Fixes
- Fixed minor issues affecting drawer behavior and animations.
- Improved overall performance and stability.
- Minor UI and code quality refinements.

---


## [0.1.2] - Documentation
- README updates only (no code changes).

## [0.1.1] - Bug Fix Release

### 🐞 Fixes
- Fixed minor issues related to drawer icon state changes.
- Improved reliability of the `onDrawerTap` callback.
- Optimized animation timing for smoother transitions.
- General stability improvements and code cleanup.

---

## [0.1.0] - Initial Release

This is the first release of **customized_flutter_slider_drawer**,  
a customized and enhanced version of the original `flutter_slider_drawer` package.

### ✨ New Features
- Added **customizable drawer icon**:
   - You can now set your own icon for the drawer.
   - The icon can change automatically when the drawer is **opened** or **closed**.
- Added **onDrawerTap** callback to handle drawer tap events easily.

### ⚙️ Improvements
- Built upon the latest stable version of `flutter_slider_drawer` (v3.0.2).
- Enhanced animation and performance consistency with Flutter 3.x.
- Updated documentation for clarity and simplicity.

### 🧹 Deprecations (inherited from the base package)
- Removed old/deprecated parameters (`isTitleCenter`, `appBarHeight`, etc.).
- Continued using `SliderAppBarConfig` for app bar customization.
- Maintains renamed enum values for clarity:
   - `LEFT_TO_RIGHT` → `leftToRight`
   - `RIGHT_TO_LEFT` → `rightToLeft`
   - `TOP_TO_BOTTOM` → `topToBottom`

### 📦 Notes
- This package is **not an official update** of `flutter_slider_drawer` — it’s a **community customization** with additional features and better flexibility.
- Original package: [flutter_slider_drawer](https://pub.dev/packages/flutter_slider_drawer)
