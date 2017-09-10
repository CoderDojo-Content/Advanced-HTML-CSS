1. A **responsive** website is one that adjusts itself to the screen size: so it always looks great whether you're looking at it on a computer, mobile phone or tablet. One way to make your website **responsive** is with the **Flexbox**.
2. Put all of the thumbnail links you just made into a new container element. It's not going to be an `article` or a `section`, but one called `div`. It's a general purpose container you can use for grouping things and making nice layouts.
    ```html
        <div class="thumbnailContainer">
    ```

3. Add the following CSS in your stylesheet:
    ```css
        .thumbnailContainer {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding: 10px;
        }
    ```
    Voilà! Your thumbnails are now displayed side by side! Drag the vertical slider on Trinket's code pane and watch how your the thumbnails move around to fit the window size.

4. You can use the same trick to make your navigation menu responsive. Delete `display: inline;` from `nav ul li`. Then, in `nav ul` add in 
    ```css
        display: flex;
        justify-content: flex-start;
    ```
    You end up with pretty much the same menu, right? The cool thing about Flex is you can control the layout with the property `justify-content`. Change its value to `flex-end` and see what happens. Or change it to `space-around` to make the menu items evely spaced, just like you did for the thumbnails.

5. -> responsive to screen size . BUT go mobile first, so do direction, no justify-content? by default, put the spare-around and flex-end into min-width x and y. **mention the mobile first thing**

6. To test your code on full size screens, download your code and open the file _index.html_ in a browser. Adjust the width of the window to see the menu change!




1. Create a div with a few pictures in it. They are arranged vertically.
2. set parent to display: flex; ----> they become horizontally arranged!
3. margin: auto; on the items ---> centered horizontally (possibly put this into total layout control as a neat trick in advance)