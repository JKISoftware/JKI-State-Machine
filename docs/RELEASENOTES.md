# Release Notes - JKI State Machine 2024
### Release Date - 2024-08-19

The 2024 release introduces new utility VIs, updates the source code to LabVIEW 2020, and adds new template features to address common developer challenges.

### New features

- **New Utility VIs**
  - [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Select State(s)` allows conditional (Boolean or error) enqueuing of states
  - [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Conditional State String` allows conditional (Boolean) enqueuing of states
  - [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Periodic State String` allows periodic (time triggered) enqueing of states

- **Template Changes**
  - [#11](https://github.com/JKISoftware/JKI-State-Machine/issues/#11) Error Handler is now appends the  previous state string (and raw arguments+comments) to the error message
  - [#30](https://github.com/JKISoftware/JKI-State-Machine/issues/#30) Added UI: Cleanup state (called by Macro: Exit)
  - [#29](https://github.com/JKISoftware/JKI-State-Machine/issues/#29) Warnings are cleared in the Error Handing State.


### Improvements

- [#20](https://github.com/JKISoftware/JKI-State-Machine/issues/#20) JKI SM Template's **OK** button renamed to **Cancel** and key binding changed from `Enter` to `Escape`
- JKI SM Editor [#98](https://github.com/JKISoftware/JKI-State-Machine/issues/#98) Duplicating a category frame in the JKI SM Editor now inserts it *after* all states in the duplicated category (instead of immediately after and absorbing all the states).

### Development Improvements
- Upgraded sources to LabVIEW 2020 and seperated compiled code
- VIPC file updated
- Additional package dependencies removed
- Added additional unit tests for new features

### Bug fixes
- [#17](https://github.com/JKISoftware/JKI-State-Machine/issues/#17) Fixed typo in UI: Initialize state comment

### Known issues
- None reported




---

> Get training here: [JKI Sate Machine Training](https://www.jki.net/training/jki-state-machine).