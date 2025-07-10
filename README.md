# grblhal-macros

A collection of custom G-code macros for use with grblHAL-based CNC controllers. These macros are designed to automate and simplify tool changes, probing, rack management, and other advanced CNC operations.

## Features
- Automatic and manual tool change support
- Tool probing and length measurement
- Tool rack slot assignment and management
- Configuration and initialization routines
- Debug output for troubleshooting

## File Overview
- `P100.macro`: Loads and sets up global configuration variables for the CNC environment.
- `P101.macro`: Defines unrackable tools and tool info storage.
- `P110.macro`: Finds a parking slot for the current tool.
- `P111.macro`: Finds a pickup slot for the selected tool.
- `P112.macro`: Sets a tool in a rack slot.
- `P115.macro`: Clears the tool rack.
- `P116.macro`: Displays tool rack state.
- `P117.macro`: (Reserved/empty)
- `P120.macro`: Moves to a specified rack slot.
- `P200.macro`: Assigns a tool to a rack slot, checks unrackable list.
- `P201.macro`: Stores tool info.
- `P202.macro`: Loads tool description.
- `P299.macro`: Utility/debug macro.
- `P300.macro`: Grabs a tool.
- `P301.macro`: Drops a tool.
- `P302.macro`: Checks if a tool is present.
- `P303.macro`: Probes tool length.
- `P304.macro`: Tool breakage detection.
- `P310.macro`: Parks the current tool.
- `P311.macro`: Picks up the selected tool.
- `TC.macro`: Main tool change macro.

## Usage
1. Upload the macro files to your controller using your preferred gcode-sender.
2. Adjust configuration values in `P100.macro` as needed for your machine.
3. The controller will automatically call `TC.macro` on tool change events.

## Requirements
- grblHAL-based CNC controller
- Macro support enabled in your controller firmware
- Either a custom version of grblHAL that supports string registers, or a plugin that provides this support

### Recommended/Forked Repositories
To enable all features used by these macros, you may need the following forks:
- https://github.com/skasti/grblHal-core
- https://github.com/skasti/grblHal-Plugin_SD_card
- https://github.com/skasti/STM32F4xx

## Versioning
Each macro includes a debug/version line at the top for easy tracking.

## License
This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) License. See the LICENSE file for details.

These macros are provided as-is, without warranty. See individual files for copyright or license information if present.

---

Maintained by skasti
