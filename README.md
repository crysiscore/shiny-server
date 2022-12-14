# Shiny Server

Shiny Server is a server program that makes [Shiny](https://rstudio.com/shiny) applications available over the web.

## Features

* Host multiple Shiny applications, each with its own URL
* Can be configured to allow any user on the system to create and deploy their own Shiny applications
* Supports non-websocket-capable browsers, like IE9
* Free and open source ([AGPLv3](http://www.gnu.org/licenses/agpl-3.0.html) license)
* Pre-built installers for select Linux distributions.



## Configuration

Shiny Server will use the [default configuration](https://github.com/rstudio/shiny-server/blob/master/config/default.config) unless an alternate configuration is provided at `/etc/shiny-server/shiny-server.conf`. Using the default configuration, Shiny Server will look for Shiny apps in `/srv/shiny-server/` and host them on port 3838. If you plan to host your apps in this directory, you can either copy an app you've already developed to that location:

```
sudo cp -R ~/MY-APP /srv/shiny-server/
```

Or you can copy some or all of the examples provided with the Shiny package. (The location of the R library varies from system to system. You can use the command `R -e ".libPaths()" --quiet` to print the directory of the R library.) For instance, on Ubuntu, you could execute `cp -R /usr/local/lib/R/site-library/shiny/examples/* /srv/shiny-server/`.

Now start a web browser and point it to `http://<hostname>:3838/APP_NAME/`

**If the browser is not able to connect to the server, configure your server's firewall to allow inbound TCP connections on port 3838.**

To customize any of the above, or to explore the other ways Shiny Server can host Shiny apps, see the [Shiny Server Configuration Reference](https://rstudio.github.io/shiny-server/latest/#configuration-settings) for details on the various ways Shiny Server can be configured.

## Documentation & Contact & Support

See [the Administrator's Guide to Shiny Server](https://rstudio.github.io/shiny-server/latest/) for more complete documentation regarding the setup and management of Shiny Server.

Please direct q
