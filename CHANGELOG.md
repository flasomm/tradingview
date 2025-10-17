# Changelog

All notable changes to the Time & Cycles Pine Script indicator will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2024-12-19

### Added
- **This Week feature**: New checkbox and color picker for current week levels
- **WH/WL labels**: Weekly High and Weekly Low labels for the current week
- **Current week display**: Shows the highest and lowest prices of the current week with orange horizontal lines
- **Independent control**: "This Week" can be toggled on/off independently from historical weekly levels

### Changed
- **PWL/PWH correction**: Fixed display offset issue where PWL-2/PWH-2 was showing instead of PWL/PWH
- **Label positioning**: "This Week" checkbox moved to optimal position (after "Today", before "D")
- **Line display**: Weekly levels now display as horizontal lines extending to the right
- **Comment translation**: All French comments translated to English for better code readability

### Fixed
- **Weekly level display**: Resolved issue where WH/WL labels were not appearing on the chart
- **Line orientation**: Fixed vertical line issue - weekly levels now display as proper horizontal lines
- **Current week tracking**: Improved initialization and tracking of current week high/low values
- **Display conditions**: Simplified plot_level function logic to ensure reliable label display

### Technical Improvements
- **Variable initialization**: Added proper initialization of current week variables at script start
- **Display logic**: Enhanced plot_level function to handle current bar display correctly
- **Code structure**: Improved code organization and readability
- **Error handling**: Better handling of edge cases in weekly level calculations

## [1.0.0] - Initial Release

### Added
- **Previous High/Low levels**: Daily and weekly historical levels (PDH/PDL, PWH/PWL)
- **Current day levels**: Today's high and low (DH/DL)
- **Daily cycles**: Time-based cycle levels (00:00, 09:30, 15:30, 16:00)
- **Trading sessions**: London, New York, Sydney, Asia, and TBD session boxes
- **Customizable display**: Color and style options for all elements
- **Timezone support**: Multiple timezone options for session display
- **Label and line controls**: Toggle options for labels, lines, and dates
- **History levels**: Configurable number of historical levels to display

### Features
- **Multi-timeframe support**: Works on intraday and daily timeframes
- **Session visualization**: Real-time session boxes with high/low tracking
- **Cycle detection**: Automatic detection of daily time cycles
- **Level management**: Automatic cleanup of old levels to maintain performance
- **Customizable styling**: Line styles (solid, dashed, dotted) and colors
