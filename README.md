After clone repo open pom.xml and change path to JDK in maven-compiler-plugin

For run tests you need:
- JVM
- JDK
- Maven

For run open repo in consol and run command:
mvn test

HowTo: setup env for tests run (main source -  https://www.edgewordstraining.co.uk/2018/05/31/intellij-with-cucumber-and-selenium-webdriver-java/ +  https://www.mkyong.com/maven/how-to-install-maven-in-windows/ )
1. Install JDK - http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html (tesed with jdk1.8.0_191)
1.2. Add a Windows environment variable (system properties, WinKey + Pause -> Advanced System Settings -> Environment Variables) JAVA_HOME to point at the JDK directory, verify in CMD with echo %JAVA_HOME% and java -v

2. Maven Install - https://maven.apache.org/download.cgi Add the path to the \bin folder of the Maven install to the Windows PATH environment variable (system properties, WinKey + Pause -> Advanced System Settings -> Environment Variables) Open a new command prompt (Winkey + R then type cmd) and run mvn -v to verify the installation. (tested with Apache Maven 3.6.0)

3. Check ChromeDriver variable (Winkey + R then type cmd and run):
ChromeDriver
expected result like:
Starting ChromeDriver 2.42.591088 (7b2b2dca23cca0862f674758c9a3933e685c27d5) on port 9515
else - https://developers.thomsonreuters.com/sites/default/files/How%20To%20Add%20ChromeDriver%20To%20System%20Variables_0.pdf
or download actual http://chromedriver.chromium.org/downloads than (for Windows) unpack and move file chromedriver.exe to folder C:\chromedriver and add ENV variable path value "C:\chromedriver" (+restart OS)

