To add collapsible sections to a GitHub Flavoured Markdown file, when viewed on GitHub Pages, do the following:

<div>
    
<button type="button" class="collapsible">+ Add Javascript to Markdown</button>

<div class="content" style="display: none;" markdown="1">

## e.g. in README.md

**This should be placed at the bottom of the markdown document**

```javascript
<script type="text/javascript">

    function loadCSS(filename){ 

       var file = document.createElement("link");
       file.setAttribute("rel", "stylesheet");
       file.setAttribute("type", "text/css");
       file.setAttribute("href", filename);
       document.head.appendChild(file);
    }

    //just call a function to load your CSS
    //this path should be relative your HTML location
    loadCSS("collapse.css");

    var coll = document.getElementsByClassName("collapsible");
    var i;

    for (i = 0; i < coll.length; i++) {
      coll[i].addEventListener("click", function() {
        this.classList.toggle("active");
        var content = this.nextElementSibling;
        if (content.style.display === "block") {
          content.style.display = "none";
        } else {
          content.style.display = "block";
        }
      });
    }

</script>
```
</div>
</div>

<div>
    
<button type="button" class="collapsible">+ Add CSS in an External File</button>
    
<div class="content" style="display: none;" markdown="1">

## e.g. in collapse.css

```css
/* Style the button that is used to open and close the collapsible content */
.collapsible {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: 5px;
  text-align: left;
  outline: none;
  font-size: 24px;
}

/* Add a background color to the button if it is clicked on (add the .active class with JS), and when you move the mouse over it (hover) */
.active, .collapsible:hover {
  background-color: #ccc;
}

/* Style the collapsible content. Note: hidden by default */
.content {
  padding: 18px 18px 18px 18px;
  display: none;
  overflow: hidden;
  background-color: #f1f1f1;
  border: 2px solid #444;
  border-radius: 5px;
}

```
</div>
</div>

<div>
    
<button type="button" class="collapsible">+ Indicate Sections to be Collapsed</button>
    
<div class="content" style="display: none;" markdown="1">

## e.g. in README.md

**Note that the line spacing and left alignment of the &lt;div&gt; tags is important!**

```html
<div>
    
<button type="button" class="collapsible">+ Collapsible Section</button>
    
<div class="content" style="display: none;" markdown="1">

<!-- Content to be hidden goes here -->

</div>
</div>
```
</div>
</div>

<script type="text/javascript">

    function loadCSS(filename){ 

       var file = document.createElement("link");
       file.setAttribute("rel", "stylesheet");
       file.setAttribute("type", "text/css");
       file.setAttribute("href", filename);
       document.head.appendChild(file);
    }

    //just call a function to load your CSS
    //this path should be relative your HTML location
    loadCSS("collapse.css");

    var coll = document.getElementsByClassName("collapsible");
    var i;

    for (i = 0; i < coll.length; i++) {
      coll[i].addEventListener("click", function() {
        this.classList.toggle("active");
        var content = this.nextElementSibling;
        if (content.style.display === "block") {
          content.style.display = "none";
        } else {
          content.style.display = "block";
        }
      });
    }

</script>
