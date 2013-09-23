Opauth-Fitbit
=============
[Opauth][1] strategy for Fitbit, implemented based on https://wiki.fitbit.com/display/API/OAuth+Authentication+in+the+Fitbit+API using OAuth 1.

Opauth is a multi-provider authentication framework for PHP.

Getting started
----------------
1. Install Opauth-Fitbit:
   ```bash
   cd path_to_opauth/Strategy
   git clone git://github.com/bickart/opauth-fitbit.git Fitbit
   ```

2. Create Fitbit application at https://dev.fitbit.com/
   - Enter your domain at JavaScript API Domain
   - There is no need to enter OAuth Redirect URL

3. Configure Opauth-Fitbit strategy with `consumer_key` and `consumer_secret`.

4. Direct user to `http://path_to_opauth/fitbit` to authenticate

Strategy configuration
----------------------
Required parameters:

```php
<?php
'Fitbit' => array(
    'consumer_key' => 'YOUR API KEY',
    'consumer_secret' => 'YOUR SECRET KEY'
),
```

Note: To obtain email, include `r_emailaddress` to `scope`, eg.: `'scope' => 'r_basicprofile r_emailaddress'`.

See FitbitStrategy.php for more optional parameters.


License
---------
Opauth-Fitbit is MIT Licensed
Copyright © Jeff Bickart (http://neposystems.com)

[1]: https://github.com/uzyn/opauth
