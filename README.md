
# Tea Station Website

This website is used to advertise a specific product or brand. 

## 🛠 Frontend 

* JavaScript
* HTML 
* CSS
* SCSS
* DOM Manipulation

# Project Screenshots

![hero_section](https://github.com/zaidaslam99/Tea_Station_Project/blob/main/project_screenshots/hero_section.png?raw=true)

![about_section](https://github.com/zaidaslam99/Tea_Station_Project/blob/main/project_screenshots/about_section.png?raw=true)

![product_section](https://github.com/zaidaslam99/Tea_Station_Project/blob/main/project_screenshots/product_section.png?raw=true)

![services_section](https://github.com/zaidaslam99/Tea_Station_Project/blob/main/project_screenshots/services_section.png?raw=true)

![contact_us_&_footer_section](https://github.com/zaidaslam99/Tea_Station_Project/blob/main/project_screenshots/contact_footer_section.png?raw=true)


## Lessons Learned

### HTML Portion

There were important concepts that I learned one of the biggest being implementations of frontend design. For this project, I started off with different sections and each section had its own component for instance check the product section down below. 

```html
<!-- products -->
<section class="products">
<div class="section-center clearfix">
<!-- products info -->
<article class="products-info">
    <!-- section title -->
    <div class="section-title">
    <h3>check out</h3>
    <h2>our products</h2>
    </div>
    <!-- end of section title -->
    <p class="product-text">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi
    quidem, repellat praesentium esse ducimus odit alias nulla laborum
    doloremque voluptatum, a cum magnam iure accusamus.
    </p>
    <a href="products.html" class="btn">inventory</a>
</article>
<!-- products inventory -->
<article class="products-inventory clearfix">
    <!-- single product -->
    <div class="product">
    <img
        src="./images/product-1.jpeg"
        alt="single product"
        class="product-img"
    />
    <h4 class="product-title">ginger peach tea</h4>
    <h4 class="product-price">$6.99</h4>
    </div>
    <!-- end of single product -->
    <!-- single product -->
    <div class="product">
    <img
        src="./images/product-2.jpeg"
        alt="single product"
        class="product-img"
    />
    <h4 class="product-title">fruit sangria</h4>
    <h4 class="product-price">$6.99</h4>
    </div>
    <!-- end of single product -->
    <!-- single product -->
    <div class="product">
    <img
        src="./images/product-3.jpeg"
        alt="single product"
        class="product-img"
    />
    <h4 class="product-title">white tea</h4>
    <h4 class="product-price">$6.99</h4>
    </div>
    <!-- end of single product -->
</article>
</div>
</section>
```
As you can tell we have declared a section tag and within it, we have two different article tags which are both within a div tag. This format ultimately dictates what you see on the screen. Within each article, we have div tags that are used, so we can call our CSS to style them. The best way to describe what is going on is to imagine a square within a square within a square. This overall is the core concept design when it comes to the HTML part of this code. Each of the sections that we are working with is going to be replicating this simple concept. However, depending on the sections our article tag ratios to content will fluctuate. 

### CSS Portion

As for the CSS portion, it's convenient to declare root variables which are later used for the purpose of styling different tags; this will help us reduce redundancy. Let's take a look at the product section and see how this is being applied, something else that we are going to cover is the use of media queries as well. 

```css
/*
=============== 
Products
===============
*/
.products {
  background: var(--clr-grey-10);
}

.products article {
  padding: 2rem 0;
}

.product-text {
  color: var(--clr-grey-5);
  max-width: 26rem;
}

.product {
  margin-bottom: 2rem;
}

.product-img {
  border-radius: var(--radius);
  margin-bottom: 2rem;
  height: 17rem;
  object-fit: cover;
}

.product-price {
  color: var(--clr-primary);
}

@media screen and (min-width: 768px) {
  .product {
    float: left;
    width: 50%;
    padding-right: 2rem;
  }
}
@media screen and (min-width: 992px) {
  .product {
    width: 33.3%;
  }
}
@media screen and (min-width: 1200px) {
  .products-info {
    float: left;
    width: 30%;
  }
  .products-inventory {
    float: left;
    width: 70%;
  }
  .product {
    margin-bottom: 0;
    padding: 0 1rem;
  }
}
```
So first and foremost it's important to understand that all we are doing is styling each tag to its respected position. Notice how the use of @media is being applied, what this does is that we specify the given parameters within the @media so when the screen changes to a set amount of pixels those changes listed will be applied. 

### JavaScript Section

So when it comes to the JavaScript portion it's simple to understand, we are using DOM manipulation and accessing elements by their Id. We then store them in a variable and add an event listener to them. 

```javascript
// setup date
const date = (document.getElementById("date").innerHTML =
new Date().getFullYear());
// setup nav
const navBtn = document.getElementById("nav-btn");
const navbar = document.getElementById("navbar");
const navClose = document.getElementById("nav-close");
// show nav
navBtn.addEventListener("click", () => {
navbar.classList.add("showNav");
});
// close nav
navClose.addEventListener("click", () => {
navbar.classList.remove("showNav");
});
```

