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
   
6. Another useful element is `aside`. You use it when you have extra stuff that doesn't really belong with the main information on a page. For example, the Attractions page on my website is a list of places to visit. I want to add some notes about how to get around. That information doesn't really belong in the `article` element with all the attractions.

7. Outside of the `article` element, add a pair of `<aside> <\aside>` tags containing your extra stuff. You can use sections and other elements as you like.
   ```html  
      <aside>
       <section>
          <h2>Getting around</h2>
          <h3>Train</h3>
          <p>You can get to most of the major towns by train from Dublin.</p>
          <h3>Bus</h3>
          <p>There are many bus and coach services offering tours to popular locations and tourist attractions.</p>
          <h3>Car</h3>
          <p>The easiest way to get around outside of the cities is probably by car. Many remote areas do not have regular public transport services.</p>
       </section>
       <section>
          <h2>Weather</h2>
          <p>The weather in Ireland is very unpredictable! Even on a beautiful day you could get unexpectedly rained on.</p>
          <p>It's best to be prepared for any kind of weather if you are going outside.</p>
       </section>
      </aside>
   ```
   
8. Use the `aside` **selector** to define CSS styles for this new element to make it stand out from the other stuff on your page.
   ```css
      aside {
        background-color: #ccddff;
        padding: 1em;
        border-style: solid;
        border-width: 2px;
        border-color: Purple;
        color: #5c00e6;
      }
      aside section {
        border-style: none;
      }
   ```   

   