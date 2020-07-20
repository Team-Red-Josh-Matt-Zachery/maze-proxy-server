## proxy-server
To run all 4 services, RUN: npm start --> this script runs: npm run concurrently and nodemon to cd into each service and run the 'start' script within that service. If this command fails anywhere, it will kill all the other commands in this script.

To efficiently update all services to their current master branch version, RUN: npm run updateAll --> this script will run 4 scripts within the proxy server called updateServiceOne, updateServiceTwo, updateServiceThree, and updateServiceFour. Each of these scripts will cd into 1 of the 4 services and RUN: git checkout && git pull --> these scripts will checkout the master branch of the service and pull the most recent commit.

To turn off the servers for all 4 services, ENTER: control+c --> for a mac

All css files have been combined on the proxy server under the dist folder inside the styles.css file.

the index.html for the proxy server exists in the dist folder of the proxy server. In the body of this file is a div for each of the 4 services which line up with what each service is expecting in their ReactDOM.render. Also, in this file exists the header and footer attributes.

# each service
To run a service, RUN: npm start --> this script runs: npm run concurrently to RUN: npm run build as well as: nodemon server/index.js --> the build script runs: npm run webpack --watch --mode development.

To run tests, RUN: npm run test --> this script will tuns: jest

To run esLint, RUN: npm run lint --> this script runs: ./node_modules/.bin/eslint
