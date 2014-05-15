# sabre-dev-studio

NodeJS wrapper for the Sabre Dev Studio API

## Getting Started
Install the module with: `npm install sabre-dev-studio`

    var SabreDevStudio = require('sabre-dev-studio');
    var sabre_dev_studio = new SabreDevStudio({
      user:     'USER',
      group:    'GROUP',
      domain:   'DOMAIN',
      password: 'PASSWORD',
      uri:      'https://api.test.sabre.com'
    });
    var options = {};
    var callback = function(error, data) {
      if (error) {
        console.log(error);
      } else {
        console.log(JSON.parse(data));
      }
    };
    sabre_dev_studio.get('/v1/shop/themes', options, callback);

## Documentation

See http://developer.sabre.com

## Examples

### Using the Flight API:

    var SabreDevStudioFlight = require('sabre-dev-studio-flight');
    var sabre_dev_studio_flight = new SabreDevStudioFlight({
      user:     '8987',
      group:    'STPS',
      domain:   'EXT',
      password: 'uR9gFO02',
      uri:      'https://api.test.sabre.com'
    });
    var callback = function(error, data) {
      if (error) {
        // Your error handling here
        console.log(error);
      } else {
        // Your success handling here
        console.log(JSON.parse(data));
      }
    };
    sabre_dev_studio_flight.travel_theme_lookup(callback);
    sabre_dev_studio_flight.theme_airport_lookup('BEACH', callback);

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_

## License
Copyright (c) 2014 Barrett Clark  
Licensed under the MIT license.
