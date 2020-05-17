RentAcar!
------------------------------------
This NodeJS program simulates a car rental.

Currently live at: https://rent-a-car-live.herokuapp.com/

Getting Started
------------------
This program was created under Windows 10 (x64) Operative System using NodeJS 8.11.1 (+ ExpressJS 4.16.3),
  npm 6.1.0 and MySQL 5.7.14.

Prerequisites
---------------
In order to use the ExpressJS program it is highly necessary to have an *internet connection* and install:

	- NodeJS v8.11+ (includes npm v6.1+)
	- MySQL v5.7+

  i) Installing NodeJS v8.11+
    It is possible that NodeJS has been already installed, to check use the following code in the command line:

    $ node --version
    [v8.11.1]

    If errors occured or NodeJS has not yet been installed please visit their
    website http://nodejs.org/en/download/ and follow the instructions there.

    1) Installing npm v6.1+
      npm comes bundled with a successful NodeJS installation,
      to check use the following code in the command line:

      $ npm --version
      [v6.1.0]


  ii) Installing MySQL v5.7+

    In order to install the MySQL server on Windows it is very important to follow the instructions
    on their website http://dev.mysql.com/downloads/windows/.
    On windows there are various variables involved about having a MySQL server.
    For example to test the app, the program MySQL Workbench was used to monitor
    the dataflow and a Wamp server was used to simulate the actual server.

    Therefore, no real instructions can be provided here!!! If the instructions under the official website were
    followed a MySQL server should be working on the desired machine.

    It is very important to run the file *./db/db.sql* on the server after the installation is complete.
    Again, no example will be shown here but under Workbench everything should turn out great.


  iii) Testing
    In order to test the program it's necessary to run the app and check if no errors were presented.
    The most common errors could be:

    1) NodeJS port error
      This happens when the program tries to run on a busy port,
      if that happens it is recommended to change the port number under the file *./bin/www*
      15: let port = normalizePort(process.env.PORT || '3000');

      Where 3000 is the default port used by the program.

    2) MySQL database errors
      - If the file *./db/db.sql* was never ran against the server an error would be provided.
      - A locahost/password/port/user error could be given if the server has different configuration
      than provided by the file *./db/db.js* and each should be set appropriately.

    3) Any possible error
      Could be on the computer's end. Bad installation or wrong configuration.

      Aside from the errors mentioned above everything should be working normally.

Deployment
--------------
The program was created to be easy to use and it is fool proof (to a dreggre).
All user inputs return success or error messages.

Before starting. Please rename the file '.env.default' to '.env', and set in it your MySQL credentials.

In order to link all npm dependencies:

    ~/RentAcar> npm ln
    [*installation warnings*]

    [audited 173 packages in 1.253s]
    [found 0 vulnerabilities]

 In order to start the NodeJS server, execute:

    ~/RentAcar> npm start
    [Database connected.]

Then opening the (default) website on **Google Chrome**(*):

  localhost:3000

Files
------
/RentAcar:
  .env.default - please rename to .env and use your own MySQL credentials
  .gitignore - git file that helps ignoring other files
	LICENSE - license
	app.js - main program
	README.md - this readme
	package.json - npm config file

/RentAcar/auth:
	folder responsable for handling login information

/RentAcar/bin:
	www - main executable program file

/RentAcar/db:
	folder containing all database information, from its representaion to actual SQL file code

/RentAcar/node_modules:
	folder generated after a successufully "npm i" installation

/RentAcar/public:
	folder containing all additional files used, from javascripts to database images

/RentAcar/routes:
	folder containing all controller files used

/RentAcar/views:
	folder containing all "visible" files used by the user

Versioning
------------
Version 2.0 - Current version

Version 3.0(TBA) - Feature that allows to add new vehicles into the website

Version 5.5(TBA) - Real e-mail verification

Author
---------
Lucio Afonso

License
---------
This project is licensed under the GPL License - see the LICENSE.md file for details

Acknowledgments
----------------------
Official sites:

	http://npmjs.com/

	http://mysql.com/

	http://jquery.com/

	http://nodejs.org/

	http://expressjs.com/


Tutorials:

	http://w3schools.com/bootstrap/

	http://tutorialspoint.com/nodejs/

	http://mysqlclient.readthedocs.io/

	https://bit.ly/2N6J7Fc (code.tutsplus.com)
