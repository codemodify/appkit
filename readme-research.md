# Summary
- **The whole field collapses onto three rendering strategies** (S / N / W) — the exact axis in your readme. appkit is firmly S, which puts its true peer group at: Qt Quick, Avalonia, Flutter, Slint, Fyne, Gio, Compose, JavaFX, Kivy, LVGL.

- **Within "S," there's a declarative-DSL sub-club** that appkit specifically belongs to: **Qt Quick (QML), Slint (.slint), Avalonia/WPF (XAML), Compose, SwiftUI, JavaFX (FXML)**. These are the ones to study for DSL + binding design.

- **Go's bench is thin and immediate-mode-leaning**. Go's notable self-rendering retained toolkit is essentially just Fyne; Gio is immediate-mode. There is **no Go toolkit doing declarative-QML-style retained UI** — which is precisely the gap appkit fills. That's a genuinely distinctive position.

> **S** = self-rendering (draws its own pixels on a canvas)
> **N** = native-wrapper (delegates to OS widgets)
> **W** = webview-based (uses an HTML/CSS engine)
> **IM** = immediate-mode (re-declares UI every frame; no persistent widget tree)
> **TUI** = terminal UI (renders to a text terminal)

## Toolkits

| Language | Toolkit | Model | Notes |
|---|---|---|---|
| C | GTK | S | GObject; GNOME's foundation |
| C | Clutter | S | GNOME scene-graph; deprecated, folded into GTK4 |
| C | EFL / Elementary | S | Enlightenment's libs; Evas = retained scene-graph canvas; powers Tizen |
| C | Motif | S | classic Unix/CDE toolkit (now open-source) |
| C | IUP | N | native widgets, Lua-friendly |
| C | Nuklear | IM | single-header |
| C | LVGL | S | embedded; dominant embedded C UI |
| C | emWin | S | embedded |
| C# | WPF | S | XAML, DirectX; Windows-only |
| C# | WinUI 3 / UWP | S | modern Windows |
| C# | WinForms | N | classic Win32 wrapper |
| C# | .NET MAUI | N | cross-platform native |
| C# | Avalonia | S | XAML, cross-platform (Skia) |
| C# | Uno Platform | S/N | XAML everywhere incl. WASM |
| C# | Eto.Forms | N | one API, native per-OS |
| C# / C++ | Unity UI Toolkit / Unreal Slate+UMG | S | game UI; engine-native |
| C++ | Qt | S | Widgets + Quick/QML; the heavyweight |
| C++ | wxWidgets | N | wraps native controls |
| C++ | FLTK | S | tiny, non-native |
| C++ | Dear ImGui | IM | tools/game editors; everywhere |
| C++ | JUCE | S | dominant in audio/DAW apps |
| C++ | U++ (Ultimate++) | S | full app framework |
| C++ | Nana | S | modern C++ |
| C++ | Elements (cycfi) | S | modern, GPU |
| C++ | FOX toolkit | S | fast, self-drawn |
| C++ | Noesis GUI | S | game UI; XAML for game engines |
| C++ | RmlUi | S | game UI; HTML/CSS for games |
| C++ | CEGUI | S | game UI; classic |
| C++ | TouchGFX | S | embedded; STM32 |
| D | DlangUI | S | self-rendering D toolkit (OpenGL/software) |
| Dart | Flutter | S | Skia/Impeller; mobile + desktop + web — the dominant self-renderer |
| Go | Gio | IM | GPU, pure Go — closest technical sibling (substrate) |
| Go | Fyne | S | OpenGL, Material-ish, most popular |
| Go | gotk4 | S | GTK4 bindings |
| Go | miqt / therecipe-qt | S | Qt bindings via CGo |
| Go | giu | IM | Dear ImGui wrapper |
| Go | walk | N | Windows-only native |
| Go | nucular | IM | Nuklear port |
| Java | Swing | S | classic, self-drawn |
| Java | JavaFX | S | scene-graph, declarative-ish |
| Java | SWT | N | Eclipse; native widgets |
| JavaScript | React Native | N | native mobile widgets |
| Kotlin | Compose Multiplatform | S | Skia (Skiko) |
| Kotlin | Jetpack Compose | S | modern Android (shares core w/ Compose MP) |
| Kotlin / Java | Android Views | N | Android's classic UI |
| Obj-C | GNUstep | S | open Cocoa/AppKit reimplementation |
| Pascal | Lazarus LCL | N | Free Pascal; native widgets per-OS (Delphi-like) |
| Python | tkinter (Tk) | S | built-in default |
| Python | PyQt / PySide | S | Qt bindings |
| Python | Kivy | S | OpenGL, touch-first |
| Python | wxPython | N | wxWidgets bindings |
| Python | DearPyGui | IM | ImGui for Python |
| Python | Flet | S | Flutter-backed |
| Python | Toga (BeeWare) | N | truly native widgets |
| Rust | egui | IM | pure Rust, very popular |
| Rust | Iced | S | Elm-style, wgpu |
| Rust | Slint | S | QML-like DSL — closest reference for appkit; also targets embedded |
| Rust | Xilem | S | Linebender's future (replaces Druid) |
| Rust | Dioxus | S/W | React-like; native + web |
| Rust | Freya | S | Skia-based, on Dioxus |
| Rust | Makepad | S | shader-driven |
| Rust | relm4 / gtk-rs | S | GTK bindings |
| Swift | SwiftUI | S | declarative |
| Swift / Obj-C | UIKit / AppKit | N | the actual Apple frameworks |

## Web (webview-based)

| Language | Toolkit | Model | Notes |
|---|---|---|---|
| C++ | Sciter | W | embeddable HTML/CSS/JS, tiny |
| C++ | Ultralight / CEF | W | embeddable browser engines |
| Go | Wails | W | Go + system webview |
| JavaScript | Electron | W | bundles Chromium; huge but ubiquitous |
| JavaScript | NW.js / Neutralino | W | lighter Electron-likes |
| JavaScript | Ionic / Capacitor | W | webview mobile |
| Rust / JS | Tauri | W | Electron alternative, system webview |

## Terminal (TUI)

| Language | Toolkit | Model | Notes |
|---|---|---|---|
| C | ncurses | TUI | terminal UI |
| C | notcurses | TUI | high-capability terminal graphics |
| C++ | FTXUI | TUI | functional terminal UI |
| Go | Bubble Tea | TUI | Elm-architecture, instructive for state/update design |
| Go | tview | TUI | widget-based terminal UI |
| Python | Textual | TUI | terminal UI |
| Rust | ratatui | TUI | terminal UI |
