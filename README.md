Advanced indicator for the **Quantower** platform that displays gamma points on the chart in real-time, with local SQLite database support and synchronization via the GexBot.com API.

## 📋 Description

GexBot Gamma Point is a powerful indicator that visualizes critical gamma levels as points on your chart. The indicator combines historical data stored in a local SQLite database with real-time data from the GexBot.com API. It works exclusively during the US market cash session (9:30-16:00 ET) and displays up to 10 different point series with a comprehensive legend.

## ✨ Features

### 🎯 Displayed Data Types
- **Zero Gamma** : Zero gamma level (classic/zero)
- **Major Positive/Negative (Volume)** : Major levels based on volume (classic/zero)
- **Major Positive/Negative (Open Interest)** : Major levels based on open interest (classic/zero)
- **Net (calculated)** : Calculation based on spot + (major_pos - |major_neg|) / 100
- **Major Long/Short Gamma** : Long/short gamma levels (state/gamma)
- **Major Positive/Negative** : Major positive/negative levels (state/gamma)

### 💾 Local Storage
- **SQLite Database** : Local storage in `C:\Quantower\GexBot`
- **Automatic Loading** : Loads historical data for the last N days
- **Real-time Persistence** : Automatically saves new API data
- **Multi-day Management** : Support for multiple days of data

### 📊 Visualization
- **Chart Points** : Display of colored points for each level
- **Complete Legend** : Configurable information table with all values
- **Statistics** : Display of Net GEX, Net GEX OI and Delta Reversal
- **Customization** : Fully configurable colors, sizes and positions

### ⚙️ Technical Features
- **Cash session only** : Works only during 9:30-16:00 ET (with DST handling)
- **Automatic Updates** : Periodic synchronization with GexBot API
- **Price Multiplier** : Price adjustment with configurable multiplier
- **10 Data Series** : Support for 10 different series simultaneously

## 🚀 Installation

Copy the compiled DLL file to the Quantower indicators folder :
   ```
   C:\Quantower\Settings\Scripts\Indicators\GexBot
   ```
Restart Quantower

## ⚙️ Configuration

### Required Parameters
- **API Key** : GexBot.com API key (get it on [gexbot.com](https://gexbot.com))
- **Ticker** : Symbol to analyze (e.g.: NQ_NDX, SPX, SPY)
- **Days to Load** : Number of historical data days to load (1-30, default: 5)
- **Refresh Interval** : API refresh interval in seconds (5-300, default: 30)

### Display Parameters
- **Point Size** : Size of points on the chart (1-10, default: 3)
- **Price Multiplier** : Multiplier to adjust prices (0.01-100.0, default: 1.0)

### Chart Display
Enable/disable each point series individually :
- Chart: Zero Gamma
- Chart: Major + (Vol)
- Chart: Major - (Vol)
- Chart: Major + (OI)
- Chart: Major - (OI)
- Chart: Net (calc)
- Chart: Major Long Gamma
- Chart: Major Short Gamma
- Chart: Major Positive
- Chart: Major Negative

### Legend Display
Enable/disable each value in the legend individually :
- Legend: Zero Gamma
- Legend: Major + (Vol)
- Legend: Major - (Vol)
- Legend: Major + (OI)
- Legend: Major - (OI)
- Legend: Net (calc)
- Legend: Major Long Gamma
- Legend: Major Short Gamma
- Legend: Major Positive
- Legend: Major Negative

### Colors
Customize colors for each series :
- Color: Zero Gamma
- Color: Major + (Vol)
- Color: Major - (Vol)
- Color: Major + (OI)
- Color: Major - (OI)
- Color: Net
- Color: Long Gamma
- Color: Short Gamma
- Color: Major Positive
- Color: Major Negative

### Legend Parameters
- **Show Legend** : Display the legend
- **Legend: Show Stats** : Display statistics (NetGEX/DRR)
- **Legend X/Y** : Legend position in pixels
- **Legend Font Size** : Font size
- **Legend Value Decimals** : Number of decimals for values
- **Legend Background** : Display legend background
- **Legend Background Alpha** : Background transparency (0-255)
- **Legend Text Color** : Text color

## 📖 Usage

1. Open a chart in Quantower
2. Add the "GexBot_Gamma_Point_V1" indicator from the indicators list
3. Configure your API Key and ticker
4. Adjust display parameters according to your preferences
5. The indicator will automatically load historical data from the local database
6. New data will be fetched via API according to the configured interval


<img width="2554" height="1260" alt="image" src="https://github.com/user-attachments/assets/ee20fe39-ccb9-4d2b-b8a8-e72beee11848" />

<img width="1125" height="871" alt="image" src="https://github.com/user-attachments/assets/40482c4d-ffac-4c01-a1f5-6340682aca70" />

<img width="2527" height="1268" alt="image" src="https://github.com/user-attachments/assets/51b23d17-8f9f-49f9-8de5-c235f8a31ebb" />


