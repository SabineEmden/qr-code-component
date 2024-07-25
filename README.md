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

![screenshot of solution to QR code component challenge](./screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- GitHub repository: https://sabineemden.github.io/qr-code-component/
- Live Site URL: https://sabineemden.github.io/qr-code-component/

## My process

### Built with

- Semantic HTML5 markup
- Self-hosted static web fonts

### What I learned

For this challenge, I took a deep dive into web sustainability best practices for custom web fonts.

The font family for this project is [Outfit](https://fonts.google.com/specimen/Outfit). It is available as a variable font with weight as the variable axis. I opted to use static fonts. The project uses only two font weights, regular 400 and bold 700. The gain in performance from using the variable font would be minimal at best, and static fonts have better browser support.

I used the [Font Subsetter](https://everythingfonts.com/subsetter) by Everything Fonts to select only Basic Latin glyphs within the Unicode range U+0020 to U+007E. These 85 glyphs are usually enough for English-only websites. Subsetting the fonts reduced the file size from 55kb each for the two original TTF files to 18kb each for the TTF subsets.

To convert the TTF file format to WOOF and WOOF2, I used the [ttf to woff converter](https://everythingfonts.com/ttf-to-woff) and the [ttf to woff2 converter](https://everythingfonts.com/ttf-to-woff2), both also by Everything Fonts. The file conversions reduced the file size to 11kb for the WOFF subsets, and 9kb for the WOFF2 subsets.

In the `@font-face` declarations in the CSS style sheet, I listed the WOOF2 files followed by the WOOF files. Browsers will go down the list until they find a file they can use.

```css
@font-face {
  font-family: "Outfit";
  font-weight: 400;
  font-display: swap;
  src: url("./fonts/Outfit-Regular-subset.woff2") format("woff2"),
    url("./fonts/Outfit-Regular-subset.woff") format("woff");
}

@font-face {
  font-family: "Outfit";
  font-weight: 700;
  font-display: swap;
  src: url("./fonts/Outfit-Bold-subset.woff2") format("woff2"),
    url("./fonts/Outfit-Bold-subset.woff") format("woff");
```

I decided not to include the `local()` function in the font-face declaration to look for local font files. The probability for Outfit to be installed as a local font on the user's device is rather small.

In this project, both font weights are 'above the fold'. I decided to preload the WOFF2 files for both fonts. The browser will use the `type` attribute to check if it supports the font file format and only download the files if it does, ignoring them if not.

```html
<link
  rel="preload"
  href="./fonts/Outfit-Bold-subset.woff2"
  as="font"
  type="font/woff2"
  crossorigin="anonymous"
/>
<link
  rel="preload"
  href="./fonts/Outfit-Regular-subset.woff2"
  as="font"
  type="font/woff2"
  crossorigin="anonymous"
/>
```

### Continued development

I want to continue focusing on sustainable web development in future projects and explore more web sustainability best practices.

### Useful resources

- [Self-hosting fonts explained (including Google fonts) // @font-face tutorial](https://www.youtube.com/watch?v=zK-yy6C2Nck) by Kevin Powell - This 16-minute video explains the basics of self-hosting custom web fonts. It covers getting fonts from Google fonts, converting from TTF to WOFF and WOFF2, adding fonts to a project, and setting up the font-face declaration in CSS.
- [The performance cost of custom web fonts, and how to solve it](https://www.wholegraindigital.com/blog/performant-web-fonts/) by Wholegrain Digital - This article from the year 2019 was the starting point for my deep dive into web sustainability best practices for custom web fonts.
- [A guide to subsetting fonts](https://the-sustainable.dev/a-guide-to-subsetting-fonts/) by sustainable.dev - This article is a brief step-by-step guide to subsetting web fonts with FontSquirrel's Webfont Generator.
- [Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator) by Font Squirrel - The Expert option offers fine-grained controls for subsetting fonts and converting the font format in one go, and works with more than one file at a time. It is much more convenient than Everything Fonts. Unfortunately, it didn't work with the original TTF font files I had.
- [How to load web fonts for the best page load performance](https://the-sustainable.dev/how-to-load-web-fonts-for-the-best-page-load-performance/) by sustainable.dev - This article give detailed instructions how to pre-load font files, use the correct font-face declaration, and avoid invisible text during font loading.

## Author

- Frontend Mentor - [@SabineEmden](https://www.frontendmentor.io/profile/SabineEmden)

## Acknowledgments

This project uses Josh Comeau's [CSS reset](https://www.joshwcomeau.com/css/custom-css-reset/).
