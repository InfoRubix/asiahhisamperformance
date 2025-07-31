# Performance & Effectiveness Dashboard

**Made by RUBIX TECHNOLOGY**

A comprehensive web-based dashboard for analyzing team and individual performance metrics based on file management data.

## Features

### Overall Performance Dashboard
- **Key Performance Indicators (KPIs)**
  - Total Active Files
  - Files Closed (Last 30 Days)
  - Files Closed (All Time)
  - Average Closing Time (Days)

- **Visual Analytics**
  - PIC Leaderboard showing active file distribution
  - Monthly performance trends with customizable time ranges (Quarter/6 Months/Year)

### Individual Analysis
- **Personal Performance Metrics**
  - Individual active file counts
  - Personal average closing times
  - Total files closed per person

- **Detailed File History**
  - Complete file tracking with reference numbers
  - Open and close dates
  - Duration calculations

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **Charts**: Chart.js
- **Data Processing**: Papa Parse (CSV parsing)
- **Fonts**: Inter (Google Fonts)
- **Data Source**: Google Sheets integration

## Setup & Installation

1. Clone or download the project files
2. Ensure you have a web server environment (Apache, Nginx, or similar)
3. Place the files in your web server directory
4. Open `index.html` in a web browser

### Data Source Configuration

The dashboard reads data from a Google Sheet via CSV export. Update the `GOOGLE_SHEET_URL` variable in the JavaScript section to point to your data source:

```javascript
const GOOGLE_SHEET_URL = 'your-google-sheet-csv-url-here';
```

## Data Format Requirements

The dashboard expects CSV data with the following columns:
- `PIC` - Person in Charge
- `REF NUM` - Reference Number
- `DOF` - Date of Filing (Date Opened)
- `DATE CLOSE` - Date Closed
- `STAGES` - Current Stage

Supported date formats:
- `DD-MMM-YYYY` (e.g., 15-Jan-2024)
- `DD/MM/YYYY` (e.g., 15/01/2024)

## Features in Detail

### Navigation
- Toggle between "Overall Performance" and "Individual Analysis" views
- Responsive design optimized for desktop and mobile devices

### Data Processing
- Automatic exclusion of system accounts ('SPA QHomes', 'Loan QHomes', 'Loan')
- Real-time calculation of file durations
- Dynamic filtering and sorting capabilities

### Performance Metrics
- Active file tracking
- Time-based performance analysis
- Comparative analytics across team members

## Browser Compatibility

- Modern browsers with ES6+ support
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Development

The application is built as a single-page application (SPA) with vanilla JavaScript. Key components:

- **Data Processing**: CSV parsing and transformation
- **Visualization**: Chart.js integration for interactive charts
- **UI Components**: Custom styled components with Tailwind CSS
- **State Management**: Simple JavaScript object-based state

---

## License & Terms

This software is proprietary to RUBIX TECHNOLOGY. Unauthorized reproduction, distribution, or modification is prohibited. For licensing inquiries, please contact RUBIX TECHNOLOGY directly.

---

**© 2025 RUBIX TECHNOLOGY. All right reserved.**