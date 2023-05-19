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
In this lecture we are learning about 
default export import and export
naming export and import
props

// default(you can mentiona any name here) and nameing  imports(only exported names you can call)
data parsing:-
props :property types ko set kar rahey ho aur data ko parse karteyho
App.js-->add logo property in Navbar 
In components>Navbar.js-->keeps props in the Navbar()function and change the header as {props.logo} and see the change in output npm start
they are many prop cycle,prop drilling--just data passing for now
validation ko add karna props mey--less developers use kartey
import propTypes from 
get errors in inspect so developer should take care about inspect also
you can write string as  logo="Al-Quran"  or logo={"Al-Quran" }
integer logo=234
default props
rfc is the short cut to get boiler plate for react code
use 
className instead class in Footer.js
htmlfor instead for in footer.js
we use less props
disadvantages:
prop drilling
if u r not using redendent prop then you will call props from parent if u have many compppnents it makes site very slow
Class-3:-------------------------------------
calculator>> textutils https://www.text-utils.com/text-tools/ 
learning Hooks in React
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
   
Lecture:-5------------------Mini Project: Managing State------------------------
   1. What happens when you call setState() inside render() method ?
ans: Stack Overflow Error.
Call to setState() invokes render(). Calling it inside render is suicidal. It gets into an infinite loop.

2. Predict the output of following code when the initial value of number is 1 in state, and user tries to invoke the following function on click of a button


handleClick = () => {
    this.setState({ number: 2 }, () => console.log(this.state.number));
    this.setState({ number: 3 }, () => console.log(this.state.number));
}
ans: 3 3
Solution Description
When setState is called multiple times it is batched together and re render happens only once.
The callbacks for both setStates will be fired after re render.

3. Predict the value of this.state.number after the click listener is invoked once and the initial value of number is 1 in state


    handleClick = () => {
        this.setState(
            prevState => {
                return {
                number: prevState.number + 2
                };
            }
        );
        this.setState(
            prevState => {
                return {
                number: prevState.number + 3
                };
            }
        );
    };
ans: 6
explanation: here we are using prevState, which remembers the last updated value, so here there will be no batching.

5. Predict the value of this.state.number after the click listener is invoked once and the initial value of number is 1 in state
Predict the output of the following code when the initial value of number is 1 in state
   handleClick = () => {
      this.setState(
          prevState => {
              return {
                  number: prevState.number + 2
              };
          },
          () => {
              console.log(this.state.number);
          }
      );

      this.setState(
          prevState => {
              return {
                  number: prevState.number + 3
              };
          },
          () => {
              console.log(this.state.number);
          }
      );
  };


ans: 6 6 
the callbacks console.log are called on updated values.
   6. setState calls
Send Feedback
The state in react can be updated by call to setState method. These calls are
ans: Asynchronous in nature. 
Solution Description
Call to setState in react is asynchronous in nature and multiple calls can be batched for better performance.

7. Updating state
Send Feedback
Why we should not update the state directly and use setState?
ans: It wont re-render the component

8. What is the purpose of using callbacks in setState?
ans: 
Solution Description
The callback function is invoked when setState is finished and the component gets rendered. Since setState() is asynchronous the callback function is used for any post action.

   
   Lecture:-6------------------Mini Project: Finishing UP------------------------
   1. Keys are given to elements in a list in React. These keys are
ans: unique among siblings only.
Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique.
Read more: https://reactjs.org/docs/lists-and-keys.html

2. props in react can _____
ans: not be changed in the component. 
Solution Description
Whether you declare a component as a function or a class, it must never modify its own props. A component cannot update its own props but can update its state and the props of its children.

3. Passing props
all
Which of the following statements is correct about props?
ans: Props in React are read-only data that can be passed and used by the various components into the application. Props are generally a static value, objects, array, or an event handler

4. What are two ways data gets handled in react?
ans: State and props.
Solution Description
Props and states both provide are used to set default values inside the components. They receive initial value from parent components and set initial value of child components.

5.Props and States in React
ans:[4,6] or [d,f]
Which of the following statements is/are incorrect about Props and States?
This problem may have one or more correct answers----
a.Props are immutable and States are mutable.
b.States can only be defined in the component itself.
c.Props are external and controlled by whatever renders the component whereas state is internal and controlled by the component itself.
d.States can be modified by using setState() and props can be modified using setProps()
e.Props and states both provide details about the item.
f.We cannot use state for defining default values in a component.
   
5. Which of the below is the correct syntax to access a property inside the props in a class components?
ans: this.props.name.
Solution Description
We can access any prop from inside a component’s class using the above syntax. The ‘this.props’ is a kind of global object which stores all of a component's props. Here ‘name’, is the key of this props object.

6. Which of the below is the correct syntax to access a property inside the props in a functional components?
ans: props.name

7. The _____ function creates an array of filtered data that pass a condition.
ans: filter.
Solution Description
The filter() function creates an array of filtered data that pass a condition. Filter() function does not work if the array is empty and filter() function does not change the original values of an array. 

8. Why are arrow functions preferred in react?
ans: Clean syntax and less code.
Scope safety.
To avoid binding 'this to methods'.
Solution Description
Read More: 
https://medium.com/@joespinelli_6190/using-arrow-functions-to-avoid-binding-this-in-react-5d7402eec64

9. What is the declarative way to render a dynamic list of components based on values in an array.
ans: Using the Array.map() method.
Solution Description
The map() function is used to iterate over an array or object and manipulate or change data items. In React, the map() function is used for rendering a list of data to the DOM.

10. What will be the output of the following code?
const cartItem = {
  itemName: 'Apples',
  qty: 6,
  price: 10
};
const { qty=1, price } = cartItem;
console.log("Total price of", cartItem.itemName , 'is', qty*price);
ans: Total price of Apples is 60, the default value is only when there is no qty in cartItem 

12.True/False: 
   ans:true
The component given below is a functional component with arrow function definition.
const Demo=(props)=> (
  <h2>Hi, {props.name}</h2>
)
   
13.  Identify the error in the given code.
class Demo extends React.Component {
    return <h2>This is a Demo class component!</h2>;
}
   ans:-- class Demo extends React.Component {
      render() {
        return 
This is a Demo class component!
;
      }
    }
   
14.How can we pass the information from a component to another component which is not a direct parent, child or sibling?
   ans:   Local Storage, Redux
15.React props:-   React - Mini project: Finishing Up - React Props
   List.js:
   import React from "react";
import ListItem from "./ListItem";

class List extends React.Component {
  render() {
    const data = [
      {
        id: 1,
        name: "LinkedIn",
        link: "http://linkedin.com",
        icon: "https://image.flaticon.com/icons/png/128/1409/1409945.png",
        bgColor: "#ff9580"
      },
      {
        id: 2,
        name: "GitHub",
        link: "https://github.com",
        icon: "https://image.flaticon.com/icons/png/128/919/919847.png",
        bgColor: "#f2faa6"
      },
      {
        id: 3,
        name: "Twitter",
        link: "https://twitter.com/",
        icon: "https://image.flaticon.com/icons/png/128/1409/1409937.png",
        bgColor: "#b8b3e8"
      }
    ];

    const listItems = data.map((item) => (
      <ListItem key={item.id} data={item} />
    ));

    return <div className="List">{listItems}</div>;
  }
}

export default List;
ListItem.js:
   import React from "react";

class ListItem extends React.Component {
  render() {
    const { data } = this.props;

    const listItemStyle = {
      backgroundColor: data.bgColor
    };

    return (
      <div className="listItem" style={listItemStyle}>
        <img src={data.icon} alt={data.name} />
        <a href={data.link}>{data.name}</a>
      </div>
    );
  }
}

export default ListItem;
