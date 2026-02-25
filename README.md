# CryptoInfo

CryptoInfo is an interactive web app that retrieves, analyzes, and visualizes cryptocurrency data.

The development was split into 4 phases.

## Part 1

- **Software Requirements Specification (SRS)**
- **Pipe-and-filter architecture** that aggregates current and historic data for the top cryptocurrencies. The pipeline consists of 4 filters that each perform a separate task: scraping the top currencies, checking the last-updated date in the database, scraping only the missing data, and updating the database, respectively

## Part 2

- **Conceptual, execution, and implementation diagrams** for the application
- **GUI mockups**
- **Technical prototype** — a web app using Spring Boot for the backend and React for the frontend, covering only some of the basic requirements

## Part 3

- **Technical analysis** using oscillators (RSI, MACD, CCI, etc.) and moving averages (SMA, EMA, WMA, etc.) as indicators, calculated with the `ta` and `pandas_ta` libraries on top of the historic data collected in Part 1
- **LSTM model** for predicting prices based on historic data for each coin, with predictions stored in the database
- **On-chain analysis** — aggregating on-chain metrics (whale movements, hash rate, TVL, etc.) from several APIs
- **Sentiment analysis** — scraping crypto-related articles and performing sentiment analysis using NLP techniques
- Full-stack web app (Spring Boot + React) integrating all of the above

## Part 4

- Code refactoring and application of design patterns
- Decoupling functionality into a separate FastAPI microservice that, once triggered, fetches new crypto-related articles, performs sentiment analysis, and stores the results in a database
- Containerizing the entire application with Docker and hosting it on Microsoft Azure


## Demo
A demo of the finished application can be seen [here](https://gitlab.finki.ukim.mk/231136/crypto-info/-/blob/main/%D0%94%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B0%204/application-dockerized-demo.mov?ref_type=heads).
