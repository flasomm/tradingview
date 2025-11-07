# TradingView Indicators

Collection of custom TradingView indicators built with Pine Script v6.

## Indicators

### [FS] Pivot Measurements

An advanced indicator that combines LuxAlgo's pivot point detection algorithm with automatic measurement calculations between consecutive pivots. This indicator helps traders identify key reversal points and measure price movements between them.

**Key Features:**
- **Pivot Detection**: 
  - Detects regular pivot highs and lows using configurable pivot length
  - Identifies missed reversal levels that occurred between regular pivots
  - Visual indicators: Red triangles (▼) for pivot highs, teal triangles (▲) for pivot lows, ghost emoji (👻) for missed pivots
  - Zigzag lines connecting pivots (solid for regular, dashed for missed)
  - Ghost levels showing missed pivot support/resistance areas

- **Automatic Measurements**: 
  - Calculates price movements between consecutive pivots
  - Displays price change (absolute and percentage)
  - Shows duration in bars, days, hours, and minutes
  - Approximates volume for each measurement
  - Color-coded: Blue for upward movements, red for downward movements

- **Visual Display**: 
  - Transparent colored boxes highlighting measurement ranges
  - Labels positioned outside boxes with detailed information
  - Fully customizable transparency for boxes, borders, and label backgrounds

**Key Parameters:**
- Pivot length (default: 50 bars)
- Regular and missed pivot colors
- Measurement count (1-10, default: 10)
- Box transparency (0-100, default: 90%)
- Border transparency (0-100, default: 50%)
- Label background transparency (0-100, default: 30%)
- Label size options

**Use Cases:**
- Identify key support and resistance levels
- Measure price movements between pivot points
- Analyze trend strength and duration
- Find potential reversal zones

For more details, see the [pivot-measurements README](indicators/pivot-measurements/README.md).

### [FS] Time & Cycles

A comprehensive indicator for tracking daily and weekly price levels, including current and previous day/week highs and lows. Essential for traders who need to monitor key price levels across different timeframes.

**Key Features:**
- **Daily Levels**: 
  - Current day high/low (PDH/PDL)
  - Previous day high/low with configurable history (up to 10 periods)
  - Automatic detection of daily timeframe
  - Color-coded lines and labels for easy identification

- **Weekly Levels**: 
  - Current week high/low (WH/WL)
  - Previous week high/low with configurable history (up to 10 periods)
  - Automatic detection of weekly timeframe
  - Separate color controls for weekly levels

- **Display Options**: 
  - Toggle labels and lines independently
  - Optional date display on labels
  - Multiple line styles (solid, dashed, dotted)
  - Color customization for each level type

- **Timeframe Support**: 
  - Works on intraday, daily, weekly, and monthly timeframes
  - Automatically adapts display based on current timeframe
  - Handles both intraday and daily chart views

**Key Parameters:**
- Daily history levels (1-10, default: 5)
- Weekly history levels (1-10, default: 3)
- Show/hide labels and lines
- Date display toggle
- Line style selection
- Individual color controls for each level type

**Use Cases:**
- Monitor daily and weekly support/resistance levels
- Track price action relative to previous periods
- Identify breakout levels
- Plan entries and exits based on key price levels

For more details, see the [times-and-cycles directory](indicators/times-and-cycles/).

## Installation

1. Open TradingView and go to the Pine Editor
2. Copy the content of the desired indicator file (`.pine`)
3. Paste it into the Pine Editor
4. Click "Save" and give it a name
5. Click "Add to Chart"

## Requirements

- TradingView account
- Pine Script v6 compatible environment

## License

- **Pivot Measurements**: Uses LuxAlgo's pivot detection algorithm. See [LuxAlgo's original script](https://fr.tradingview.com/script/OxJJqZiN-Pivot-Points-High-Low-Missed-Reversal-Levels-LuxAlgo/) for pivot detection license details.
- Other components: See individual indicator files for license information.
