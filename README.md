# react-ts-ddyckt

[Edit in StackBlitz next generation editor ⚡️](https://stackblitz.com/~/github.com/charleslin220/react-ts-ddyckt)


Overview of Streaming Data Visualization Application. 
Author: Charles (Jie Lin)
Date: 12 Jan 2024

The Streaming Data Visualization application is designed to showcase real-time financial data using React and Highcharts. The application consists of several key components, orchestrated to provide a dynamic and interactive user experience.

Key Components:

1. TradeDataProvider (Context Provider)

  This component sets up a React context for managing and distributing trade data throughout the application. It encapsulates two main pieces of state: tradeData and highLowValues.
  tradeData stores an array of trade information, including price, size, and trade side (buy/sell).
  highLowValues holds calculated metrics such as the highest/lowest buy price, sell price, and trade size.
  The context provides updateTradeData, a function used to update these state values.

2. WebSocketComponent

  Establishes a WebSocket connection to receive real-time trade data.
  Processes incoming data and updates the application's state via the updateTradeData method provided by TradeDataProvider.
  Handles connection status, displaying whether the WebSocket is connected or disconnected.

3. ChartComponent

  Utilizes Highcharts to visualize the trade data.
  The chart dynamically updates to display data from the last 60 seconds.
  Series in the chart represent different aspects of the trade data, such as buy price, sell price, and trade size.

4. Highcharts Configuration

  Configured to display time-series data.
  Supports interactive features like zooming and tooltips.
  Customized to enhance readability, such as differentiating series through colors and styles.

5. Styling and Layout

  The application employs CSS for styling, enhancing readability and user experience.
  Includes responsive design elements to ensure usability across various devices and screen sizes.
6. Responsive Table for High/Low Values

  Displays the high and low values of trade metrics in a tabular format.
  Styled to align with the dark theme of the application.

Functionality:

- The application visualizes live financial data streamed via WebSocket, allowing users to view up-to-date market trends.
- The data is presented in an interactive chart, where users can explore different aspects of the data through various series.
- The application maintains the latest 60 seconds of data, ensuring the visualization remains relevant and current.
- High and low values of the data are calculated and displayed, providing quick insights into market extremes.

Dependencies:

React
Typescript
Highcharts
WebSocket API
CSS