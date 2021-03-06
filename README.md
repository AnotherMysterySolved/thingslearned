### _A work in progress..._
<br />
<br />

**Helpful Sources:**
- MDN
- Codecademy
- W3Schools
- CSS-Tricks
- JavaScript is Sexy

<br />
<br />
<br />


# -- CSS ------------------------
<br />

## POSITIONING

### Static
- The default state of all html elements
- Static positioned elements are *not* affected by the top, bottom, left, and right properties

### Relative
- An element with position: relative; is positioned relative to its normal position
- Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position.
- Other content will not be adjusted to fit into any gap left by the element.

### Absolute
- An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
- However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

### Fixed
- An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. 
- The top, right, bottom, and left properties are used to position the element.

## SELECTORS
### Adjacent Selector 

```
  ul + p {
    color: red;
  }
```
In the above example, only the *first* p immediately following the ul will appear in red. 
### Direct Descendent Selector 
```
  .container > ul {
    border: 6px solid red;
  }
```
In the above example, the output would be a border appearing only around the container and not its children (ul)

### nth-child Selector 
```
  p: nth-child(3) {
    color: red;
  }
```
In the above example, the *third* p element will appear in red

```
  p: nth-child(odd) {
    color: red;
  }
```
In the above example, *every odd* p element will appear in red

```
  p: last-of-type {
    color: red;
  }
```
In the above example, the *last* p element will appear in red

```
  p: nth-child(3n) {
    color: red;
  }
```
In the above example, *every* third p element will appear in red



### Tilde (~) / Sibling Combinator Selector 
```
  ul ~ p {
    color: red;
  }
```
In the above example, *any* p element existing after the ul will appear in red

<br />


# -- HTML ------------------------

<br />

## BLOCK LEVEL ELEMENTS
  -  p
  -  h1, h2, h3, h4, h5, h6
  -  ol, ul
  -  pre
  -  address
  -  blockquote
  -  dl
  -  div
  -  fieldset
  -  form
  -  hr
  -  noscript
  -  table
## INLINE ELEMENTS
By default will not create a new line when rendered in the browser
**CANNOT** take width, height, margin, or padding styles
  -  a
  -  b
  -  big
  -  i
  -  small
  -  tt
  -  abbr
  -  acronym
  -  cite
  -  code
  -  dfn
  -  em
  -  kbd
  -  strong
  -  samp
  -  time
  -  var
  -  bdo
  -  br
  -  img
  -  map
  -  object
  -  q
  -  script
  -  span
  -  sub
  -  sup
  -  button
  -  input
  -  label
  -  select
  -  textarea

## INLINE-BLOCK ELEMENTS
Sit inline with the content but have the characteristics of a block element in that you **CAN** adjust width, height, margin, or padding styles
  -  Images
  -  Buttons
<br />


# -- JavaScript ------------------------
<br />

## FOR LOOPS
  ### Forward
```
    var vacationSpots = ['Paris', 'New York', 'Barcelona'];

    for (var i = 0; i < vacationSpots.length; i++) {
      console.log('I would love to visit ' + vacationSpots[i]);
    }
```

### Backward
```

   var vacationSpots = ['Paris', 'New York', 'Barcelona'];

    for (var i = vacationSpots.length - 1; i >= 0; i--) {
      console.log('I would love to visit ' + vacationSpots[i]);
    } 
```
    
## PUSH & POP - ARRAYS
```
  var bucketList = ['run', 'hike', 'swim'];

  bucketList.push('cycle', 'fish');
  bucketList.pop('run');

  console.log(bucketList);
```
## RANDOM NUMBER
  This will be between 0-100
```
  Math.floor(Math.random()*100)
```

## TWO WAYS TO ADD NEW PROPERTIES TO AN OBJECT
```
var obj = {
   key1: value1,
   key2: value2
};

// Using dot notation:

obj.key3 = "value3";

// Using square bracket notation:

obj["key3"] = "value3";
```

The first form is used when you know the name of the property. The second form is used when the name of the property is dynamically determined. Like in this example:
```
var getProperty = function (propertyName) {
   return obj[propertyName];
};

getProperty("key1");
getProperty("key2");
getProperty("key3");
```

## SUBSTRINGS
  "some word".substring(x, y) where x is where you start chopping and y is where you finish chopping the original string.
```
  "hello". substring(0, 2);
```

## SWITCH STATEMENTS
```
  var moonPhase = "full";

  switch (moonPhase) {
    case "full":
      console.log("Howwwlll!!");
      break;
    case "mostly full":
      console.log("Arms and legs are getting hairier")
      break;
    case "mostly new":
      console.log("Back on two feet");
      break;
    default:
      console.log('Invalid moon phase');
      break;
  }
```

## WHILE STATEMENT
```
  var cards = ['Diamond', 'Spade', 'Heart', 'Club'];
  var currentCard = 'heart';

  while (currentCard !== 'Spade') {
    console.log(currentCard);

    var randomNumber = Math.floor(Math.random() * 4);

    currentCard = cards[randomNumber];
  }

  console.log('We got a spade!');
```
<br />

# -- jQuery ------------------------
<br />


## HIDE AN ELEMENT(s)
```
function main() {
    $('.skillset').hide();
  }

  $(document).ready(main);
```

## FADE IN AN ELEMENT(s)
```
function main() {
    $('.skillset').hide();
    $('.skillset').fadeIn(1000);
  }

  $(document).ready(main);
```

## NEXT
  jQuery has a function named next to help us select elements that are next to another element. If we have this in our HTML:

```
  <div class='item-one'> ... </div>
  <div class='item-two'> ... </div>
  If we wanted to hide item-two, we could write:

  $('.item-one').next().hide();
```


## SHOW AN ELEMENT
  To show an element, the syntax looks as such:
```
  $('.example-class').show();
```
  show is attached directly to the jQuery selector.

  show will change the CSS attribute "display: none" to a visible display property, therefore showing the element.


## SLIDETOGGLE
jQuery provides a method named slideToggle that can animate an element's entrance and exit. The syntax looks like this:
```
$('.example-class').slideToggle(400);
```

## TEXT
  We can change the text of an element with the jQuery function text. It's syntax looks like this:
```
$('.my-selector').text('Hello world!');
```

## THIS
  $(this) selects the clicked element. If there are multiple elements with a class of .example-class, this will only toggle the class of the one that is clicked on.
```
  $('.example-class').on('click', function() {
    $(this).toggleClass('active');
  });
  ```

## TOGGLE
  toggle will hide or show an element, each time it is triggered. The syntax looks like this:
```
$('example-class').toggle();
```
## TOGGLECLASS
  We can toggle a CSS class with a jQuery function named toggleClass. The syntax looks like this:

  ```
  $('.example-class').toggleClass('active')
  ```

<br />

# -- ReactJS ------------------------
<br />

## Event Listeners in JSX
- An event listener attribute's value should be a function.
- Note that in HTML, event listener names are written in all lowercase, such as onclick or onmouseover. **In JSX, event listener names are written in camelCase**, such as onClick or onMouseOver
```
function myFunc() {
  alert('Make myFunc the pFunc... hahahaha');
}

<img onClick={myFunc} />
```


## Event Listener in a Component
```
import React from 'react';
import ReactDOM from 'react-dom';

class Button extends React.Component {
  scream() {
    alert('AAAAAAAAHHH!!!!!');
  }

  render() {
    return <button onClick={this.scream}>AAAAAH!</button>;
  }
}

ReactDOM.render(
	<Button />,
        document.getElementById('app')
	);
```

## if Statements in JSX
- You **CANNOT** inject an if statment into JSX
- A common way around this is to write an if statement, and not inject it into JSX
```
import React from 'react';
import ReactDOM from 'react-dom';

let message;

if (user.age >= drinkingAge) {
  message = (
    <h1>
      Hey, check out this IPA!
    </h1>
  );
} else {
  message = (
    <h1>
      Hey, check out this O'DOUL'S!
    </h1>
  );
}

ReactDOM.render(
  message, 
  document.getElementById('app')
);
```
Another example:
```
import React from 'react';
import ReactDOM from 'react-dom';

function coinToss() {
  // This function will randomly return either 'heads' or 'tails'.
  return Math.random() < 0.5 ? 'heads' : 'tails';
}

const pics = {
  kitty: '#',
  doggy: '#'
};
let img;

// if/else statement begins here:
if (coinToss() === 'heads') {
  img = (
    <img src={pics.kitty} />
  );
} else {
  img = ( 
    <img src={pics.doggy} />
  );
}

ReactDOM.render(img, document.getElementById('app'));
```
## Import & Export from a Different File
NavBar.js (notice line 3)
```
import React from 'react';

export class NavBar extends React.Component {
  render() {
    const pages = ['home', 'blog', 'pics', 'bio', 'art', 'shop', 'about', 'contact'];
    const navLinks = pages.map(page => {
      return (
        <a href={'/' + page}>
          {page}
        </a>
      )
    });

    return <nav>{navLinks}</nav>;
  }
}
```
ProfilePage.js (notice line 3)
```
import React from 'react';
import ReactDOM from 'react-dom';
import { NavBar } from './NavBar';

class ProfilePage extends React.Component {
  render() {
    return (
      <div>
	<NavBar />
        <h1>All About Me!</h1>
        <p>I like movies and blah blah blah blah blah</p>
        <img src="https://s3.amazonaws.com/codecademy-content/courses/React/react_photo-monkeyselfie.jpg" />
      </div>
    );
  }
}
```

## JS in the JSX

```
var React = require('react');
var ReactDOM = require('react-dom');

ReactDOM.render(
  // to use JS we simply wrap w/e it is in: { }
  <h1>{2 + 3}</h1>,
  document.getElementById('app')
);
```

## Keys
- When you make a list in JSX, sometimes your list will need to include something called keys:
```
<ul>
  <li key="li-01">Example1</li>
  <li key="li-02">Example2</li>
  <li key="li-03">Example3</li>
</ul>
```
- A key is a JSX attribute. The attribute's name is key. The attribute's value should be something unique, similar to an id attribute.
- keys don't do anything that you can see! React uses them internally to keep track of lists. If you don't use keys when you're supposed to, React might accidentally scramble your list-items into the wrong order.
- An example using mapping:
```
import React from 'react';
import ReactDOM from 'react-dom';

const people = ['Rick', 'Morty', 'Summer'];

const peopleLis = people.map((person, i) =>
  // expression goes here:
  <li key={'person_' + i}>{person}</li>
);

// ReactDOM.render goes here:
ReactDOM.render(<ul>{peopleLis}</ul>, document.getElementById('app'));
```
## Logic in a Render Function
```
import React from 'react';
import ReactDOM from 'react-dom';

class Random extends React.Component {
  render() {

    // First, some logic that must happen
    // before rendering:
    const n = Math.floor(Math.random()*10+1);

    // Next, a return statement
    // using that logic:
    return <h1>The number is {n}!</h1>;
  }
}

ReactDOM.render(
	<Random />, 
	document.getElementById('app')
);
```

Another Example with a Conditional:
```
import React from 'react';
import ReactDOM from 'react-dom';

const fiftyFifty = Math.random() < 0.5;

// New component class starts here:
class TonightsPlan extends React.Component {
  render() {
    if (fiftyFifty) {
      return <h1>Tonight I'm going out WOOO</h1>;
    } else {
      return <h1>Tonight I'm going to bed WOOO</h1>;
    }
  }
}

ReactDOM.render(
	<TonightsPlan />,
	document.getElementById('app')
);
```

## .map in JSX
If you want to create a list of JSX elements, then .map() is often your best bet
```
import React from 'react';
import ReactDOM from 'react-dom';

const people = ['Rowe', 'Prevost', 'Gare'];

const peopleLis = people.map(person =>
  // expression goes here:
	<li>{person}</li>);
);

ReactDOM.render(<ul>{peopleLis}</ul>, document.getElementById('app'))
```

In the above example, the output will be: 5

## Props
Props is the name of the object that stores passed-in information. ```this.props``` refers to that storage object. At the same time, each piece of passed-in information is called a prop. This means that props could refer to two pieces of passed-in information, or it could refer to the object that stores those pieces of information ```:(```

## Props to pass info from one component to another
Greeting.js
```
import React from 'react';

export class Greeting extends React.Component {
  render() {
    return <h1>Hi there, {this.props.name}!</h1>;
  }
}
```
App.js
```
import React from 'react';
import ReactDOM from 'react-dom';
import { Greeting } from './Greeting';

class App extends React.Component {
  render() {
    return (
      <div>
        <h1>
          Hullo and, "Welcome to The Newzz," "On Line!"
        </h1>
        <Greeting name="Ruby" />
        <article>
          Latest newzz:  where is my phone?
        </article>
      </div>
    );
  }
}

ReactDOM.render(
  <App />, 
  document.getElementById('app')
);
```
**Output will be:**
<br/>
Hullo and, "Welcome to The Newzz," "On Line!"
<br/>
Hi there, Ruby!
<br/>
Latest newzz: where is my phone?


## Render
  ```
  var React = require('react');
var ReactDOM = require('react-dom');

var myDiv = (
  <div className="big">I AM A BIG DIV</div>
  );

ReactDOM.render(
  myDiv,
  document.getElementById('app')
);
```

## Render A Component
- A component class needs a set of instructions which tell the component class how to build components. When you make a new component class, these instructions are the body of your class declaration:
```
class MyComponentClass extends React.Component
{ // everything in between these curly-braces is instructions for how to build components

  render() {
    return <h1>Hello world</h1>;
  }
}
```
- This class declaration results in a new component class, in this case named MyComponentClass. MyComponentClass has one method, named render. This all happens via standard JavaScript class syntax.

- **NOTE:** JSX elements can be either HTML-like, or component instances. JSX uses capitalization to distinguish between the two! That is the React-specific reason why component class names must begin with capital letters. In a JSX element, that capitalized first letter says, "I will be a component instance and not an HTML tag."

- Whenever you make a component, that component inherits all of the methods of its component class. MyComponentClass has one method: MyComponentClass.render(). Therefore, <MyComponentClass /> also has a method named render.

- You could make a million different ```<MyComponentClass />``` instances, and each one would inherit this same exact render method.

- Since the component has a render method, all that's left to do is call it. To call a component's render method, you pass that component to ```ReactDOM.render()```. Notice the component, being passed as ```ReactDOM.render()```'s first argument:
```
ReactDOM.render(
  <MyComponentClass />,
  document.getElementById('app')
);
```
- ```ReactDOM.render()``` will tell ```<MyComponentClass />``` to call its render method.

- ```<MyComponentClass />``` will call its render method, which will return the JSX element ```<h1>Hello world</h1>```. ```ReactDOM.render()``` will then take that resulting JSX element, and add it to the virtual DOM. This will make "Hello world" appear on the screen.

## Self-closing Tags
- Most HTML elements use two tags: an opening tag (<div>), and a closing tag (</div>). However, some HTML elements such as <img> and <input> use only one tag. When you write a self-closing tag in HTML, it is optional to include a forward-slash immediately before the final angle-bracket
- In JSX, you have to include the slash. If you write a self-closing tag in JSX and forget the slash, you will raise an error
```
var profile = (
  <div>
    <h1>I AM JENKINS</h1>
    <img src="images/jenkins.png" />
    <article>
      I LIKE TO SIT
      <br />
      JENKINS IS MY NAME
      <br />
      THANKS HA LOT
    </article>
  </div>
);
```
## Ternary Operators show up a lot in JSX
- The ternary operator works the same way in React as it does in regular JavaScript
- Here's how you might use the ternary operator in a JSX expression:
```
const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);
```
Another example:
```
import React from 'react';
import ReactDOM from 'react-dom';

function coinToss () {
  // Randomly return either 'heads' or 'tails'.
  return Math.random() < 0.5 ? 'heads' : 'tails';
}

const pics = {
  kitty: '#',
  doggy: '#'
};

const img = <img src={pics[coinToss() == 'heads' ? 'kitty' : 'doggy']} />;

ReactDOM.render(
	img, 
	document.getElementById('app')
);
```

## Variables in JSX
- When you inject JavaScript into JSX, that JavaScript is part of the same environment as the rest of the JavaScript in your file.
- That means that you can access variables while inside of a JSX expression, even if those variables were declared on the outside.
```
import React from 'react';
import ReactDOM from 'react-dom';

const theBestString = 'tralalalala i am da best';

ReactDOM.render(<h1>{theBestString}</h1>, document.getElementById('app'));

// Output == tralalalala i am da best
```
## Variable Attributes in a Component
```
import React from 'react';
import ReactDOM from 'react-dom';

const owl = {
  title: "Excellent Owl",
  src: "#"
};

// Component class starts here:
class Owl extends React.Component {
  render() {
    return (
      <div>
        <h1>{owl.title}</h1>
        <img src={owl.src} alt={owl.title} />
      </div>
    );
  }
}

ReactDOM.render(
  <Owl />,
  document.getElementById('app')
); 
```

When writing JSX, it's common to use variables to set attributes.
```
// Use a variable to set the `height` and `width` attributes:

const sideLength = "200px";

const panda = (
  <img 
    src="images/panda.jpg" 
    alt="panda" 
    height={sideLength} 
    width={sideLength} />
);
```
Object properties are also often used to set attributes:
```
const pics = {
  panda: "http://bit.ly/1Tqltv5",
  owl: "http://bit.ly/1XGtkM3",
  owlCat: "http://bit.ly/1Upbczi"
}; 

const panda = (
  <img 
    src={pics.panda} 
    alt="Lazy Panda" />
);

const owl = (
  <img 
    src={pics.owl} 
    alt="Unimpressed Owl" />
);

const owlCat = (
  <img 
    src={pics.owlCat} 
    alt="Ghastly Abomination" />
);
```
