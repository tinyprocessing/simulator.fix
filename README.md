# Simulator Fix ![CI](https://github.com/jessesquires/Nine41/workflows/CI/badge.svg)

*Automate overriding the status bars for all running iOS simulators*

## About


[Xcode 11](https://developer.apple.com/documentation/xcode_release_notes/xcode_11_release_notes) shipped with `simctl status_bar`, a tool to override the status bar values in the simulator so you can take perfect screenshots.

However, it has some issues:
* The overrides do not persist across launches of the simulator
* The numerous override options are difficult to remember
* There are no sensible defaults

This script fixes most of those issues. It overrides the status bars for all currently running simulators using "Apple's defaults" &mdash; full cellular bars, full wifi bars, full battery, no "carrier" name, and `9:41` for the time.

## Requirements

- Swift 5.3+
- Xcode 12.0+
- [SwiftLint](https://github.com/realm/SwiftLint)

## Installation

### [Swift Package Manager](https://swift.org/package-manager/)

Add `simulator.fix` to the `dependencies` value of your `Package.swift`.

```swift
dependencies: [
    .package(url: "https://github.com/michaelsafir/simulator.fix.git", from: "1.0")
]
```

Alternatively, you can add the package [directly via Xcode](https://developer.apple.com/documentation/xcode/adding_package_dependencies_to_your_app).



## Usage

After cloning the repo, you can create a custom bash command:

```bash
swift run
```

