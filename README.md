# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:
* Examples of semantic and non-semantic tags
* The differences between semantic and non-semantic tags
* The benefits of using semantic tags (when possible)

### Response 1
Semantic tags like `header`, `footer`, `main`, and `nav` convey the meaning of the content they enclose, while non-semantic tags like `div` are primarily used for layout and styling. The key difference is that semantic tags describe the structure and role of content, making the webpage easier to understand for both browsers and humans, while non-semantic tags have no specific meaning and are used for formatting and styling purposes.

The benefits of using semantic tags include better accessibility, as they allow screen readers to interpret the page's structure more easily and provide context for users with disabilities. Additionally, semantic tags help improve content indexing, allowing search engines to crawl and index the page more efficiently, leading to better rankings. Using semantic tags, the structure of the webpage becomes clearer and more organized, benefiting both users and search engines.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2
To make a website more accessible, developers can implement several key practices:

1. **Use Semantic HTML Tags**: Tags like `header`, `footer`, `main`, and `nav` help screen readers understand the structure and purpose of the content, making it easier for users with visual impairments to navigate.
2. **Ensure Keyboard Navigation**: Make sure all interactive elements, like forms and buttons, are accessible vis keyboard, allowing users with motor disabilities to navigate easily.
3. **Responsive Design**: A responsive website adjusts to different screen sizes and devices, providing a consistent experience for all users, including those using mobile phones, or assistive technologies.
4. **Provide Text Alternatives**: Add alt text to images and captions to videos so that users with visual or hearing impairments can understand the content.
5. **Color Contrast and Readability**: Ensure there is enough contrast between text and background colors for users with low vision or color blindness to read the content easily.

#### Why It's Important for Developers to Create Accessible Websites:

Creating accessible websites is important because it ensures that all users, regardless of their abilities, can access and interact with the content. It also helps developers comply with legal requirements, avoid potential lawsuits, and enhance the overall user experience. Additionally, accessible websites tend to be better structured, which can improve SEO and make it easier for search engines to index the content. In short, accessibility expands the reach of your website and makes it inclusive for everyone.


## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;" >hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

Writing inline styles might be considered useful because they allow you to quickly apply styles directly to a single element without needing an external CSS file. However, writing styles in a separate CSS file is generally a better practice because it keeps the HTML focused on structure, while the CSS file handles the styling. This separation makes the code easier to maintain, especially as the site grows. Inline styles can become cumbersome and harder to manage if used extensively, while a separate CSS file allows for consistent styling across the site and easier updates.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

* An explanation of the concept of "classes" and "ids" with an analogy.
* An example of the usage using an HTML code block and a CSS code block.
* An explanation of the syntax using the terms: **attribute**, **selector** 

### Response 4
In HTML, `class` and `id` attributes help us identify elements on a webpage, but they serve different purposes. Think of an **ID** as a unique name for a single person, while a **class* is like a label for a group of people who share something in common. 

- **ID**: Just like every person has a unique ID number that only they possess, each element with an `id` should have a unique identifier. This means you can only use one element with a specific ID on a page, and it’s used to target that specific element, much like calling out a specific person by their unique name.

- **Class**: Now, imagine you have a group of people who are all part of the same team. You can label them all with the same class (like "Team A") so that you can refer to any member of that team, not just one person. A `class` can be applied to multiple elements, and it’s used to style all elements that share that class, just like you would treat every person in the group similarly.

```html
<!-- ID -->
<p id="principal">Mr. Smith</p>
<p id="assistant-principal">Ms. Anderson</p>

<!-- Classes -->
<p class="teacher">Ms. Miller</p>
<p class="teacher">Mr. Davis</p>
<p class="teacher">Ms. Rodriguez</p>

```

In the HTML code above:

- The two elements with the `id` attribute, `principal` and `assistant-principal`, represent two unique individuals.
- The three elements with the `class` attribute of `teacher` represent a group of teachers.

```css
/* ID Selector */
#principal {
    color: blue;
}

#assistant-principal {
    color: purple;
}

/* Class Selector */
.teacher {
    color: yellow;
}

```

In this CSS code:

- The `#` selector targets elements with a specific `id`. For example, the `#principal` selector applies a blue color to the element with the ID of `principal`, and `#assistant-principal` applies purple to the element with the ID of `assistant-principal`.

- The `.` selector targets elements with a `class`. In this case, `.teacher` applies a yellow color to all elements with the class `teacher`.

#### Explanation of Syntax:
- **Attribute**: The `id` and `class` are attributes in HTML, which provide additional information about an element. The `id` attribute is unique and identifies a single element, while the `class` attribute can be used by multiple elements to group them together.
  
- **Selector**: In CSS, a **selector** is used to target specific HTML elements to apply styles to them. An `id` selector is prefixed with `#,` for example, `#principal,` and a `class` selector is prefixed with. ``, for example, `.teacher.`


## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

When building a website, **HTML** and **CSS** are used for the structure and styling, while **JavaScript** and the **DOM API** are used to add interactivity and dynamic content.

- **HTML and CSS**: Use HTML for the static structure (headings, paragraphs, images, etc.) and CSS for styling (colors, layout, fonts). This content stays the same after the page loads.
- **JavaScript and the DOM API**: Use JavaScript with the DOM to make the website interactive or dynamic. For example, updating content, handling user input, and modifying elements on the page in response to actions.

#### Best Practice:

It's not the best practice to build everything with JavaScript. HTML provides a semantic structure that is important for accessibility and SEO. JavaScript should be used to enhance interactivity, not replace basic content.
