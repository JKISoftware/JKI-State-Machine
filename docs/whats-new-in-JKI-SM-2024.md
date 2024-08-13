# What's New in JKI State Machine 2024

This is a major new release with a focus on a few significant improvements:

1. **New State Enqueuing VIs**, to make it easier to conditionally enqueue states based on boolean logic and periodic timing (in a way that produces readable code).
2. **Improved Error Handling**, to include information about the state where the error occurred as well as clear (or handling) "warnings" (non-zero `error code` but `status` is False).
3. **Upgrading source code to LV2020**, to make it easier for community members to contribute and for the development team to take advantage of newer LabVIEW features.

There are also some other nice improvements to the template and misc fixes.

## New State Enqueuing VIs
We've added a few useful utility VIs to make it easier to create state logic in your application in a way that produces readable code.

- [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Select State(s)` allows conditional (Boolean or error) enqueuing of states
- [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Conditional State String` allows conditional (Boolean) enqueuing of states
- [#21](https://github.com/JKISoftware/JKI-State-Machine/issues/#21) `Periodic State String` allows periodic (time triggered) enqueing of states

## Improved Error Handling
Better error handling is always nice. So, we've added a couple nice improvements:

- [#11](https://github.com/JKISoftware/JKI-State-Machine/issues/#11) Error Handler now appends the previous state string (and raw arguments+comments) to the error message, **so you know which frame produced the error**.
- [#29](https://github.com/JKISoftware/JKI-State-Machine/issues/#29) Warnings are now cleared in the Error Handing State, whereas previously warnings would persist on the error wire (e.g. until a real error occurred).

## Other Improvements

### Misc Template Changes

- [#20](https://github.com/JKISoftware/JKI-State-Machine/issues/#20) CHANGED the JKI SM Template's **OK** button: renamed it to **Exit** and removed key binding since many users were finding that the `Enter` key binding was problematic.

- [#30](https://github.com/JKISoftware/JKI-State-Machine/issues/#30) NEW state `UI: Cleanup` state (which is called by `Macro: Exit`) provides a place to put code that resets the user interface to a default state and helps avoid saving unwanted state data in the UI (such as Graph/Chart data, Multi-Column Listbox strings).

- [#17](https://github.com/JKISoftware/JKI-State-Machine/issues/#17) FIXED typo in `UI: Initialize` state comment text.

### JKI State Machine Editor UI Fix

- [#98](https://github.com/JKISoftware/JKI-State-Machine/issues/#98) FIXED issue where duplicating a category frame resulted in the new category absorbing all the states of the existing/duplicated category. Now, the existing category and states are left intact when the new category is created.

### Development Improvements (Internal to Project)
- Upgraded sources to LabVIEW 2020 and seperated compiled code
- VIPC file updated
- Unused package dependencies removed
- Created additional unit tests for new features

## Known issues
- None reported




---

> Get training here: [JKI Sate Machine Training](https://www.jki.net/training/jki-state-machine).