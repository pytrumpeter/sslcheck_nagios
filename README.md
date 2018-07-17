# nagios-sslcert-plugin

This plugin can be used with Nagios to check for a certificate's expiration date.  If the expiration date is approaching and is within a configurable threshold, a warning will be issued.  If the certificate is expired, Nagios will show critical.

### Installing

Place in your Nagios plugins directory.  On a Nagios server running Linux, for me, this is /usr/local/nagios/libexec.

### Configuration

If you want the warning threshold to be something other than 30, set the WARNING_DAYS constant in the python file to whatever you desire. Of course, this is a global setting and will affect all instances of service monitoring that use this plugin.

In Nagios, configure a new command to use the plugin:

BLAH

Now, to use this plugin on a specific host, add a service and use this command, with the following syntax: check_ssl_cert -H [hostname] -p [port number]

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

