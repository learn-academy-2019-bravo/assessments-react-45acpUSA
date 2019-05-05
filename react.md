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


 //Googled Answer


 #### 7. How would you explain state to a friend who doesn't know code?

 //Your Answer


 //Googled Answer


 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.


 //Your Answer


 //Googled Answer


#### 9. Write a paragraph or so about your experience with building tic-tac-toe. Some topics to start with might be: things you learned about yourself, concepts from React that stood out to you, something about pair programming (if you paired), or the experience of building something in code from scratch.
