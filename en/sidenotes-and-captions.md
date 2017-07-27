1. Do you find that when you add a picture you also add some text that goes with it, a **caption**? Then you could make use of two elements designed just for that purpose: `figure` and `figcaption`!
2. Find an `img` element where you have text above or below that goes with the picture. I'm working with the Tito picture on index.html, but you can go with whatever is on your website.  

   ```html
      <img id="imgTito" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />  		
      <p>
        This is Tito. He will be your tourguide! As you can see, Tito loves CoderDojo.
      </p>
   ```
3. On the line above the code, add the tag `<figure>`. Place the closing tag `<\figure>` on a new line after the code.

4. Next, remove the `p` tags, or whatever tags you have around the text \(maybe it's a heading like `h2`?\) and put the text in between `<figcaption> <\figcaption>` tags instead. The whole thing should look something like this:
   ```html
      <figure>
         <img id="imgTito" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />  		
         <figcaption>
         This is Tito. He will be your tourguide! As you can see, Tito loves CoderDojo.
         </figcaption>
      </figure>
   ```
   * The `figcaption` element is your **caption**. It can go either above the `img` element or below it.

5. When you run your code, the picture and text might have changed position, to be centered on the page. Maybe you were happy with the original positioning of the elements and don't want this. Simply define CSS rules for the `figure` and set the margin properties to zero, or values that suit you. You can style both `figure` and `figcaption` as you would any other element, with background colour, borders, etc.
   ```css
      figure { 
          margin-top: 0px;
          margin-bottom: 0px;
          margin-left: 0px;
          margin-right: 0px;
      }
   ```
   * The `figure` element acts as a sort of **container** for your picture and its caption. As well as allowing you to treat them as one unit when defining styles, grouping them together logically helps to maintain a good structure to your website.
   