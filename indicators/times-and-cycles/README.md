# [FS] Time & Cycles

A comprehensive TradingView indicator for tracking daily and weekly price levels, daily cycles, and trading sessions. Essential for traders who need to monitor key price levels across different timeframes and identify important time-based market structures.

## Features

### Daily and Weekly Levels

#### Current Levels
- **Today (DH/DL)**: Current day high and low levels
  - Automatically updates throughout the trading day
  - Color-coded for easy identification
  - Works on intraday timeframes

- **This Week (WH/WL)**: Current week high and low levels
  - Updates in real-time as the week progresses
  - Separate color control for weekly levels
  - Displays labels centered on the week's high/low

#### Historical Levels
- **Previous Daily High/Low (PDH/PDL)**: 
  - Configurable history (1-10 periods, default: 5)
  - Shows multiple previous day levels
  - Automatically tracks and updates daily highs/lows

- **Previous Weekly High/Low (PWH/PWL)**:
  - Configurable history (1-10 periods, default: 3)
  - Shows multiple previous week levels
  - Tracks weekly extremes accurately

### Daily Cycles

Tracks specific time-based price levels that occur at key market hours:

- **00:00**: Midnight cycle level
- **09:30**: Market open cycle (US market open)
- **15:30**: Afternoon cycle
- **16:00**: Market close cycle (US market close)

Each cycle can be individually enabled/disabled with custom colors and line styles.

### Trading Sessions

Visual representation of major trading sessions with customizable time blocks:

- **London Session**: Default 07:00-16:00 (configurable)
- **New York Session**: Default 13:00-22:00 (configurable)
- **Sydney Session**: Default 21:00-06:00 (configurable)
- **Asia Session**: Default 00:00-09:00 (configurable)
- **TBD Session**: Custom session (default: 09:00-12:00)

**Session Features:**
- Timezone selection (11 major timezones supported)
- Custom session times for each market
- Color-coded session blocks
- Optional session labels
- Configurable border styles

## Parameters

### Previous High/Low

#### Level Visibility
- **Today**: Toggle and color for current day high/low
- **This Week**: Toggle and color for current week high/low
- **D**: Toggle and color for previous daily levels
- **W**: Toggle and color for previous weekly levels

#### Display Options
- **Show Labels**: Toggle to show/hide all labels
- **Show Lines**: Toggle to show/hide all lines
- **Show Dates**: Optional date display on labels

#### History
- **History Levels (PDL/PDH)**: Number of previous daily levels (1-10, default: 5)
- **History Levels (PWL/PWH)**: Number of previous weekly levels (1-10, default: 3)

#### Style
- **Line Style**: Choose between solid, dashed, or dotted lines

### Daily Cycles

Each cycle (00:00, 09:30, 15:30, 16:00) has:
- Enable/disable toggle
- Color selection
- Line style selection (solid, dashed, dotted)

### Sessions

- **Sessions Timezone**: Select from 11 major timezones
- **Session Configuration**: For each session (London, NY, Sydney, Asia, TBD):
  - Enable/disable toggle
  - Custom label text
  - Color selection
  - Session time range (HHMM-HHMM format)
- **Blocks Border Style**: Style for session blocks (solid, dashed, dotted)
- **Show Labels**: Toggle session labels

## Usage

### Basic Setup

1. Add the indicator to your chart
2. The indicator automatically detects your timeframe:
   - **Intraday**: Shows daily and weekly levels, cycles, and sessions
   - **Daily**: Shows weekly levels
   - **Weekly/Monthly**: Adapts display accordingly

3. Configure level visibility:
   - Enable/disable Today, This Week, Previous Daily, Previous Weekly
   - Set history levels for previous periods

4. Customize appearance:
   - Choose colors for each level type
   - Select line styles
   - Toggle labels and dates

### Daily Cycles

1. Enable the cycles you want to track (00:00, 09:30, 15:30, 16:00)
2. Customize colors and line styles for each cycle
3. Cycles are only displayed on intraday timeframes

### Trading Sessions

1. Select your preferred timezone
2. Enable the sessions you want to display
3. Customize session times if needed (defaults are provided)
4. Adjust colors and labels for each session
5. Choose border style for session blocks

## Use Cases

### Support and Resistance Trading
- Identify key daily and weekly support/resistance levels
- Monitor price action relative to previous periods
- Plan entries and exits based on historical levels

### Breakout Trading
- Track when price breaks above/below previous day/week highs/lows
- Identify potential breakout levels
- Monitor multiple historical levels for confirmation

### Time-Based Trading
- Use daily cycles to identify key time-based price levels
- Monitor trading sessions for volatility patterns
- Plan trades around session opens and closes

### Multi-Timeframe Analysis
- Combine daily levels on intraday charts for context
- Use weekly levels on daily charts for broader perspective
- Track multiple historical periods for trend analysis

## Technical Details

- **Pine Script Version**: v6
- **Timeframe Detection**: Automatically adapts to current chart timeframe
- **Level Tracking**: Uses arrays to efficiently store and manage historical levels
- **Real-Time Updates**: Levels update automatically as new bars form
- **Performance**: Optimized with efficient array management and conditional rendering

## Notes

- Daily levels are only displayed on intraday timeframes
- Weekly levels work on all timeframes
- Cycles are only active on intraday timeframes
- Sessions require timezone configuration for accurate display
- The indicator uses `max_bars_back=5000` to ensure sufficient historical data
- Labels are offset to prevent overlap and improve readability
- Historical levels are automatically limited to prevent performance issues

## Timeframe Compatibility

- **Intraday** (seconds, minutes, hours ≤ 240): Full functionality
  - Daily levels (current and historical)
  - Weekly levels (current and historical)
  - Daily cycles
  - Trading sessions

- **Daily**: Weekly levels only
- **Weekly/Monthly**: Adapted display for longer timeframes

