# Ex02 Commercial Website
## Date:

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NH Fashion</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>NH Fashion</h1>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#products">Shop</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#" id="cart-btn">🛒 Cart (<span id="cart-count">0</span>)</a></li>
        </ul>
    </nav>
</header>

<section class="hero">
    <h2>Luxury Accessories Collection</h2>
    <p>Chains • Earrings • Rings </p>
    <button onclick="scrollToProducts()">Shop Now</button>
</section>

<section class="products" id="products">
    <h2>Our Collection</h2>

    <div class="product-container">

        <div class="card">
            <img src="https://images.unsplash.com/photo-1603561596112-0a132b757442" alt="Chain">
            <h3>RING</h3>
            <p>₹999</p>
            <button onclick="addToCart()">Add to Cart</button>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1617038220319-276d3cfab638" alt="Earrings">
            <h3>Earrings</h3>
            <p>₹499</p>
            <button onclick="addToCart()">Add to Cart</button>
        </div>

        

        <div class="card">
            <img src="https://images.unsplash.com/photo-1611652022419-a9419f74343d" alt="Bangles">
            <h3>Chain</h3>
            <p>₹799</p>
            <button onclick="addToCart()">Add to Cart</button>
        </div>

    </div>
</section>

<!-- Contact Section -->
<section class="contact">
    <h2>Contact Us</h2>
    <p>We’d love to hear from you! Reach out for orders or queries.</p>

    <div class="contact-container">

        <div class="contact-info">
            <h3>NH Fashion</h3>
            <p>📍 Chennai, Tamil Nadu</p>
            <p>📞 +91 98765 43210</p>
            <p>📧 nhfashion@email.com</p>
        </div>

        <form class="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>

    </div>
</section>

<footer>
    <p>© 2026 NH Fashion</p>
</footer>

<script>
let cartCount = 0;

function addToCart() {
    cartCount++;
    document.getElementById("cart-count").innerText = cartCount;
}

function scrollToProducts() {
    document.getElementById("products").scrollIntoView({ behavior: "smooth" });
}
</script>

</body>
</html>
```
## style.css

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background: #fafafa;
}

/* Header */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #000;
    color: white;
    padding: 15px 30px;
}

header h1 {
    color: gold;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 20px;
}

nav a {
    color: white;
    text-decoration: none;
    transition: 0.3s;
}

nav a:hover {
    color: gold;
}

/* Hero */
.hero {
    height: 90vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
                url('https://images.unsplash.com/photo-1519741497674-611481863552');
    background-size: cover;
    background-position: center;
    color: white;
    text-align: center;
    animation: fadeIn 2s ease-in;
}

.hero h2 {
    font-size: 3rem;
}

.hero button {
    margin-top: 20px;
    padding: 12px 25px;
    border: none;
    background: gold;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
}

.hero button:hover {
    transform: scale(1.1);
}

/* Products */
.products {
    padding: 50px 20px;
    text-align: center;
}

.product-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 25px;
    margin-top: 30px;
}

.card {
    width: 250px;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    transition: 0.3s;
    animation: fadeUp 1s ease;
}

.card:hover {
    transform: translateY(-10px);
}

.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card h3 {
    margin: 10px 0;
}

.card p {
    color: #555;
}

.card button {
    margin: 10px;
    padding: 10px;
    border: none;
    background: black;
    color: white;
    cursor: pointer;
    transition: 0.3s;
}

.card button:hover {
    background: gold;
    color: black;
}

/* Footer */
footer {
    background: #000;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 30px;
}

/* Animations */
@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}

@keyframes fadeUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Responsive */
@media (max-width: 768px) {
    .hero h2 {
        font-size: 2rem;
    }

    nav ul {
        flex-direction: column;
        gap: 10px;
    }

    header {
        flex-direction: column;
    }
}

@media (max-width: 480px) {
    .card {
        width: 90%;
    }
}

/* Contact Section */
.contact {
    padding: 50px 20px;
    background: #f4f4f4;
    text-align: center;
}

.contact h2 {
    margin-bottom: 10px;
}

.contact-container {
    display: flex;
    justify-content: center;
    align-items: flex-start;
    gap: 40px;
    margin-top: 30px;
    flex-wrap: wrap;
}

/* Contact Info */
.contact-info {
    max-width: 300px;
    text-align: left;
}

.contact-info h3 {
    color: gold;
    margin-bottom: 10px;
}

/* Contact Form */
.contact-form {
    display: flex;
    flex-direction: column;
    width: 300px;
}

.contact-form input,
.contact-form textarea {
    margin-bottom: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    outline: none;
}

.contact-form textarea {
    height: 100px;
    resize: none;
}

.contact-form button {
    padding: 10px;
    border: none;
    background: black;
    color: white;
    cursor: pointer;
    transition: 0.3s;
}

.contact-form button:hover {
    background: gold;
    color: black;
}
```




## OUTPUT

<img width="1865" height="885" alt="Screenshot 2026-05-07 134559" src="https://github.com/user-attachments/assets/b52d2703-61e1-4439-9bf9-99366da25582" />


<img width="1868" height="885" alt="image" src="https://github.com/user-attachments/assets/d467b9a1-6415-4f0a-a2d4-ba6f04ac2857" />

<img width="1890" height="694" alt="image" src="https://github.com/user-attachments/assets/448bd356-da3e-4993-84f3-3699383765fc" />

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
