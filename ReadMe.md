Install the webDriver nmanager to mange broser drivers
  pip install webdrivermanager

 Manage the browser drivers
 webdrivermanager firefox chrome --linkpath D:/BrowserDrivers


Links to some of the more popular browser drivers follow.

Chrome:	https://chromedriver.chromium.org/downloads
Edge:	https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
Firefox:	https://github.com/mozilla/geckodriver/releases

Safari:	https://webkit.org/blog/6900/webdriver-support-in-safari-10/

 
Start the local server

python demoapp/server.py

 Verify with http://localhost:7272


 Running tests
The test cases are located in the login_tests directory. They can be executed using the robot command:

robot login_tests

 



also run an individual test case file and use various command line options supported by Robot Framework:

robot login_tests/valid_login.robot
robot --test InvalidUserName --loglevel DEBUG login_tests

Using different browsers
The browser that is used is controlled by ${BROWSER} variable defined in resource.robot resource file. Firefox browser is used by default, but that can be easily overridden from the command line:

robot --variable BROWSER:Chrome login_tests
robot --variable BROWSER:IE login_tests
