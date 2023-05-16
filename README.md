# React

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


