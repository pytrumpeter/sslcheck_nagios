# sslcheck-nagios

This plugin can be used with Nagios to check for a certificate's expiration date.  If the expiration date is approaching and is within a configurable threshold, a warning will be issued.  If the certificate is expired, Nagios will show critical.

### Installing

Place in your Nagios plugins directory.  On a Nagios server running Linux, for me, this is /usr/local/nagios/libexec.

### Configuration

If you want the warning threshold to be something other than 30, set the WARNING_DAYS constant in the python file to whatever you desire. Of course, this is a global setting and will affect all instances of service monitoring that use this plugin.

In Nagios, configure a new command to use the plugin:

```
define command {
    command_name    check_ssl_certificate
    command_line    $USER1$/check_ssl_certificate -H $HOSTNAME$ -p $ARG1$
}
```

Now, to use this plugin on a specific host, add a service and use this command, with the following syntax: check_ssl_certificate -H [hostname] -p [port number]

## Contributing

Not much to this yet, so by all means, fork it and submit a PR if you like.  I'm pretty much open.

## Authors

* **Nick Harvey** - *Initial work* - James Madison University Libraries

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
