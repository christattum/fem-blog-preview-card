# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Figma Dev Mode
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### TODO

- Hover styles

### What I learned

Subscribed to paid Figma subscription to use Dev Mode. This makes pulling CSS and custom properties much quicker. I wanted to get familar with the professional workflow as soon as possible. I am not a total beginner at CSS so I thought this was a good approach.

Also brushed up on Flexbox which I used for the main card content using flex-direction: column. Learneed that by default items stretch to fill full width. After trying unsuccessfuly to get inline-block to work, which it doesn't, the correct fix was to assign the align-self: flex-start property to the category.


```css
.card .content {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-150);
}

.card .category {
  align-self: flex-start;
}
```

### Responsive Fonts

To avoid using media queries, I used a technique I learned a while ago, to use the clamp() function to dynamically scale fonts based on the view width.

First I added three CSS variables for the three font sizes:-

```css
  --font-size-heading: 2.4rem;
   --font-size-body: 1.4rem;
  --font-size-desc: 1.6rem;
```

These are the desktop sizes. The mobile sizes are:-

```css
  --font-size-heading: 2rem;
  --font-size-body: 1.2rem;
  --font-size-desc: 1.4rem;
```

Using the utility here:-
https://clamp-calculator.netlify.app/

Note: I'm using the 62.5% root font size trick, so I can use rems instead of pixels, where 1 rem = 10px so the maths is easy :) In the utility, set 1rem = 10px to reflect this.

I plugged the two variables in with the two view widths for desktop and mobile which are 1440px and 375px respectively (from the style guide).

```css
--font-size-heading: clamp(2rem, 1.859rem + 0.376vw, 2.4rem);
--font-size-body: clamp(1.2rem, 1.13rem + 0.188vw, 1.4rem);
--font-size-desc: clamp(1.4rem, 1.33rem + 0.188vw, 1.6rem);
```

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
