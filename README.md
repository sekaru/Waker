# Waker
The general workflow of Waker is:
* Call server endpoint to return the host and port(s) of a server
* After returning the server info, check to see if it's up
* If it isn't, post a status on the Twitter bot (limited to every half hour)

## Libraries
* [service-checker](https://www.npmjs.com/package/service-checker): used to check if a server is up (using rawTcp)
* [twit](https://www.npmjs.com/package/twit): twitter bot framework
* [express](https://www.npmjs.com/package/express): basic REST server
* [dotenv](https://www.npmjs.com/package/dotenv): storing config options as process environment variables
* [geoip-lite](https://www.npmjs.com/package/geoip-lite): getting physical server locations for [Eyes](https://github.com/sekaru/eyes)
* others: [moment](https://www.npmjs.com/package/moment), [log4js](https://www.npmjs.com/package/log4js), [lodash](https://www.npmjs.com/package/lodash)

## Make it your own
Clone the project and `npm install`

Make a Twitter app at: https://apps.twitter.com

In your root folder, create a '.env' file (or copy and rename the .env.template file) and fill in these properties:

```
T_CONSUMER_KEY=yourtwitterconsumerkey
T_CONSUMER_SECRET=yourtwitterconsumersecret
T_ACCESS_TOKEN=yourtwitteraccesstoken
T_ACCESS_TOKEN_SECRET=yourtwitteraccesstokensecret
MAX_GIFS=8
STATUS_INTERVAL=30
PORT=8000
```

