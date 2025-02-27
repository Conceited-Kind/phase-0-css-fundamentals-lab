# CSS Fundamentals Lab

## Learning Goals

- Link an external CSS file
- Write CSS rules to style HTML

## Introduction

In this lab, we will be adding style to our `index.html` page by linking an
external CSS file. If you open `index.html` in the browser, you will see basic
HTML that has been provided. The website emulates a basic Real Estate website
(the links on it have been disabled, we will be working with only the basic
`index.html` landing page).

As you can see, our basic page is rather lackluster. This is where you come in!
You will be adding CSS, using selectors, to jazz the page up. All of our CSS
should be written in `style.css`.

## Getting Started

**Fork and clone** this lesson into your local environment. Navigate into its
directory in the terminal, then run `code .` to open the files in Visual Studio
Code. Run `npm test` as you work through this assignment to see your progress.

## Link an External CSS File

As usual, we need to make sure our HTML is loading our style sheet.

We have two options:

1. Write CSS rules inside of a `<style>` tag ("internal CSS"), which tells HTML
   "Hey, I want to define some CSS styling here"
2. Write CSS rules in an external file that is specified with the `<link>` tag
   ("external CSS").

In our case, we want to provide a link to our style sheet, instead of writing
all of our CSS code directly in the `<style>` tag. This allows us to only have
to write styles for the entire site once, instead of repeating every `<style>`
element on every page. A common workflow is to see developers work on CSS inside
of the `<style>` tag until their styling is done. At that point, they move it to
their external file and remove the `<style>` element from the HTML page. Feel
free to try it out!

In `index.html`, provide a `<link>` tag which correctly sources the CSS file
located in this directory. The `<link>` tag will link to our file with an `href`
attribute, like so:

```html
<link rel="stylesheet" href="relative path to CSS file" />
```

Links to style sheets should go at the end of the `<head>` section! Make sure
you provide a _relative_ path to the style sheet.

Now, what is a relative path? You could write `href="style.css"` and the content
of `style.css` would change your `index.html` file. But we want to teach you to
require external resources (like CSS or JavaScript) by using _relative paths_.
Relative paths make it _crystal clear_ which file is being used. Relative paths
start with `./` which means "from the directory I am currently in." So, when we
use `link` to associate with a style sheet and we write `href="./style.css"`
we're saying: "From the directory in which I, the `index.html` file live, look
for a file called `style.css` and use it." This pattern will help you and other
developers remove any possible confusion.

Hint: Try adding the following temporarily to your `style.css` file to test if
your linked CSS is working:

```css
h1 {
  color: red;
}
```

If you see your `<h1>` change to red, you've linked your style sheet correctly!
Don't forget to delete it once you have your link working.

## Write CSS Rules to Style HTML

For this exercise, we are going to be transforming our base HTML into a more
exciting version using CSS.

It is important to note that there are _many_ ways to go about transforming the
HTML with CSS to match the end product. For this lesson, we will provide you
with general guidance in _one way_ of getting to the desired view by adding to
the `style.css`. Ultimately, the goal is to have your website look like the
finished product whatever way works the best for you.

**Note:** If you are having trouble finding the specific CSS property you need
to get a specific visual outcome, use your Google skills with queries such as:
"CSS center text within div".

In following the guidelines, you should be referencing the `index.html` to find
the appropriate tags/IDs that we will use as selectors in our `style.css` file.
Don't forget: you can use the Chrome Inspector Tool (`cmd + shift + C` on Mac)
to inspect specific elements of the DOM (and make trial changes to their CSS) in
the browser.

### What We Have

![incomplete lab](https://curriculum-content.s3.amazonaws.com/fewds-css/css-fundamentals-lab-incomplete.png)

### What We Want

![complete lab](https://curriculum-content.s3.amazonaws.com/fewds-css/css-fundamentals-lab-complete.png)

### Deliverables

f the `width` of the bottom row (since we have 4 divs).

## Conclusion

CSS allows many avenues to the same goal. The important takeaway is to
experiment and become familiar with the commonly used rules. This will enable
you to identify what properties will get you to which end result the quickest.

You will find that even years into your career as a front end developer, you
will be referencing basic CSS documentation. _This is to be expected!_ To be
comfortable quickly finding the property/value you are looking for online is the
most important skill set you can develop right now. Memorization is for
machines, adaptation is for humans!

[un-styled]:
  https://curriculum-content.s3.amazonaws.com/web-development/unstyled-codepen.jpeg
[styled]:
  https://curriculum-content.s3.amazonaws.com/web-development/styled-codepen.jpeg
