1. Put all of the card links you just made into a new container element. It's not going to be an `article` or a `section`, but one called `div`. It's a general purpose container you can use for grouping things and making nice layouts.
    ```html
        <div class="cardContainer">
    ```
2. Add the following CSS in your stylesheet:
    ```css
        .cardContainer {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding: 10px;
        }
    ```
    Voilà! Your cards are now displayed side by side! Drag the vertical slider on Trinket's code pane and watch how your the thumbnails move around to fit the window size.

3. Try deleting the `width` and `height` properties from the `.card` class and see what happens: Flex cleverly fits the cards together like a jigsaw puzzle, keeping an even height across everything that's in the same row.

4. If you have a navigation menu at the top of your page, that's another place you might use this trick. Find the CSS rules for your menu. If you prefer, you can try it out with my website. Delete `display: inline;` from the **list items** \(in my website, that's the `nav ul li` block.\). Then, in the list, `nav ul`, add in 
    ```css
        display: flex;
        justify-content: flex-start;
    ```
    You end up with pretty much the same menu, right? The cool thing about Flex is you can control the layout with the property `justify-content`. Change its value to `flex-end` and see what happens. Or change it to `space-around` to make the menu items evely spaced, just like you did for the cards.

5. A **responsive** website is one that adjusts itself to the screen size: so it always looks great whether you're looking at it on a computer, mobile phone or tablet. Let's make your menu responsive. Start with the regular styles: this will be your **default** behaviour.

6. Add the following CSS rules to your menu. You probably have colours and borders defined as well; I've left them out to save space here!
    ```css
        nav ul {
            padding: 0.5em;
            display: flex;
            flex-direction: column;
        }
        nav ul li {
            text-align: center; 
            list-style-type: none;
            margin-right: 0.5em;
            margin-left: 0.5em;
        }
    ```

6. You're going **mobile first**: the default style is good for small screens. You define different styles for bigger screens like this:
  ```css
        @media all and (min-width: 600px) {
            nav ul {
                flex-direction: row;
                justify-content: space-around;
            }
        }
   ```
   Everything inside this block applies whenever the window is wider than _600 pixels_. Can you add another block for screens bigger than _800 pixels_, with `flex-end` instead of `space-around`?

7. To test your code on full size screens, download your code and open the file _index.html_ in a browser. Adjust the width of the window to see the menu change! You can put any CSS rules you like into these blocks, to define different styles for different screen sizes. It'll be especially useful when you do **CSS grid** layouts later!