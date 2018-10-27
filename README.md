URLSCAN.IO API
==============

This module was created as the primary interface to urlscan.io for the gabne.ws URL shortener project. The urlscan.io service is used to scan submitted URLs for known hazards and reject those deemed to be hazardous.

## Getting Started

    $ npm install urlscan-api

This will install the `urlscan-api` module into your project and prepare it for use by also resolving it's dependencies.

In your script(s) that want to make use of `urlscan-api`, it must be required and set to a local constant or variable:

    const urlscan = require('urlscan-api');

## Initialize The API

Next, you have to initialize the module with your urlscan.io API key and other options as shown:

    var options = {
      apiKey: '########-####-####-####-############'
      public: true
    };
    var scanner = urlscan(options);

## Scan URLs

Now, you are ready to start scanning URLs with the urlscan.io API:

    scanner
    .scanUrl(url)
    .then((result) => {
      console.log('URL scan result', result);
    })
    .catch((error) => {
      console.log('URL scan error', error);
    });