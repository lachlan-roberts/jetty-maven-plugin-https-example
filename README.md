# Demo of using HTTPS with the Jetty Maven Plugin

### Using `mvn jetty:run-distro` with a jetty-base directory.
This goal works by having a preconfigured jetty-base directory referenced in the jetty-maven-plugin configuration with `<jettyBase>`.

This allows you to do the configuration as you would with jetty standalone with ini files, and avoid writing xml files.

To add more modules just `cd` to the jetty-base directory and go `java -jar $JETTY_HOME/start.jar --add-to-start=ssl,https` to create the `.ini` files that you can edit.

See https://www.eclipse.org/jetty/documentation/current/quick-start-configure.html


### Using `mvn jetty:run` with xml files.
With this goal you need to copy over all the xml configuration files to set up HTTPS.

Here I have copied `jetty.xml`, `jetty-https.xml`, `jetty-ssl.xml` directly from jetty-home `etc/` directory and left them unchanged.

The configuration for the keystore is all done in the `jetty-ssl-context.xml` file.