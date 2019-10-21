# Data Engineering Quiz

## Overall Goal

Welcome!  This is the Penn Engineering code challenge.

We hope you find this challenge interesting. We won't provide any kind of starter code, so feel free to configure your own environment to achieve the proposed goals.  You should limit this exercise to no more than an hour or two.  The goal is to test your familiarity with building pipelines and ETL processes.

### Expectations

The goal of this exercise is to develop a simple ETL process for pulling in historical data about several cryptocurrencies and exposing features from the dataset through an API.  You will be consuming data from the [CoinAPI.io](https://coinapi.io/) service, persisting it in a database, transforming the data to fit your schema, and exposing certain queries through a simple API.

Once you're done and commit your results to a VCS such as Github, Bitbucket, or Gitlab.

Provide a link to your repo so that we can review the code.  Instructions for running the code should be provided as well in a `README` file.

### Getting started

- **API Key**: The [CoinAPI.io](https://coinapi.io/) service requires a key to allow you to launch queries, so you'll have to create an API key to proceed.
- **Free Account**: If you check out the [API Pricing](https://www.coinapi.io/pricing), you'll see that the free accounts have a limitation of 100 daily requests. You'll address this limitation as part of the challenge, but keep in mind that you have this daily limit while fetching the information.


### Part One

To start off we're going to need to ingest data from [CoinAPI.io](https://coinapi.io/).  In order to do this you'll need to do the following

-  Register for a free account for [CoinAPI.io](https://coinapi.io/) and get an API key
-  Create a script to take in a cryptocurrency symbol
-  With the cryptocurrency symbol pull the last years worth of data for the cryptocurrency
-  Persist the data in a database of your choosing.  Bonus points for using Postgres

We're going to fetch historical price data for the following coins:

* Bitcoin (`BTC`)
* Ethereum (`ETH`)
* Ripple (`XRP`)
* Dogecoin (`DOGE`)

Once the data has been written to the database for each coin we can move onto Part Two.


### Part Two

Now that we have our data organized in our database you're going to expose it through an API.  The API should support the following two of queries on any coin

* Fetch daily differences in coins between two arbitrary dates
* Fetch average hi/low price points between two arbitrary dates
* Show the N best opening dates for a coin where N in an integer between 1 and 5 inclusive

You can also add any other API endpoints you'd like to expose.

Commit your code, and send us a link!
