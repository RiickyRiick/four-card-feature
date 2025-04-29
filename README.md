# Frontend Mentor - Ricky's 'Four Card Feature Section' Solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK).
 Frontend Mentor challenges help you improve your coding skills by building realistic projects. 


## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)



## Overview

Coming into this project, I already had some knowledge of CSS Grid and Flexbox 
(check out the resource section to see all the website's helpful things that assisted 
me throughout the project). I started the 'Mobile-First workflow' but didn't prefer it. Ultimately, I restarted the project and wrote my code 
starting from the 'Desktop-First workflow. 

I started using Grid-areas at first, but I spent more time trying to figure out 
how the design could be made simple instead of using 'Grid-area: 1 / 2 / 3 / 5 (just 
an example). Creating three columns was way easier to execute (thanks again to Mr Coder for
explaining this process and to Dr. Angela). 

It's super rewarding when you can get a simple flow of transitioning from 'Desktop' to 
'Mobile' design, since creating a responsive design, needs a consistent structure within the code. 

Again, don't underestimate the HTML side. Grouping is very critical to learn, properly executing 
they will show greatly within your CSS code, and most importantly, they'll prevent headaches down the road. 


### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

<img src="./design/My Desktop Design.png"/>
<img src="./design/My Mobile Design.png"/>


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

My grouping section was a lot clearer and concise within the HTML. I then proceeded to work from top to bottom, ensuring I kept my steps in an orderly fashion.

I went from:

-HTML-
--correct HTML tags
--Grouping

-CSS-
--body, i.e., all the small details (fonts, margin, sizing, etc.)
--container 
--top header
--box-container
--grid-items
--responsive testing
--finished aligning the .attribution (footer)

Throughout the process, I found it super useful to remember the names you use for the grouping within the HTML. This project consisted of a bit of grouping, so going back and forth between your HTML and CSS page can be a bit of a hassle. 

In conclusion, this project was more well-structured. The stages that I had set up for myself were well executed. I will try this process again. 


### Built with

- Semantic HTML5 Markup
- Flexbox
- CSS Grid
- Desktop-first workflow

### What I learned

For this project, I learned that you don't always need to use the
body to align the page:

```html
body {
 height: 100vh;
 display: flex;
 justify-content: center;
 align-items: center;
}
```
...adding this ended up being a mistake of mine since my CSS Grid 
wasn't responsive and only added difficulty trying to find fluidity
when sizing down my viewport.

_____________________________________________________________________

I also learned that you can override:
```css
text-align: right;
```
With:
```css
text-align: left;
```
It might seem strange, or even a simple execution that's a no-brainer, but I overlook this. All you need to do is have a more specific name that overrides it. 

For example:
```html
<div class="box-container">
 <section class="grid-items supervisor">
 <div class="text">
 <h5>Supervisor</h5>
 <p>Monitors activity to identify project roadblocks</p>
 </div>
 <img src="./images/icon-supervisor.svg" alt="magnifying glass icon">
 </section>
```
```css
.grid-items {
 background-color: hsl(0, 0%, 100%);
 border-radius: 10px;
 padding: 20px;
 text-align: right;
 box-shadow: 1px 10px 20px RGB(220, 214, 239);
}

.text {
 text-align: left;
 padding-bottom: 60px;
}
```
...within the HTML above, I had a .grid-items class for all the boxes. This helped me edit each box simultaneously; it's a significant advantage. Within the CSS code, I had a text-align: right, so all the content went right, but it's only supposed to be for the image. So then, how do you fix it? Aha, with another div wrap targeting only the text. This specific target lets you override the first alignment, giving you the correct placement for the text and image. Pretty neat rule. (Thanks Mr Coder!)

_______________________________________________________________________________

Now, another cool thing that I learned was regarding the flexbox align-self rule. Here is a screenshot I took with an added 1px solid black border around the .box-container for a better representation of what I'm about to explain:

'Without align-self'
<img src="./design/Align-self none.png"/>
```css
.supervisor, .calculator {
 align-self: ;
}
```
'With align-self: center'
<img src="./design/Align-self center.png"/>
```css
.supervisor, .calculator {
 align-self: center;
}
```
The best way I can explain this is if you take a look at the first image, the .supervisor and .calculator. These are the only .grid-items taking the full height of the .box-container. Two .grid-items (.team-builder and .karma), which are grouped together, take up the center. 

Now, since all the .grid-items are the same size, adding the align-self: center not only aligns the .supervisor and .calculator to the center but simultaneously shrinks them back to their original size, just like the .grid-items in the center, since it was only taking up the full height of its 'Parent Grid Container' to cover the space that was undefined. 

_______________________________________________________________________



## Useful resources

I have been using Mimo's Platform for the past 5 months. They introduced Flexbox and CSS Grid to me: 
--This project helped me go back and review the material I learned in Mimo.

I'm still taking this Udemy course called "The Complete Full-Stack Web Development Bootcamp";
taught by Dr. Angela Yu, who is the Developer and Lead Instructor:

-- This project helped me learn how to keep things simple. With Dr. Angela, we had to create a Mondorian type 
of art that she provided. This is what I created: 

<img src="./design/Mondrian Design.png/"/>

Having completed this project was already a significant advantage stepping into this project. 


I also finished playing two games on Codepip that were called,


"Flexbox Froggy" and "CSS Grid Garden" really recommend both of these games. 


## Author

--Website: (https://www.rarroyoharo.com)<a href="https://www.rarroyoharo.com" target="_blank">rarroyoharo.com</a> 
--Frontend Mentor - [@RiickyRiick]<a href="https://www.frontendmentor.io/profile/RiickyRiick" target="_blank">@RiickyRiick</a> 



## Acknowledgments

All glory to my Lord and Savior, Jesus Christ, for breathing life into me yet another day and giving me another opportunity to continue growing as a web developer, but most importantly, being able to spread his love and compassion to everyone. Blessings


I also want to thank Vanza Setia for his article, "The benefits of writing a good challenge README." I've always seen this section as an essential part of my learning, even before I read his article. However, I realized I wasn't doing a better job of explaining my procedures or work more clearly. Even now, I catch myself when I know what I'm typing isn't clear and concise. If you haven't already, please check out his article. I also encourage you to write more in your README; the benefits are just too much not to do. 

<p><a href="https://www.frontendmentor.io/articles/the-benefits-of-writing-a-good-challenge-readme-3EIwMaYVgz" target="_blank">The benefits of writing a good challenge README</a>"</p>



<a href="https://mimo.com" target="_blank">Mimo.com</a>
<a href="https://www.udemy.com/course/the-complete-web-development-bootcamp/?couponCode=25BBPMXPLOYCTRL" target="_blank">The Complete Full-Stack Web Development Bootcamp</a> : 
taught by <a href="https://www.udemy.com/course/the-complete-web-development-bootcamp/?couponCode=25BBPMXPLOYCTRL#instructor-1">Dr. Angela Yu, Developer and Lead Instructor Profile</a>
<a href="https://codepip.com/games/grid-garden/" target="_blank">CSS Grid Garden Game/a>
<a href="https://codepip.com/games/flexbox-froggy/" target="_blank">Game/a>Flexbox Froggy</a>


