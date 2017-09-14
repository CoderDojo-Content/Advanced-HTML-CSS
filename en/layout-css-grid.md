1. You should now have a page where **main** contains three elements: one **article** and two **aside**. Add new CSS classes to **main** and each of three elements inside it.
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
   The container you'll change the layout of is **main**, but you could do this with any kind of container, like a **div** or **article**, or even the whole page **body**. The technique you're going to use is called **CSS grid**.

2. Set the **display** property to _grid_ on the overall container:
   ```css
        .attPageLayoutGrid {
            display: grid;
            grid-column-gap: 0.5em;
            grid-row-gap: 1em;
        }
   ```
    What do you think the **grid-column-gap** and **grid-row-gap** properties do?

3. Next, you name a **grid-area** for each element: 
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
4. Then you design your layout! Let's put the two **aside** elements side by side at the bottom. For this you need two **columns** of equal width. You can keep the **row** height automatic. Put the following code inside the _.attPageLayoutGrid_ CSS rules:
   ```css
        grid-template-rows: auto;
        grid-template-columns: 1fr 1fr;
        grid-template-areas: 
            "agArticle agArticle"
            "agAside1 agAside2";
   ```
    _fr_ stands for _fraction_. You could use _px_ if you wanted exact measurements instead of proportional ones. Notice how you make the **article** take up all the space over the two columns.

5. Let's try putting the **aside** elements over on the right, and making them half the width of the **article**. Change the values of **grid-template-columns** and **grid-template-areas** to:
   ```css
        grid-template-columns: 2fr 1fr;
        grid-template-areas: 
            "agArticle agAside1"
            "agArticle agAside2";
   ```

6. If you don't want the **aside** elements to stretch all the way to the bottom, you can add a blank space using a dot: 
   ```css
        grid-template-areas: 
            "agArticle agAside1"
            "agArticle agAside2"
            "agArticle . ";
   ```

7. Here's what the layout looks like for each of these three examples: ![](assets/GridLayouts_390_1200.png)

8. With **CSS grid** you can make almost any layout you like. In this example the **header** and **footer** were left out of the design, but they could be included in the grid too. If you want to learn more about **CSS grid**, go to [dojo.soy/a-html-css-grid](TODO)
