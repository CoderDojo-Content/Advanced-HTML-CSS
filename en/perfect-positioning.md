1. On this card you will use CSS to position HTML elements exactly and make a photo collage. ![](assets/photoCollageWithText.png)

2. Add a **div** to your page and put as many images in it as you like. Give the **div** and the **img** elements **id** values.
   ```html
      <div id="photoBox">
        <img id="imgHorse" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
      </div>
   ```
   The photos will appear one after the other on the web page, in the order they appear in your code.
   
3. In your CSS file, add separate style rules for each of the elements using **id selectors**. For each of the elements inside the container, add the property `position: absolute;`. This lets you choose exact positions for them. You will want to define those positions _relative to_ (i.e. _within_) the container, so you also need to add the property `position: relative;` to the container itself.
    ```css
        #photoBox {
            width: 800px;
            height: 400px;
            position: relative;
        }
        #imgHorse {
            width: 120px;
            position: absolute;
        }
        #imgTeaCat {
            width: 250px;
            position: absolute;
        }
    ```

4. Then, you choose the exact positions you want for each picture. There are four properties you can use: **left**, **right**, **top**, and **bottom**. They represent how far each of the edges should be from the parent's edge. Use either **top** or **bottom** for the vertical position and use either **left** or **right** for the horizontal position.

 This code places the cat picture _100 pixels_ from the top and _60 pixels_ in from the left.
    ```css
        #imgTeaCat {
            width: 250px;
            top: 100px;
            left: 60px;
            position: absolute;
        }
    ```
    * The position values can also be negative!

5. You can also decide how the pictures overlap, using the **z-index** property. The value can be any whole number. The picture with the _highest_ number ends up on _top_ of the pile!
    ```css
        #imgHorse {
            width: 120px;
            top: 20px;
            left: 10px;
            position: absolute;
            z-index: 10;
        }
        #imgTeaCat {
            width: 250px;
            top: 100px;
            left: 60px;
            position: absolute;
            z-index: 7;
        }
    ```

6. You can position any html elements in this way, not just images. Try creating your own collage of photos, perhaps with some text over the top! Use exact positioning together with different **z-index** values to get the overlap effect the way you want it.
