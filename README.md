# Galen Test First Example

*Into the proyect*

**Run the hub**

```java -jar /home/claudia/Downloads/selenium-server-standalone-2.46.0.jar -role hub -hubConfig selenium/hubConfig.json```

**Run the node**

```java -jar /home/claudia/Downloads/selenium-server-standalone-2.46.0.jar -role node -nodeConfig selenium/localNodeConfig.json -Dwebdriver.chrome.driver="/home/claudia/Downloads/chromedriver"```

**Run the test**

```galen test test/ -DwebsiteUrl="file:///home/claudia/htdocs/galen-test/website/index.html" --htmlreport reports```

> Change ```file:///home/claudia/htdocs/galen-test/website/index.html``` for the url of your page.