**Test: Advanced CSS Topics**

1. **What are CSS variables and how can you use them?**

   - Answer: CSS variables, also known as custom properties, are entities defined by CSS authors that contain specific values to be reused throughout a document. They are set using the `--` prefix and accessed with the `var()` function. For example:

   ```css
   :root {
     --main-bg-color: #333;
   }
   body {
     background-color: var(--main-bg-color);
   }
   ```

   This code sets a global variable for the main background color and then uses it for the body's background color.

2. **How do pseudo-classes like :nth-child work?**

   - Answer: Pseudo-classes like `:nth-child` select elements based on their position within a parent element or sequence. For example, `li:nth-child(2)` targets the second `<li>` element within its parent. This pseudo-class can take a formula as an argument, allowing for complex selection patterns like every odd row in a table or every third item in a list.

3. **Explain the use of the @supports rule.**

   - Answer: The `@supports` rule checks if the browser supports certain CSS features before applying styles. This is used to feature-detect CSS properties and values, providing a way to apply fallbacks or alternative styles. For instance, you can use `@supports` to detect grid layout support and provide a flexbox fallback if not supported.

4. **Describe a use case for the will-change property.**

   - Answer: The `will-change` property is used to inform the browser of likely changes to an element's style, allowing for performance optimizations. It should be used sparingly, for instance, when an element will undergo animations or transformations. This hint allows the browser to prepare for the change, potentially reducing flicker or lag.

5. **What is the advantage of using a preprocessor like SASS?**
   - Answer: Preprocessors like SASS extend CSS with features not available in pure CSS, such as variables, nesting, mixins, and functions. This can simplify the task of writing complex CSS and improve maintainability by allowing for smaller, modular files and clearer style logic. For instance, SASS variables can be used across multiple files, and mixins can insert a group of styles with a single directive.

By preparing for and understanding these intermediate and advanced concepts, a programmer can effectively handle a wide range of web design challenges and build responsive, efficient, and well-architected websites.
