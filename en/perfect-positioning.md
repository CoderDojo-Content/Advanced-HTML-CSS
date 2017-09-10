1. Add a `div` to your page and put a couple of images in it. Give the `div` and the `img` elements `id` values. I'm also adding a CSS **class** to give the photos all a border.
    ```html
        
      <div id="photoBox">
        <img id="imgHorse" class="photo" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="photo" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
      </div>
    ```
    You will use CSS to position the photos exactly and make a photo collage.
2. In your CSS file, add separate style rules for each of the elements using **id selectors**.
    ```css
        #photoBox {
            width: 800px;
            height: 400px;
        }
        #imgHorse {
            width: 120px;
        }
        #imgTeaCat {
            width: 250px;
        }
        .photo {
            border: 1px solid white;
        }
    ```

3. The photos appear one after the other in the order they appear in your code. To choose exact positions, you do two things. First, add the property `position: absolute;` to each photo's CSS rules. Second, add the property `position: relative;` to the CSS rules for the container they are in. This makes it be the **parent** of the images so the positions are in relation to it.
2. the code
    ```css

        #imgHorse {
            width: 120px;
            top: 200px;
            left: 390px;
            position: absolute;
            z-index: 10;
        }
        #imgTeaCat {
            width: 250px;
            top: 210px;
            left: 160px;
            position: absolute;
            z-index: 7;
        }
    ```