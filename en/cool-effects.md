1. Let's add a little animation when you hover over the cards you made earlier! With the `transform` property you can move something up or down with `translateY` and left or right with `translateX`. Add the following CSS code. Try out different values in the traslate function!
    ```css
        .card:hover {
            box-shadow: 0px 2px 2px rgba(0,0,0,0.2); 
            transform: translateY(-2px);
        }
    ```
    Play about with different pixel values in the `box-shadow` property to see what they do. 
     
2. `rgba(0,0,0,0.2)` is another way of defining a colour. It's got the usual three numbers \(from 0 up to 255\) for Red, Green and Blue. The fourth number, called the **alpha** value, sets how see-through something is; it is a number between `0` and `1`.

2. Finally, make the animation smooth by adding the following property to the `.card` class from earlier: `transition: all 0.2s ease-out;` A duration of _0.2s_ means the animation lasts for 0.2 seconds.

3. Another effect you've probably seen on loads of websites is **lightbox**, where you click on something and the screen dims while something else, like a bigger picture or a popup box, appears in front of everything. To get this effect you will make two links.

4. The first link is for the actual **lightbox**. It contains all the stuff that will appear when you click. Make sure you give the link itself an `id`.
    ```html
        <a href="#_" class="lightbox" id="boxLemur">
           <h3>Lemur!!</h3>
           <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" class="bigPics"/>
           <p>A lemur enjoying a little snack</p>
         </a>
    ```
    You can put anything you like in between the link tags. I've got a picture, a heading and some text. Maybe you just want a picture and no text.

4. The other link is of course the thing that you click to make the lightbox appear. Simply add a pair of `a` tags around the element, in this case a small picture of a lemur. The **target** of the link will be the lightbox, which you set using the `id`. You might recognise this technique from earlier!
    ```html
        <a href="#boxLemur">
            <img src="monkey-2223271_640.jpg" class="smallPics">
        </a>
    ```

5. Here's the CSS for the lightbox. Can you work out what most of it does?
    ```css
        .lightbox{
            background: rgba(0,0,0,0.8);
            color: #ffffff;
            text-align: center;
            text-decoration: none;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            position: fixed;
            visibility: hidden;
            z-index: 999;
        }
        .lightbox:target {
            visibility: visible;
        }
    ```
    Setting the `position` property to `fixed` means it stays put when you scroll. The `:target` pseudo-class only applies when the lightbox was the target of the last link clicked. So when you click anywhere the `visibility` will be set back to hidden.

6. You can add as many lightboxes as you want to a page. They can all use the same CSS class. Just make sure each one has a different `id`! For each one, you need to make something on your webpage into a link that you can click to make the lightbox appear, and you use the `id` as the `href` value in that link; just you've done above!
