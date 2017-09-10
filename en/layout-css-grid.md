1. Let's look at the Attractions page. At the moment all the elements are displayed one after the other. You are going to make a more interesting layout by writing some CSS classes. The container you'll change the layout of is `main`, but you could do this with any kind of container, like `div` or `article`, or even the whole page `body`.

2. `main` contains three elements: one `article` and two `aside`s. Give each one a new css class, and give `main` another.

    ```html
        <main class="attPageLayoutGrid">
            <article class="attGridArticle">
                <!--other stuff here-->
            </article>
            <aside class="attGridAside1">
                <!--other stuff here-->
            </aside>
            <aside class="attGridAside1">
                <!--other stuff here-->
            </aside>
        </main>
    ```
3. To design the layout, you're going to use **CSS grid**. In the overall container, you set the `display` property to `grid`:
    ```css
        .attPageLayoutGrid {
            display: grid;
            grid-column-gap: 0.5em;
            grid-row-gap: 1em;
        }
    ```
    What do you think the `grid-column-gap` and `grid-row-gap` properties do?
4. Next, you name a `grid-area` for each element: 
    ```css
        .attGridArticle {
            grid-area: agArticle;
        }
        .attGridAside1 {
            grid-area: agAside1;
        }
        .attGridAside2 {
            grid-area: agAside2;
        }
    ```
5. Then you design your layout! Let's put the two `aside` elements side by side at the bottom. For this you need two **columns** of equal width. You can keep the **row** height automatic. Put the following code inside the `.attPageLayoutGrid` rules:
    ```css
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto;
        grid-template-areas: 
            "agArticle agArticle"
            "agAside1 agAside2";
    ```
    Notice how you make the `article` take up all the space over the two columns
    * `fr` stands for _fraction_. You could use `px` if you wanted exact measurements instead of proportional ones.

6. Let's try putting the `aside` elements over on the right, and making them half the width of the `article`. Change your code to:
    ```css
        grid-template-columns: 2fr 1fr;
        grid-template-rows: auto;
        grid-template-areas: 
            "agArticle agAside1"
            "agArticle agAside2";
    ```

7. If you don't want the `aside` elements to stretch all the way to the bottom, you can add in another row, and put a blank space on it using a dot: 
    ```css
        grid-template-columns: 2fr 1fr;
        grid-template-rows: auto;
        grid-template-areas: 
            "agArticle agArticle"
            "agArticle agAside2"
            "agArticle .";
    ```
8. Here's what the layout looks like for each of these three examples:


9. You can make almost any layout you like using CSS grid. In this example the header and footer were left out of the design, but they could be included in the grid too. 
 * Like Flex, covering all the details would easily fill a whole Sushi Series on its own. If you want to learn more about CSS grid, go to dojo.soy/a-html-css-grid 