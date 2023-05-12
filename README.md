# WHMCS cPanel Email Usage #

[![GitHub Tests Action Status](https://img.shields.io/github/actions/workflow/status/eugenevdm/cpanel-email-usage/run-tests.yml?branch=main&label=tests&style=flat-square)](https://github.com/eugenevdm/cpanel-email-usage/actions?query=workflow%3Arun-tests+branch%3Amain)

## Summary ##

This module allows you to view the disk usage of your cPanel email accounts from within WHMCS.

## Installation

- Copy the files from `modules/servers/cpanelemailusage` to your WHMCS installation directory.
- Add new cPanel servers specifying cPanel Email Usage as the server type. No need to specify 2087 as port as it will assume that port number by default.

In WHMCS, all email accounts that's filled in the `domain` field will now start showing usage.

That also means that if you have overuse turned on, clients will be automatically billed.

## Screenshots

Client area showing client's email disk usage and disk limit:

![Client Area Resource Usage](/screenshots/client_area_resource_usage.png)

Admin area showing client's email disk usage and disk limit:

![Admin Area Disk Usage](/screenshots/admin_area_disk_usage.png)

## Development

```bash
cd /Users/username/Code/whmcs/modules/servers
ln -s /Users/username/Code/whmcs-modules/cpanel-email-usage/modules/servers/cpanelemailusage 
```

## Testing

### Usage Update Test

To test if the module is working, run the following command:

```bash
php -q /Users/username/Code/whmcs/crons/cron.php do --UpdateServerUsage
```

After go to the WHMCS UI and see if there is usage.

### Unit Tests

To test software, do this:

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.