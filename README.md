# React
Class_1========================================================
-Frontend library--JS library--component based language[class component based,function component based]
before react we used running node >> npm init >> 
npm create-react-app name of you application --automatically node installed
1GB=1024MB npm node package manager---npx-node package execution saves storage just execute the project

npx create-react-app my-react-app
nodemodules>>public >>src>> gitignore>>package.json>>readme file
cd my-react-app
npm start
production mey run karnahay:-npm run build.

public folder> only index.html removed evrything--<div id="root"> </div>
src >> index.js and App.js 
main root file--> index.js
import ReactDOM from 'react-dom/client' --> DOM manipilation JS andar html pages ko render kartethey
react fragmentation:- adding extra div in App.js 
create-react-app=======================================
Installation:
open terminal redirect to you directory:-
# sudo npm install create-react-app or remove sudo

open your folder for project 
# cd Coding

create a rect app use small letters 
# create-react-app helloworld
# cd helloworld
# ls
# npm start
Open VS code now: check all your created folders
your server directly get opened and start running this is called create-react-app template

Webpack================================================
A module bundler
app.js header.js navbar.js -> bundler -> bundler.js ->index.html
webpack.config.js
in react
1> Entry point: index.js  [webpack will take imports require from index.js]
2> Perform transformation: SASS [Loader sass convert to css . ]
3> outputs: dist folder 

Imports Exports=============================================
in script tags if index.js files jquery defined first then you can include code in down order matters
es6 also do the same import abc(){} in 1.js and export abc() in 2.js
in src folder you will create every js file
src> 1.js 2.js
in 2.js>>write
function log(){
console.log('LOG');
}
function greet(){
console.log('Hi');
}
function sum(){
console.log('SUM');
}
const a=90;
export default log;

in 1.js export log in this js file
import log from './2.js';
log();


