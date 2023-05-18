# React
Class_1========================================================
-Frontend library--JS library--component based language[class component based,function component based]
before react we used running node >> npm init >> 
npm create-react-app name of you application --automatically node installed
1GB=1024MB npm node package manager---npx-node package execution saves storage just execute the project

1.npx create-react-app my-react-app
nodemodules>>public >>src>> gitignore>>package.json>>readme file
2.cd my-react-app
3.npm start
4.to check output of your project--production mey run karnahay:-npm run build.

public folder> only index.html removed evrything--<div id="root"> </div>
src >> index.js and App.js 
index.js-->main root file
import ReactDOM from 'react-dom/client' --> DOM manipilation JS and html pages ko render kartethey
main code logic App.js meyhi likhtey index.js meytho sirf imports and App.js ko call kartey
<></> isko react fragmentation kehtey:- adding extra div in App.js and best instead <div></div>tags

Class-2:-------------------------------------
props important in React interview
exports and import

module.js module2.js 2 files create outside of src folder
// default(you can mentiona any name here) and nameing  imports(only exported names you can call)

DataParsing
Class-3:-------------------------------------
const[text,setText]=useState("this is correct setYext formmate");
camel case in react:--to change a value we use-----onChange={} Handler

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
Lecture:-1------------------Mini Project: Starting the Project------------------------
Lecture:-2------------------Mini Project: Starting the Project------------------------
Lecture:-3------------------Mini Project: Starting the Project------------------------
Lecture:-4------------------Mini Project: Starting the Project------------------------
1. How do you write an inline style specifying the font-size:10px and color:blue in JSX?
ans: style={{fontSize:10, color:'blue'}};

2. Which of the following is the correct syntax for adding a click event handler, foo, to a button in React Jsx ?
ans: <button onClick={this.foo}>

3. What is a state in React ?
ans: A state in React is used to store the property values that belong to a component.   it enables a component to keep track of changes between renders

4. Over the image
Send Feedback
You are given a code to display an image on the page, you have to print “I’m on the image” in the console as soon as you move over the image. So which of the following is a correct event for that?
import React from "react"
function App() {
   return (
       <div>
           <img ------- src="ABC"/>
        </div>
   )
}

export default App
ans: onMouseOver={()=>console.log("over the image")}
  
5.Find the error
Find error/s in the given code:
import React from "react"

function App(){
   constructor(){
       this.state={
           myName: “CN”
       }
   }
   render(){
       return (
           <div>
               <h1>{this.state.myName}</h1>
           </div>
       )
   }
}
export default App
Options
This problem may have one or more correct answers[1,4]
>It should be a class component instead of a functional component----
Instead of {this.state.myName} in <h1> it should be {myName}
render() statement should not be there.
>super() is missing from the constructor-----

6.As soon as the state of react component gets changed, the component will
ans: be-rerendered.
Solution Description
As soon a state gets updated, the component re-renders itself

7. Output of the code
Send Feedback
Find out what happens when the following render() method gets executed?
 render(){
   let code = ["Java","ES6","Ruby"]
     return (
        <div>
           {code.map(item => <p>{item}</p>)}
        </div>)
   }
ans: Displays the list of code in the array.
Solution Description
map will iterate over each element of the list to display

8. Styling in React
Send Feedback
What is the correct method to write an inline style specifying the background color: yellow and color:green; in JSX.
ans: style = {{backgroundColor: 'yellow', color:'green'}}
