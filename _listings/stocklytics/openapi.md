swagger: "2.0"
x-collection-name: Stocklytics
x-complete: 1
info:
  title: Stocklytics Intraday Historical Stock Prices API
  description: the-intraday-historical-prices-api-allows-you-to-get-a-list-of-the-price-for-a-particular-stock-for-the-current-day-or-the-latest-day-of-trading-if-markets-are-closed-in-5-minute-intervals--this-data-is-perfect-for-generating-intraday-stock-graphs-or-performing-stock-analysis-in-near-realtime--data-for-this-api-is-updated-every-5-minutes-
  version: v1
host: api.stocklytics.com
basePath: /services/pressroom/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  historicalPrices/{API_VERSION}/:
    get:
      summary: Historical Prices
      description: The Historical Prices API can be used to look up the Open, Close,
        High and Low price, as well as the volume of stock traded for a stock code
        within a particular date range. The API supports the downloading the entire
        historical data set we have on file for a stock, we index data for a stock
        with a start date of January 1st 1980.
      operationId: getHistoricalpricesApiVersion
      x-api-path-slug: historicalpricesapi-version-get
      parameters:
      - in: query
        name: api_key
        description: Allows us to identify the request initiator
      - in: path
        name: API_VERSION
        description: Version of the API
      - in: query
        name: end
        description: The start and end dates to return data for
      - in: query
        name: format
        description: Format of returned data
      - in: query
        name: order
        description: Order of returned data sorted by date
      - in: query
        name: start
        description: The start and end dates to return data for
      - in: query
        name: stock
        description: The stock code/ticker for the stock to look up
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Prices