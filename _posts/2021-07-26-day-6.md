---
title: Day 6 - Corrections in translation.json file
---

- ## Task:
  * To do corrections in translations.json file

Hy Guys!!!      
Today I do not have much to tell you about, I mean it was an usual day with obviously new things but as a whole my task was same as previous one. So, I started working on correcting 
new translation in spanish that I missed and some new were also given by clients. I completed the work and opened a PR which is yet to be reviewed and merged to main repo.     
One more thing today ng-select-clone clone that I made on saturday was reviewed by my mentor. I got a very detailed review with suggestions and mistakes I should take care while making 
a project like this. I would like to tell you all what reviews I got:-
The output result looks good but
I found some issues which i am mentioning

1. I forgot to mention that you dont have to use any library for select dropdown and stuff it should be from scratch 
2. One of the advantage of scss is nesting which is not used in the css section
- We dont have to overexploit nesting but we need to use enough which makes our code look good and ofcourse avoid global class declaration for each and every style declaration. Which happens in css unless we create something like .a .b {} something like this.
3. You can also create mixins for media queries and just plug them in inside the respective element which makes code look self explanatory
4. The code was not formatted properly (un-formatted code is not accepted at most of the places) if someone is asking to use eslint it is not acceptable at all.
5. Fix css class naming conventions maybe one of your own or from the community i just found .header-container{} and .bodyContainer{} one is in kebab-case and other in camelCase.
6. Try to use widths and heights in percentage when working on layouts, fix widths are going to cause issues in responsive designs.
7. Dont store absolute widths inside scss variables.
- By this we basically have to understand about DRY pattern and consistency by dry we mean Do not repeat yourself which means we have to variabalize only the things which are going to be used again and again in the whole app. You can declare the variable which are going to be used 1 time and only in single class section maybe for a card maybe for a header but those should be local to the style we are refering to
8. Use separate scss files for different purpose
- For example if you are writing scss for a card component you can split the code by making a new file and importing it to the central index file which will help manage the code.
9. On frontend side to client the quality of the frontend coder is defined by the output generated if there is even a single noticable thing which is not matching the design or the specification given then there could be 10 raised questions on why this is not same as the design and stuff. (The only reason i mentioned in design to be pixel perfect) I can still notice the difference in spacing, fonts, heights, shadows, hover effects etc. Try comparing side by side what i am trying to say. Try noticing all these minor details because these minor details are something which can group together and ruin the whole frontend design.
10. Code spliting is good but too much code spliting can cause a lot of issues, and the code spliting where the component is not going to be reused and has only one sole purpose of fitting inside a specific layout has no use at all (This is just causing complexity and increasing file)
- A component can be a page, an icon, a block section or something which is going to perform a specific task for example:- Button, CustomRadio, CheckBox, A SelectInput component, Modals etc. There should be a sole purpose of the existence of the component. If a component is just filling gaps for class names and micro layouts it is of no use.
- For example you could have a single card component which contained the layout dom for the whole card. Ofcourse code splitting can happen but prefer it only in cases where we are going to reuse those different blocks or our single component is getting lengthy.

That is it for now and here are some blogs you can have a look at:-    
[link1](https://bradfrost.com/blog/post/sass-selectors-to-nest-or-not-to-nest/)       
[link2](https://www.freecodecamp.org/news/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849/)     
[link3](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)     
[link4](https://tutorial.techaltum.com/css_fixed_liquid_layout.html)      

You can perform these improvements in the code 
If you have any questions just ping me 

Nice work done with mixins ans inheritance :star:      
So, this was the exact review I got from my mentor. The sole purpose of pasting the review here is that all the readers can also experience how things go in training and what you 
have to work on. And another reason is that everytime I will take a look at this blog, I will remind myself of not doing these mistakes.     
#### Thank you for reading.    
### Happy Improving 😎
