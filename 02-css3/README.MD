# CSS

## Introduction to CSS
- [Overview of CSS]()

- [CSS Selectors](https://github.com/nyangweso-rodgers/Web-Applications/tree/main/css3/css-Selectors)

- [CSS Units](https://github.com/nyangweso-rodgers/Web-Applications/tree/main/css3/css-Units)
    - [Absolute Units]()
    - [Relative Units]()

- [Introduction to CSS3](#Introduction-to-CSS3)

# Overview of CSS
# Common CSS mistakes
1. __Not Using fallback fonts__: 
    - every computer doesn't have every font that yu use.
    - also, imported fonts like google fonts, sometimes for some reason may not get downloaded
    - so it's always better to use fallback fonts

    ```css
        body { 
            font-family: Roboto, Arial, sans-serif;
            }
    ```

2. __Using `px` for everything__:
   - if we use `px` units, every user  will see the same sized elements and is not good as every user has a different monitor.
   - instead of using `px` units, use `relative` units like `rem`, `em`, the elements will scale based on the size of the monitor screen size.

    ```css
        p {
            font-size: 1.3rem;
            line-height: 1.6;
            padding: 1em;
        }
    ```

3. __Complicating Selectors__:
   - example:

    ```css
        header .navigation ul.nav-links {
            line-style-type: none;
        }
    ```

    - when you can use direct class for a particular element, you should not complicate by nesting with different selectors

    ```css
        .nav-links { 
            line-style-type: none;
        }
    ```

4. __Repeating the same code__:
   - when there are same styles for multiple elements, don't repeat your code, just group selectors

    ```css
        #home-section {
            background-color: #f5f5f5;
            color: #202020;
        }
        #about-section {
            background-color: #f5f5f5;
            color: #202020;
        }
    ```
    - to group selectors, separate each selector with a comma:

    ```css
        #home-section, #about-section {
            background-color: #f5f5f5;
            color: #202020;
        }
    ```

5. __Using Color Names__:
    - avoid using color names since every browser doesn't display the same color
    - if you want the colors to function the sane in all browsers, use `hex`, `rgb` or `hsl`

    ```css
        .box {
            background-color: #f0f0f0;
        }
    ```

6. __`z-index` Mistakes__:
   - many developers use a really high `z-index` value to put an element in front.
   - and it becomes difficult when you want to put another elements in front of others. The `z-index` value starts increasing much higher.

    ```css
        .modal-container {
            z-index: 123;
            }
        .modal {
            z-index: 123456;
        }
    ```
    - the solution is to use moderate values, so that it doesn't become difficult for a long run

    ```css
        .modal-container {
            z-index: 1;
            }
        .modal {
            z-index: 2;
        }
    ```

7. __Not Using Shorthand__:
   - there are many properties which you can use both shorthand and longhand methods:

    ```css
        .container {
            margin-top:1em;
            margin-bottom:2em;
            margin-left:0;
            margin-right:0;
        }
    ```
    - most of these cases can be simplified by using the shorthand method

    ```css
        .container {
            margin: 1em 2em 0 0;
        }
    ```

8. Using `!important` more oftenly
9. Using `inline css`
10. Not organizing your css
11. inconsistent naming
12. using CSS's @import
13. Using ids insteadd of classes
14. Using only one stylesheet for everything