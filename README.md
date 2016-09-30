# README #

### Author: Harpreet Dhillon , harpreet@uoregon.edu ###
 
### Application Specifics ###
* The webserver will automatically transmit any .html or .css files that are currenly in the ./pages/ directory.
* Any subdirectories within the ./pages/ directory will also be considered valid paths when attempting to reach it by url.
* The application will return one of four status upon each connection:
  ** 200 - Everything is OK
  ** 401 - Not implemented
  ** 403 - Forbidden (if the url contains '//', '..', or '~' or if the page you are trying to reach is not a html or css page)
  ** 404 - Not found


### Running the Application ###
* Test deployment to other environments including Raspberry Pi.  Deployment 
  should work "out of the box" with this command sequence: 
  ** git clone <yourGitRepository> <targetDirectory>
  ** cd <targetDirectory>
  ** make configure
  ** make run 
  ** (control-C to stop program)
* The default port is 8000, so the webserver should be reachable at http://127.0.0.1:8000
* 'Out of the box' the only page available is trivia.html which is reachable at http://127.0.0.1:8000/trivia.html
 
### Testing the Applicaiton ###
* There is a default test shell script in the ./tests/ directory named 'tests.sh'.
* Usage:
 ** ./tests.sh http://127.0.0.1:8000
* Assuming you have already started the webserver in another terminal, the tests script will attempt to get a list of pages and return the output vs. expectation
