# Trucknet

These are the static html pages at the document root for the Library of Approximate Location Trucknet network.

These are not meant to be used on their own, and should be setup alongside <https://github.com/charliemacquarie/sevenandahalf/> to work as intended.

Once setup, library materials can be added to a directory that must be named `storage` at the document root. The directory can contain any number of subdirectories to help organize materials logically. Please note though, that maps meant to be accessed through `sevenandahalf` ("Where am I?" on the homepage) must be set up using the process built in to <https://github.com/charliemacquarie/sevenandahalf/>

## Setup
(this is basic stuff, but I forget every time)

At the document root (/var/www/html/), delete the default index.html from Apache2:
> bash:
```
sudo rm -rf index.html
```

Still at the document root (/var/www/html/), clone the trucknet repository into place:
> bash:
```
sudo git clone https://github.com/charliemacquarie/trucknet .
```

Edit the main apache2 config file to allow .htaccess override for directory styling. In /etc/apache2/apache2.conf, under `<Directory "/var/www">`, replace `AllowOverride None` with `AllowOverride All`.
