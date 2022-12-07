# CS 410 Final Project

This project was created to analyze local sentiment about weather in selected cities,
using both the Twitter API and National Weather Service API. This project leverages Flask and D3.js.

In order to run the application, you need Python and Node/NPM installed on your machine.

Project was created using:

Python 3.10.5
Node 19.2.0
NPM 8.9.13

For information on installing Node and NPM you can look here:

https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

Keep in mind a Node version needs to be activated after installing, otherwise the npm command will not work.

To clone the repository run the following from the command line:
```
git clone https://github.com/josh-monto/weather_sent.git
```

I have included a bearer token for the Twitter API generated from a secondary developer account to ease the process of deploying the application. I don't expect rate limits to be hit, as the application is not a heavy user of data, but in case that does happen let me know.

This bearer token will be removed once evaluation for the project is over.

From this point forward it is recommended to run a virtual environment (https://docs.python.org/3.10/library/venv.html). Flask will not function if it is not installed and run from a virtual environment

Now, with Node and NPM installed (and activated), repository cloned, and virtual environment activated, navigate to the project root folder in the command line and run the following commands to install d3 (must be version 4) and all Python packages:

```
npm install --save d3
pip install flask tweepy noaa_sdk vaderSentiment pandas rank_bm25
```

Now run the project:

```
python -m flask run
```

Once the message `Running on http://127.0.0.1:5000` appears, navigate to http://127.0.0.1:5000 in a browser window. The page may take up to 15 seconds to open.

Once the page opens, you can select a city from the dropdown menu and click Submit once (the Submit button does not currently deactivate while code runs). Wait up to 15 seconds for the page to update with information for the selected city.