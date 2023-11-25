**Test: Basic CSS Concepts**

1. **Explain the CSS Box Model.**

   - Answer: The CSS Box Model is a fundamental concept in web design and development, which describes how every web page element is modeled as a rectangular box. It consists of margins, borders, padding, and the actual content. The content is the space where text and images appear, padding is the whitespace inside the border around the content, the border is a potentially visible boundary around the padding, and margin is the outermost layer that handles the space between the box and neighboring elements. Understanding the box model is crucial for layout control and element sizing.

2. **Describe the difference between class and ID selectors in CSS.**

   - Answer: Class and ID selectors are both ways to target HTML elements for styling. A class selector can be used to style any number of elements by using the same class value, which makes it ideal for applying uniform styles to multiple elements. It's denoted with a period (.) followed by the class name. An ID selector is used for unique elements on a page since the ID must be unique within the page. It's denoted with a hash (#) followed by the ID value. IDs are generally used for elements that have a unique style or are targeted by JavaScript.

3. **What are pseudo-classes and pseudo-elements, and how do they differ?**

   - Answer: Pseudo-classes and pseudo-elements are special types of selectors in CSS. Pseudo-classes select elements based on their state rather than their name, class, or ID. For example, `:hover` can be used to define a style for when the user hovers over an element. Pseudo-elements, on the other hand, allow styling of part of an element. For example, `::first-line` selects the first line of text in an element, and `::before` creates a pseudo-element before the content of the selected element. They differ in that pseudo-classes define the state of an element, while pseudo-elements target specific content within an element.

4. **How do you apply multiple styles to a single selector, and how do you group multiple selectors?**

   - Answer: To apply multiple styles to a single selector, you list the desired properties and values within the selector's block in the CSS file. For example:

   ```css
   p {
     color: red;
     font-size: 14px;
     line-height: 1.6;
   }
   ```

   To group selectors, you list multiple selectors separated by commas, and the grouped selectors will share the same declared properties and values. Like so:

   ```css
   h1,
   h2,
   h3 {
     font-family: Arial, sans-serif;
     margin-top: 15px;
   }
   ```

   This approach reduces code redundancy and maintains a cleaner stylesheet.

5. **Give examples of text formatting properties in CSS.**
   - Answer: Text formatting in CSS is done using properties that affect the font and text appearance. Examples include `font-family` to specify the typeface, `font-size` for the size of the text, `font-weight` for the weight of the font (e.g., bold), `line-height` for the space between lines of text, `text-align` for horizontal alignment (e.g., left, right, center, justify), `color` for the text color, and `text-decoration` for adding decorations like underline or line-through.
