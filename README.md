# Using local Node and Yarn

By default, vaadin-maven-plugin downloads and installs Node and Yarn from the internet. This behavior can be overridden and the plugin can use locally installed Node and Yarn.

In order to do this, nodePath and yarnPath parameters should be specified in the plugin configuration:

pom.xml com.vaadin flow-maven-plugin 1.1.0.beta4 /usr/local/Cellar/node/10.8.0/bin/node /usr/local/Cellar/yarn/1.9.4/bin/yarn copy-production-files package-for-production

Note In order to use locally installed tools, both paths should be specified. If any of the paths is not specified, both tools will be downloaded. If both versions and paths are specified, paths are used.

https://github.com/vaadin/flow/releases

Here you can find a test repository with the configuration of the flow-maven-plugin:

https://github.com/DiegoSanzVi/example-flow-maven-plugin

mvn clean install -Dvaadin.productionMode mvn clean package -PproductionMode

If you have any feedback, do not hesitate to send it to me.

