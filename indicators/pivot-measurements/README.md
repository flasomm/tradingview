# [FS] Pivot Measurements

An advanced TradingView indicator that combines LuxAlgo's pivot point detection algorithm with automatic measurement calculations between consecutive pivots.

## Features

### Pivot Detection
- **Regular Pivots**: Detects standard pivot highs and lows using configurable pivot length
- **Missed Pivots**: Identifies missed reversal levels that occurred between regular pivots
- **Visual Indicators**:
  - Regular pivot highs: Red downward triangle (▼)
  - Regular pivot lows: Teal upward triangle (▲)
  - Missed pivots: Ghost emoji (👻)
- **Zigzag Lines**: Connects pivots with colored lines (solid for regular, dashed for missed)
- **Ghost Levels**: Horizontal lines indicating missed pivot levels

### Measurement System
- **Automatic Measurements**: Calculates price movements between consecutive pivots
- **Visual Display**:
  - Transparent colored boxes (blue for upward, red for downward movements)
  - Measurement labels showing:
    - Price change (absolute and percentage)
    - Duration (bars, days, hours, minutes)
    - Volume approximation
- **Smart Positioning**: Labels positioned outside boxes (above for upward, below for downward)
- **Color Coding**: Blue for positive movements, red for negative movements

## Parameters

### Pivot Detection
- **Pivot Length** (default: 50): Number of bars on each side to identify a pivot point
- **Regular Pivots**: Toggle and colors for regular pivot highs and lows
- **Missed Pivots**: Toggle and colors for missed pivot detection

### Measurements
- **Number of Measurements** (1-10, default: 10): Maximum number of measurements to display
- **Show Measurement Boxes**: Toggle to show/hide measurement boxes and labels
- **Box Transparency** (0-100, default: 90): Transparency level for measurement boxes
- **Border Transparency** (0-100, default: 50): Transparency level for box borders
- **Label Background Transparency** (0-100, default: 30): Transparency level for label backgrounds
- **Label Size**: Size of measurement labels (tiny, small, normal, large)

## Usage

1. Add the indicator to your chart
2. Configure the **Pivot Length** based on your timeframe:
   - Lower values for shorter timeframes (e.g., 10-20 for 1-5 min)
   - Higher values for longer timeframes (e.g., 50-100 for daily)
3. Adjust pivot colors and visibility as needed
4. Customize measurement display settings:
   - Set the number of measurements to display
   - Adjust transparency levels for boxes, borders, and labels
   - Choose label size

## Technical Details

- **Pine Script Version**: v6
- **Pivot Detection**: Based on [LuxAlgo's Pivot Points High Low & Missed Reversal Levels](https://fr.tradingview.com/script/OxJJqZiN-Pivot-Points-High-Low-Missed-Reversal-Levels-LuxAlgo/) algorithm for detecting regular and missed pivots
- **Measurement Calculation**:
  - Measures between consecutive pivots (from most recent to older)
  - Calculates price change, percentage change, duration, and approximate volume
  - Automatically sorts pivots chronologically
- **Performance**: Optimized with helper functions to reduce code duplication

## Notes

- The indicator automatically limits the number of stored pivots to optimize performance
- Measurements are only created when there are at least 2 pivots detected
- All measurements are recalculated on each bar update
- The indicator uses `max_bars_back=5000` to ensure sufficient historical data

## License

This indicator uses LuxAlgo's pivot detection algorithm from [Pivot Points High Low & Missed Reversal Levels](https://fr.tradingview.com/script/OxJJqZiN-Pivot-Points-High-Low-Missed-Reversal-Levels-LuxAlgo/). Please refer to the original LuxAlgo license for pivot detection components.

