# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
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

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: https://sabineemden.github.io/qr-code-component/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```

```css
.proud-of-this-css {
  color: papayawhip;
}
```

```js
const proudOfThisFunc = () => {
  console.log("🎉");
};
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

#### Self-hosting custom web fonts

The font family for this project is [Outfit](https://fonts.google.com/specimen/Outfit). It is available as a variable font with weight as the variable axis. I opted to use static fonts. The project uses only two font weights, regular 400 and bold 700. The gain in performance from using the variable font would be minimal at best.

I used the [Font Subsetter](https://everythingfonts.com/subsetter) by Everything Fonts select only the Basic Latin glyphs within the Unicode range U+0020 to U+007E. These 95 glyphs are usually enough for English-only websites. To convert the TTF file format to WOOF and WOOF2, I used the [ttf to woff converter](https://everythingfonts.com/ttf-to-woff) and the [ttf to woff2 converter](https://everythingfonts.com/ttf-to-woff2), both also by Everything Fonts. This reduced the file size from 55kb each for the two original TTF files to 18kb each for the TTF subsets, 11kb for the WOFF subsets, and 9kb for the WOFF subsets.

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

#### Self-hosting custom web fonts

- [Self-hosting fonts explained (including Google fonts) // @font-face tutorial](https://www.youtube.com/watch?v=zK-yy6C2Nck) by Kevin Powell - This 16-minute video explains the basics of self-hosting custom web fonts. It covers getting fonts from Google fonts, converting from TTF to WOFF and WOFF2, adding fonts to a project, and setting up the font-face declaration in CSS.
- [A guide to subsetting fonts](https://the-sustainable.dev/a-guide-to-subsetting-fonts/) by sustainable.dev - This article is a brief step-by-step guide to subsetting web fonts with FontSquirrel's Webfont Generator.
- [Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator) by Font Squirrel - The Expert option offers fine-grained controls for subsetting fonts and converting the font format in one go, and works with more than one file at a time. It is much more convenient than Everything Fonts. Unfortunately, it didn't work with the original TTF font files I had.
- [How to load web fonts for the best page load performance](https://the-sustainable.dev/how-to-load-web-fonts-for-the-best-page-load-performance/) by sustainable.dev - This article give detailed instructions how to pre-load font files, use the correct font-face declaration, and avoid invisible text during font loading.

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
