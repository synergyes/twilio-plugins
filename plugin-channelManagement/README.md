# Manage worker Capacity from Flex!

![Channel Management](https://zaffre-cow-9057.twil.io/assets/Screen%20Shot%202019-02-06%20at%203.13.36%20PM.png)

## Setup

Make sure you have [Node.js](https://nodejs.org) as well as [`npm`](https://npmjs.com) installed.

Afterwards install the dependencies by running `npm install`:

```bash
cd plugin-channelManagement

# If you use npm
npm install
```

Edit your public/appConfig.js file;
- Replace the accountSid value with your Project Account SID.
- Replace the serviceBaseUrl value with you Runtime domain (without the https://).

Upload the Functions from the src/functions directory to your Twilio Functions.

Under Twilio / Functions / Configure, make sure you have added your TWILIO_WORKSPACE_SID to your environment variables.

## Development

In order to develop locally, you can use the Webpack Dev Server by running:

```bash
npm start
```

This will automatically start up the Webpack Dev Server and open the browser for you. Your app will run on `http://localhost:8080`. If you want to change that you can do this by setting the `PORT` environment variable:

```bash
PORT=3000 npm start
```

When you make changes to your code, the browser window will be automatically refreshed.

## Deploy

Once you are happy with your plugin, you have to bundle it, in order to deply it to Twilio Flex.

Run the following command to start the bundling:

```bash
npm run build
```

Afterwards, you'll find in your project a `build/` folder that contains a file with the name of your plugin project. For example `plugin-example.js`. Take this file and upload it into the Assets part of your Twilio Runtime.
