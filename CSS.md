# CSS

The primary objectives of a project are to ensure optimal performance and deliver a high-quality product that satisfies the customer. One crucial aspect of achieving these goals is the organization and management of stylesheets. In this guide, we will discuss the logic and structure behind stylesheets in projects, with a focus on reducing file quantity and enhancing page load speed.

## Strategy Overview

To achieve our main goals of optimizing performance and satisfying customers with a quality product, we need to focus on the logic and structure behind stylesheets in projects. Our strategy aims to reduce the number of file requests and improve page load speed. Here's a concise overview:

1. **Identify Similar Elements**: Find elements that share common characteristics.

2. **Understand Element Roles**: Evaluate the roles of these elements in the HTML structure.

3. **Analyze Role Differences**: Identify any differences in style requirements for elements with similar roles.

4. **Create a Blueprint File**: Develop a blueprint stylesheet that provides basic styling for semantic elements and emphasizes above-the-fold content.

5. **Generate Page-Specific Stylesheets**: Create a main stylesheet for each page with specific, properly named, and well-structured custom classes. Load these stylesheets after the blueprint stylesheet.

6. **Consider Component-Specific Stylesheets**: Optionally, create separate components and stylesheets for elements that repeat or have slightly different styles.

7. **Performance Considerations**: For projects with few pages and elements, using a single stylesheet may be suitable, but always prioritize performance.

By implementing this strategy, we can minimize file requests, enhance page load speed, and ensure a satisfying user experience.

The stylesheets structure will looks like that:

```bash
├── css
│   ├── blueprint.css
│   ├── repeatcomponent.css
│   ├── landingpage.css
│   └──...
```


## Recomendations:

1. **Use a CSS Reset**: different browsers may have varying default margins, padding, and other styles for semantic elements, employing a CSS Reset ensures consistent rendering across different platforms.

    ```css
    /* Example of a simple CSS reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    ```

2. **Use Descriptive and Consistent Naming**: Consistent and descriptive naming makes your code easier to read and understand.

    ```css
    /* Not Recommended */
    .s-scr {
      ...
    }

    /* Recommended */
    .sidebar-scroll {
      ...
    }
    ```

3. **Use Shorthand Properties**: Shorthand properties help to reduce the amount of code and increase readability.

    ```css
    /* Not Recommended */
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 10px;
    margin-left: 20px;

    /* Recommended */
    margin: 10px 20px;
    ```

4. **Avoid Using `!important`**: Using `!important` can make debugging more difficult by breaking the natural cascading in your stylesheets.

    ```css
    /* Not Recommended */
    .container {
      padding: 10px !important;
    }

    /* Recommended */
    .container {
      padding: 10px;
    }
    ```

5. **Use Relative Units**: Relative units like `em`, `rem`, or `%` are flexible and scalable, making them a better choice for responsive web design.

    ```css
    /* Not Recommended */
    .container {
      font-size: 16px;
    }

    /* Recommended */
    .container {
      font-size: 1em;
    }
    ```

6. **Use Comments Wisely**: Comments can help organize your code and make it more readable to others.

    ```css
    /* 
      This is a multi-line comment
      It can span multiple lines
    */

    // This is a single line comment
    ```

7. **Structure CSS With a Top-Down Approach**: Start global and go more specific. For example, define general styles like font and color first, then go into more detail.

    ```css
    body {
      font-family: Arial, sans-serif;
      color: black;
    }

    .container {
      background-color: white;
    }

    .sidebar {
      background-color: grey;
    }
    ```

8. **Use a Preprocessor**: Preprocessors like Sass or Less provide more functionality and can make your code cleaner.

    ```scss
    // With SCSS
    $font-stack: Helvetica, sans-serif;
    $primary-color: #333;

    body {
      font: 100% $font-stack;
      color: $primary-color;
    }
    ```

9. **Modularize CSS**: Breaking down your CSS code into separate parts can make it more maintainable. It is a good idea to have all of the common styling first in the stylesheet. This means all of the styles which will generally apply unless you do something special with that element. You will typically have rules set up for:

    ```css

        body {
            ...
        }

        h1, h2, h3, h4 {
            ...
        }

        ul {
            ...
        }

    ```

10. **Use BEM (Block Element Modifier) Methodology**: BEM is a naming methodology that provides a more strict approach to CSS architecture. It makes your code scalable and reusable, making it more maintainable.

    ```css
    /* BEM CSS example */
    .block {
      ...
    }

    .block__element {
      ...
    }

    .block--modifier {
      ...
    }
    ```
