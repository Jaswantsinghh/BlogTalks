---
title: Day 2 - React-i18n, conditional rendering & ESlint
---
- ## Tasks
  * [Correction in conversion of keywords from `en` to `esp` or vice versa using i18n module.](#react-i18next)
  * [Conditional rendering in a React component.](#conditional-rendering-in-react)
  * [Learn about ESlint.](#eslint)

# React-i18next
After doing some simple corrections in translation.json file yesterday, today the task was a bit lengthy (not complicated). There were many places where we need to check a particular react component and then
its corresponding translations in `en/translation.json` as well as `esp/translation.json`.     
So, I changed the translations in modules accordingly. I give me a better understanding of i18n and how it works. Yesterday, I just got to touch i18n from outside but today I manipulated 
it on my own and it was a great learning however.

# Conditional Rendering in react
I will not confuse with its formal definition, but I will try to explain it in simple language. I assume that you know react, if not, no problem I will try to keep it as simple as possible.
So, in react.js we build something big by joining smaller components together. Just take an example of wall consisting of a window and a photo. Now, this huge will is made up
 of smaller components bricks, a window and a photo. Now we can do further breakdown of window as it comprises of components glass pane, wooden frame etc. same with photo.    
 Now consider this wall as your project and bricks as components, you'll join breaks together and keep a window in it. This is how you use react by creating components.     
Now when we use a react component to show something on frontend, it is known as rendering.   
I encountered a problem today while correcting translations. The default keyword we had was star, and we was using it with each number like 1 star, 2 star, 3 star so on... But for 
numbers>1 we need to use plural form of star i.e. stars.     
So, here conditional rendering came into picture. I created a condition that `if(no  of star>1)` render `stars` component else render `star` component.    
I think conditional rendering is clear to you now, It is just using some conditions when rendering something on screen, just like `if-else` conditional statement in any programming language.
#### An example of conditional rendering:-
```jsx
render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
      The user is <b>{isLoggedIn ? 'currently' : 'not'}</b> logged in.
    </div>
  );
}
```
After completing these task I pushed all the commits to the repo and opened the PR to main directory.

# ESlint
## About
ESLint is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs.    
ESLint is an open source JavaScript linting utility originally created by Nicholas C. Zakas in June 2013. Code linting is a type of static analysis that is frequently used to find problematic patterns or code that doesn't adhere to certain style guidelines.          
JavaScript, being a dynamic and loosely-typed language, is especially prone to developer error. Without the benefit of a compilation process, JavaScript code is typically executed in order to find syntax or other errors. Linting tools like ESLint allow developers to discover problems with their JavaScript code without executing it.
The primary reason ESLint was created was to allow developers to create their own linting rules. ESLint is designed to have all rules completely pluggable. The default rules are written just like any plugin rules would be. They can all follow the same pattern, both for the rules themselves as well as tests. While ESLint will ship with some built-in rules to make it useful from the start, you'll be able to dynamically load rules at any point in time.      

ESLint is written using Node.js to provide a fast runtime environment and easy installation via npm.
## Installation
### Prerequisite:
  - NPM       

You can install ESLint using npm:
```bash
$ npm install eslint --save-dev
```
You should then set up a configuration file:
```bash
$ ./node_modules/.bin/eslint --init
```
After that, you can run ESLint on any file or directory like this:
```bash
$ ./node_modules/.bin/eslint yourfile.js
```
## Configuration
After running `eslint --init`, you'll have a .eslintrc file in your directory. In it, you'll see some rules configured like this:
```javascript
{
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["error", "double"]
    }
}
```
The names "semi" and "quotes" are the names of rules in ESLint. The first value is the error level of the rule and can be one of these values:

- "off" or 0 - turn the rule off
- "warn" or 1 - turn the rule on as a warning (doesn't affect exit code)
- "error" or 2 - turn the rule on as an error (exit code will be 1)      
The three error levels allow you fine-grained control over how ESLint applies rules (for more configuration options and details, see the [configuration docs](https://eslint.org/docs/user-guide/configuring/)).

Thank you for reading this post.
#### Happy linting :)
