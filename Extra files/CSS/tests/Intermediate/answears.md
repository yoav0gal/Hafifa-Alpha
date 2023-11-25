**Test: Intermediate CSS Concepts**

1. **Describe the difference between block, inline, and inline-block display values.**

   - Answer: The `display` property determines the layout behavior of an element. `block` elements start on a new line and occupy the full width available, stacking vertically. Examples include `<div>` and `<p>`. `inline` elements do not start on a new line and only occupy as much width as necessary, allowing them to sit next to other elements horizontally, like `<span>`. `inline-block` elements are a mix, allowing elements to sit next to each other but still apply width and height values like a block element.

2. **How do Flexbox and CSS Grid differ in layout design?**

   - Answer: Flexbox is a one-dimensional layout method for laying out items in rows or columns. It's a great tool for distributing space and aligning items in a container when the size of the container or the size of the items is unknown. CSS Grid is a two-dimensional layout system that handles both rows and columns simultaneously, which is ideal for creating complex layouts and aligning content within a grid.

3. **Explain how media queries contribute to responsive design.**

   - Answer: Media queries allow CSS to apply different styles depending on a device's characteristics, like its screen size, resolution, or orientation. This is the cornerstone of responsive design, ensuring that a website is usable and aesthetically pleasing on mobile phones, tablets, and desktops. A media query can conditionally include a block of CSS properties only if a certain condition is true.

4. **Give an example of how to create an animation using keyframes in CSS.**

   - Answer: To create an animation with keyframes, you define the `@keyframes` rule with a name, and then specify the animation's stages, along with the CSS properties that should change at each stage. Then, you use the animation name in the element's style you want to animate. For example:

   ```css
   @keyframes fadeIn {
     from {
       opacity: 0;
     }
     to {
       opacity: 1;
     }
   }
   .fade-in-element {
     animation: fadeIn 2s;
   }
   ```

   This code will cause an element with the class `.fade-in-element` to fade in over two seconds.
