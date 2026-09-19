# CSS Float Intro

This repository contains the starter files for a Web Design 1 coding exercise introducing the CSS `float` property.

In this exercise, you will learn how to float an image so text wraps around it. You'll also learn why floats can be useful, why they can be tricky, and why modern web designers usually use other layout tools, such as Flexbox and Grid, for most page layout.

This is also the first exercise where you will make your own copy of an instructor template repository. Instead of downloading a ZIP file, you'll create your own GitHub repository from this starter project, clone it to your computer, complete the coding exercise, commit your changes, push them back to GitHub, and submit your repository URL in Canvas.

---

## Use Canvas for the Full Assignment Instructions

Canvas has the full assignment description, screencast videos, due date, and submission instructions.

This GitHub repository is where the starter files are stored.

For this exercise, follow the instructions in Canvas and watch the screencast videos in order. This README is here to help you understand the project, remember the main concepts, and check your work before submitting.

---

## Important: Make Your Own Copy

Do not edit my original repository.

For this assignment, you will make your own copy of the starter repository using GitHub’s template/copy process. Your copy will become your own repository.

After you create your own repository, you must clone your copy to your computer using GitHub Desktop. Then you will edit the files in Visual Studio Code.

The basic workflow is:

1. Create your own copy of this template repository.
2. Clone your copy to your computer using GitHub Desktop.
3. Open the project folder in Visual Studio Code.
4. Complete the coding exercise.
5. Save your files.
6. Commit your changes in GitHub Desktop.
7. Push your changes to GitHub.
8. Submit your repository URL in Canvas.

If you only change the files on your computer but do not commit and push, your instructor will not be able to see your finished work on GitHub.

---

## What You Will Practice

By completing this exercise, you will practice how to:

- Create your own repository from a starter template
- Clone a repository using GitHub Desktop
- Open a project folder in Visual Studio Code
- Use the CSS `float` property
- Compare floating an image with floating a figure
- Use a class selector to target a specific figure
- Add a background color, padding, width, and margin to a floated element
- Use a global responsive image rule
- Use the `clear` property to stop content from wrapping around a float
- Commit your changes in GitHub Desktop
- Push your committed changes to GitHub
- Submit a GitHub repository URL in Canvas

---

## Starter Files

This repository includes:

- `index.html`
- `reset.css`
- `styles.css`
- `ivan-cookie.jpg`
- `README.md`

The `index.html` file contains the page content.

The `reset.css` file helps reduce browser default styling differences.

The `styles.css` file is where you will write the CSS for this exercise.

The image file `ivan-cookie.jpg` is the image you will use when practicing floats.

Do not delete or rename the starter files unless your instructor specifically tells you to.

---

## Recommended Folder Organization

When you clone the repository, save it somewhere organized on your computer.

A good setup would be to create one main folder for this course, then place each coding exercise inside it.

Example:

- 📁`web-design-1`
  - 📁`handsome`
  - 📁`learning-html`
  - 📁`hollow-earth`
  - 📁`css-float-intro`

Keeping your files organized will make the course much easier. Web projects depend on file names and folder locations, so losing track of files can cause broken images, missing CSS, and other problems.

---

## Important: Open the Folder, Not Just One File

When working in Visual Studio Code, open the entire project folder.

Do not open only `index.html` by itself.

Opening the full folder allows VS Code to see all of the project files, including the HTML file, CSS files, image file, and README.

This matters because your HTML file needs to find the CSS and image files using file paths. If you open only one file, it is easier to get confused about where everything is located.

---

## A Short History of Floats

The CSS `float` property was originally created to allow text to wrap around images, similar to what you might see in a newspaper or magazine layout.

For example, an image could float to the right side of a paragraph while the text flows around it on the left.

For many years, web designers also used floats to create entire page layouts. Before Flexbox and Grid were supported, floats were one of the main ways to put columns next to each other on a webpage. Today, we don't use floats for full page layout anymore.

Modern CSS layout tools are better for that:

- **Flexbox** is better for one-dimensional layouts, such as rows, columns, navigation bars, and groups of cards.
- **Grid** is better for two-dimensional layouts, such as page structures with rows and columns.

However, floats are still useful for smaller effects, especially when you want text to wrap around an image, figure, or pull quote.

That is why floats are still worth learning.

---

## What the Float Property Does

The CSS `float` property moves an element to the left or right side of its container and allows surrounding inline content, such as text, to wrap around it.

Common values include:

- `float: left;`
- `float: right;`
- `float: none;`

A left float moves the element to the left side.

A right float moves the element to the right side.

The value `none` removes the float and returns the element to normal document flow.

---

## Why Floats Can Be Confusing

Floats can be useful, but they have quirks.

When an element is floated, it's partly removed from normal document flow. That means surrounding text may wrap beside it, but other block elements may behave in ways that seem unexpected at first.

For example:

- Text may wrap beside the floated item.
- The parent container may not fully stretch around the floated item.
- Later sections may continue wrapping beside the float when you expected them to start underneath it.
- Images may overflow if their container is too narrow.
- Captions may not move with images if you only float the image instead of the whole figure.

This exercise is designed to help you see those quirks directly.

---

## Why We Don't Usually Float Every Image

At the beginning of the exercise, you'll create a rule like:

- `img { float: right; }`

That works, but it is usually not a good long-term choice.

The selector `img` targets every image on the page. If your page has several images, they would all float, even if you only wanted one specific image to move to the side.

A better approach is to give one element a class, then target that specific class in CSS.

For example:

- Add a class to the figure you want to float.
- Use a class selector in CSS to style only that figure.

This gives you more control.

---

## Floating an Image vs. Floating a Figure

One important part of this exercise is seeing the difference between floating just an image and floating a figure.

If you float only the image, the image will move to the side, but the caption will stay behind.

That happens because the image and caption are separate elements.

A better solution is to wrap the image and caption in a `figure` element, then float the entire figure.

That way, the image and caption move together as one unit.

This is an important design idea:

Sometimes you style the individual element.

Other times you style the container that holds related elements together.

---

## The Figure Element

The `figure` element is used for content that is related to the main page content but can also stand on its own.

A common use is grouping an image with its caption.

In this exercise, the figure will contain:

- an image
- a figcaption

The `figcaption` element provides a caption for the figure.

This is more meaningful than placing an image and caption randomly in the page, because the HTML structure shows that the caption belongs with the image.

---

## The Responsive Image Rule

A useful global image rule is:

- `img { max-width: 100%; height: auto; }`

This rule helps images fit inside their containers.

The `max-width: 100%;` rule tells the image not to be wider than the container it is inside.

The `height: auto;` rule keeps the image proportional so it does not look stretched or squished.

This is one of the few times when using the `img` selector globally is a good idea, because it is a general safety rule that can help all images behave better.

---

## Why Width Matters

When you float a figure, you will usually give it a width.

Without a width, the browser may allow the figure to take up more space than you expect.

A width gives the floated element a predictable size so the text can wrap around it more cleanly.

In this exercise, you may use a width such as:

- `width: 200px;`
- `width: 250px;`

At this stage, pixel widths are easier to understand. Later, you will learn other ways to size elements for more flexible layouts.

---

## Why Margin Matters

Floated elements often need margin.

If you float an image or figure without margin, the surrounding text may sit too close to it. That makes the page harder to read and can look crowded.

For example, if a figure is floated to the right, you might add space on the left and bottom:

- `margin-left: 1rem;`
- `margin-bottom: 1rem;`

This creates breathing room between the floated figure and the text.

---

## The Clear Property

The `clear` property controls whether an element is allowed to sit beside floated elements.

A common rule is:

- `clear: both;`

This tells the element to move below floated elements on either side.

In this exercise, the bottom section of the page explains floats. That section can be used to demonstrate what happens when content continues wrapping beside a float.

If you want that section to start underneath the floated figure, you can use `clear`.

For example:

- `.float-notes { clear: both; }`

This is useful when you want one part of the page to stop wrapping and begin underneath the float.

---

## What You Will Change in the HTML

In the HTML file, you will start with an image.

During the exercise, you will wrap that image in a `figure` element and add a caption.

You will also add a class to the figure so you can target it in CSS.

The class name may be something like:

- `cats`

That class lets your CSS style one specific figure instead of every image on the page.

---

## What You Will Change in the CSS

In the CSS file, you will practice several rules.

You may start by trying to float all images.

Then you will delete or replace that approach because it is too broad.

Next, you will target the specific figure using a class selector.

You will add styles such as:

- `float`
- `background-color`
- `padding`
- `width`
- `margin`
- `max-width`
- `height`
- `clear`

The exact code will be demonstrated in the course videos.

---

## GitHub Workflow Reminder

For this assignment you will submit the URL of your GitHub repository instead of a ZIP file submission.

That means you need to make sure your work gets uploaded to GitHub.com.

The basic GitHub Desktop workflow is:

1. Make changes in VS Code.
2. Save your files.
3. Open GitHub Desktop.
4. Review the changed files.
5. Write a short commit message.
6. Click Commit.
7. Push your changes to GitHub.

A commit saves a checkpoint.

A push uploads that checkpoint to GitHub.com.

Your instructor can only see files that have been pushed to GitHub. Nobody else can see files that are only on your laptop.

---

## Before You Submit

Before submitting your work in Canvas, check the following:

- You created your own repository from the template
- You cloned your own repository to your computer
- You opened the full project folder in VS Code
- Your HTML file is named `index.html`
- Your CSS file is linked correctly
- Your image appears in the browser
- Your image has useful `alt` text
- The image and caption are grouped in a `figure`
- The `figure` has a class
- The figure floats to the left or right
- The figure has a visible background color and padding
- The figure has a width
- The image fits inside the figure
- The floated figure has margin so the text has breathing room
- The bottom notes section clears the float if instructed
- Your page looks correct when opened in a browser
- Your changes have been committed in GitHub Desktop
- Your changes have been pushed to GitHub
- The repository URL you submit opens your repository on GitHub.com

---

## What to Submit

Submit the URL of your GitHub repository in Canvas.

Do not submit only a screenshot.

Do not submit a ZIP file unless your instructor specifically asks for one.

The submitted URL should look something like:

- `https://github.com/your-username/css-float-intro`


Before submitting, open your repository URL in a browser and make sure it goes to your GitHub repository.

---

## Troubleshooting Tips

If something is not working, check these common issues first.

### My image does not show up

Check:

- Did you save the HTML file?
- Is the image file in the correct folder?
- Is the image file name spelled exactly the same way in the HTML?
- Does the file extension match?
- Did you accidentally move or delete the image?

Remember that these are different file names:

- `ivan-cookie.jpg`
- `Ivan-Cookie.jpg`
- `ivan-cookie.jpeg`
- `ivan_cookie.jpg`

Small differences matter.

### My caption is not floating with the image

You may have floated the `img` instead of the `figure`.

If you want the image and caption to move together, float the figure that contains both of them.

### My image is spilling outside the figure

Make sure you added the responsive image rule:

- `img { max-width: 100%; height: auto; }`

This helps the image shrink to fit inside the figure.

### My text is too close to the image

Add margin to the floated figure.

If the figure floats right, add space on the left.

If the figure floats left, add space on the right.

You may also want margin on the bottom.

### My next section is still wrapping beside the float

Use the `clear` property on the section that should start underneath the float.

A common rule is:

- `clear: both;`

### GitHub does not show my latest work

Check GitHub Desktop.

You may have saved your files locally but forgotten to commit or push.

Remember:

- Saving updates the files on your computer.
- Committing creates a checkpoint.
- Pushing uploads the checkpoint to GitHub.com.

Your instructor can only see the work that has been pushed to GitHub.

---

## Final Reminder

Floats are older than Flexbox and Grid, but they are still useful for certain design effects.

The main goal of this exercise is not to use floats for an entire page layout. The goal is to understand how text can wrap around a floated element and how to control the quirks that come with that behavior.

Once you understand floats, you will be better prepared to appreciate why modern layout tools like Flexbox and Grid are so helpful.
