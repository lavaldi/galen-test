# Galen Test First Example

**Download the Selenium Server for Windows and Linux, and IEServer.exe**

http://www.seleniumhq.org/download/

*Into the proyect*

**Run the hub in Linux**

```java -jar /home/claudia/Downloads/selenium-server-standalone-2.46.0.jar -role hub -hubConfig selenium/hubConfig.json```

**Run the node in Windows**

```java -jar C:\selenium-grid-node\selenium-server-standalone-2.46.0.jar -role node -nodeConfig C:\selenium-grid-node\localNodeConfig-ie.json -Dwebdriver.ie.driver="C:\selenium-grid-node\IEDriverServer.exe" -hub http://%COMPUTER_IP%:4444/grid/register```

> :warning: Both machines (Linux and Windows, either physical or virtual) must be in the same network (try pinging between them).

**Run the test in Linux**

```galen test test/ -DwebsiteUrl="file:///home/claudia/htdocs/galen-test/website/index.html" --htmlreport reports```

> Change ```file:///home/claudia/htdocs/galen-test/website/index.html``` for the url of your page.