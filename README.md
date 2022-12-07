# CS 410 Final Project

The video presentation can be found here: https://uofi.box.com/s/palrjvvnq8ifucwd66v6xzlhxgc3tw0t

The full documentation submission is found in the Final Project Documentation PDF

Instructions for running application can be found below.

This project was created to analyze local sentiment about weather in selected cities,
using both the Twitter API and National Weather Service API. This project leverages Flask and D3.js.

In order to run the application, you need Python and Node/NPM installed on your machine.

The project was created using:

Python 3.10.5

Node 19.2.0

NPM 8.9.13

For information on installing a Node Version Manager (NVM) as well as Node and NPM you can look here:

https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

Keep in mind a Node version needs to be activated (using command nvm use ...) after installing, otherwise the npm command will not work.

To clone the repository run the following from the command line:
```
git clone https://github.com/josh-monto/weather_sent.git
```

A bearer token must be added to a 'bearer_token.txt' file in the root folder of this project to access the Twitter API. I have included a bearer token from a secondary developer account for project evaluation, but I will revoke it once evaluation is over. After that, a token can be generated once a Twitter developer account is created. Instructions here:

https://developer.twitter.com/en/docs/authentication/oauth-2-0/bearer-tokens

I didn't need a token for the NWS API.

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
