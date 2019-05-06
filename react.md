# React Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Here is a list of pros and cons to using the React library to build your application -- but some of them are false. Remove the false statements from the list:

- React is a modern, efficient answer to complex UI applications

- React is a flexible library that plays the role of V in an MVC framework


 #### 2. What are "smart"(logic) and "dumb"(display) components? Explain the difference and also add why we bother to make the distinction between them.


 //Your Answer
Dumb, or "pure", components are those whose sole function is to render. This means that they do not have any other methods other than render and do not hold their own state or pass down props to any possible children components.

Smart, or "impure", components are essentially the opposite of dumb components. Their sole function is to house the logic to allow interaction and functionality of different things on the DOM. This means that they either hold state and pass down props, have other methods other than just render (but will have render as well), or a combination of both. Smart components don't normally control the overall layout of the DOM, but more often a small piece that has functionality.

 //Googled Answer
Google confirms my explanation of smart and dumb components.

#### 3. When we use "yarn add ..." in the terminal - what is yarn doing? And what file will always be automatically updated after we add a package with yarn?


 //Your Answer
Yarn is one of a few different package managers. When we use yarn add, we are simply adding a package to be able to use. The conceptuality of yarn and other package managers is still beyond my understanding, but I believe that the PWD or present working directory (directory you are currently in within terminal) is the file that will always be automatically updated after we add a package with yarn.

 //Googled Answer
I was so wrong! The files that are automatically updated are the package.json and yarn.lock files. This enables other developers working on the project to get the same dependencies as yourself.

#### 5. There are three mistakes in this code that would cause it to break our application. Find the mistakes and fix them:

    import React, { Component } from 'react';

    class Recipes extends Component {
      constructor(props){
        super(props)
        this.state = {
          recipes: [
            {name: 'Meatballs'},
            {name: 'Mac & Cheese'}
          ]
        }
      }

      render() {
        let recipes = this.state.recipes.map(function(recipe){
          return(
            <li key={recipe.name}>{recipe.name}</li>
            )
            })
        return (
          <ul>
            {recipes}
          </ul>
        );
      }
    }

    export default Recipes;

#### 6. Name three html input types. (NOTE: text is the default type - so it doesn't count in this case)

 //Your Answer
password, email and number

 //Googled Answer
Google confirmed my answer. There A LOT more though.

 #### 7. How would you explain state to a friend who doesn't know code?

 //Your Answer
I would use the analogy of physical states (chemistry) with an example of water. Let's assume room temperature is about 68 degrees F. The current state of water would be liquid. If we were to do something to change our environment, let's say make it really cold, and we now have a room temp that is below 32 degrees F, this water would change state. The water would now be solid and become ice. If we raise the temperature back to that comfortable 68 degrees, the state would change again and become liquid once more. If the room temperature would to change one last time and increase to above 212 degrees F, it would change state to a gas.

There are also multiple floors in this analogous building and there is one rule: the water ALWAYS starts on the top floor. Water can be moved down to to the floor below but never brought back up. The only thing you can do on a floor below to interact with the physical state of the water above is to change the temperature. Nevertheless, when water is moved from one floor down to another, it is in the same physical state that it was before being moved. For example, if water was solid on the top floor and brought down one floor, it would still be solid. Unless something else acts upon it to change its state will it remain solid.

 //Googled Answer
"State is a way to update our UI based on events."
Much more concise and does not require an elaborate analogy, assuming most people would know what UI or user interface is.

 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.


 //Your Answer
State is like the global variables for that component. You may call upon them anywhere within that component, though it is typically done within a method. Like the googled answer above states (heh get it?), it is a way to update our UI based on events. The elements housed within state will usually be altered through events, or anything intentionally designed to alter state. For example, you may have counter on your page with a count set to zero within state and a method set to an onClick event that increase the counter every click. Another way to think of state is that it usually houses elements that will be displayed on the DOM and can be altered depending on the designed functionality of the component.

Properties, or more commonly referred to as props, are simply information that is meant to be passed down from a parent component to a child component. The syntax of passing down a prop looks very similar to an html tag attribute, but the naming convention is the big giveaway. You can, and should, name your props according to what their current name is or what their intended function is. For example, if I wanted to pass down a method named handleClick, I would pass it as handleClick={this.handleClick}. This is intended to eliminate confusion. Methods are not the only things that can be passed down. State can also be passed down to children components. This can allow for the concept of separation of concerns which allows you to manipulate a parent component's state from a child component. The interaction between parent and children component is necessary for complex functions to become reality on a DOM.

 //Googled Answer
There are some convoluted answers out there but what they are essentially saying is that state is what lives in the parent component and props are what's passed down (usually state) to the child(ren) component(s).

#### 9. Write a paragraph or so about your experience with building tic-tac-toe. Some topics to start with might be: things you learned about yourself, concepts from React that stood out to you, something about pair programming (if you paired), or the experience of building something in code from scratch.
Not required.
