1. With CSS you can make a bunch of little preview cards that give an _overview_ or summary of stuff that's on your website. I'm going to do some highlights of the tourist attractions in Ireland. You can change it to whatever you like. You could use this technique to make a portfolio page showing off all your projects that you've done! Add the following HTML code to your web page:
    ```html
        <article class="thumbnail ">
            <img src="monkey-2223271_640.jpg" class="smallPics">
            <h4>Fota Wildlife Park</h4>
            <p><span class="locationText">Location:</span> Fota Island, County Cork</p>
		</article>
  	```

2. Here's the CSS code for the classes `thumbnail` and `smallPics` as well as for the heading `h3`:
    ```css
        h3 {
            font-family: "League Gothic", sans-serif;
            font-style: normal;
            font-weight: 400;
        }
        .smallPics {
            height: 60px;
            border-radius: 10px;
        }
        .thumbnail {
            width: 200px;
            height: 200px;
            border: 2px solid lightblue;
            box-sizing: border-box;
            margin-top: 10px;
            font-family: "Lato", sans-serif;
        }
    ```
    The font-families **League Gothic** and **Lato** are used a lot in CoderDojo materials!

3. Do you see the extra element in there, `<span> </span>`? This is a handy tag you can use just for setting CSS styles, for example _part_ of the text in a paragraph. Here's the CSS code for the `locationText` class:
    ```css
        .locationText {
            color: darkblue;
        }
    ```

3. You should have something that looks like this now: Let's turn the whole thing into a link so people can click to see more information.

4. Place the whole `article` element inside a link element. Make sure the closing `</a>` tag is after the closing `</article>` tag! 
    ```html
        <a href="attractions.html#scFota">  
            <article class="thumbnail ">
                <img src="monkey-2223271_640.jpg" class="smallPics">
                <h3>Fota Wildlife Park</h3>
                <p><span class="locationText">Location:</span> Fota Island, County Cork</p>
            </article>
        </a>
    ```
    
5. Notice how the value of `href` in my link ends in `#scFota`? This is a neat trick you can use to jump to a particular part of a page. First you type the URL of the page to link to, followed by `#`. In the code file for the page you are linking to, find the part you want to jump to and give that element an `id`, for example, `<section id="scFota"`. The value of the `id` is what you type after the `#` in your link.

6. Now all the text has gone funny because it's a link. You can fix it by adding a class to the link, `class="thumbnailLink"`. Here's some CSS you could use
    ```css
        .thumbnailLink {
            color: inherit;
            text-decoration: none;
        }
    ```
    Setting the value of any property to `inherit` makes it use the value of the parent element, so in this case the text colour will match the rest of the text on the homepage.

7. Let's add a little animation when you hover over the card! With the `transform` property you can move something up or down with `translateY` and left or right with `translateX`. Add the following CSS code. Try out different values in the traslate function!
    ```css
        .thumbnail:hover {
            box-shadow: 0px 2px 2px rgba(0,0,0,0.2); 
            transform: translateY(-2px);
        }
    ```
    Play about with different pixel values in the `box-shadow` to see what they do. 
     * `rgba(0,0,0,0.2)` is another way of defining a colour. It's got the usual three numbers for Red, Green and Blue. The fourth number, called the **alpha** value, sets how see-through something is; it is a number between `0` and `1`.

8. Finally, add the following property to the `.thumbnail` class: `transition: all 0.2s ease-out;` This makes the movements smooth and last for `0.2` seconds.