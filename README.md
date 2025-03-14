<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shirts & Hoodies</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Reset some basic styles */
        body, h1, p {
            margin: 0;
            padding: 0;
        }

        /* Basic styles for the body */
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #000000;
            color: #fff;
            line-height: 1.6;
            padding: 20px;
            margin: 0;
            padding-bottom: 50px;
            position: relative;
            min-height: 100vh;
        }

        html {
            height: 100%;
        }

        /* Header styles */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 10;
            padding: 10px 20px;
            font-size: 1.5em;
            font-weight: 600;
            text-align: left;
        }

        header h1 {
            font-size: 1.5em;
            color: #ff3333;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
        }

        /* Hero Section */
        .hero {
            background: url('your-image.jpg') no-repeat center center/cover;
            height: 50vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            margin-top: 60px; /* Space for fixed header */
        }

        .hero-content h2 {
            font-size: 2em;
            margin-bottom: 10px;
        }

        .hero-content button {
            padding: 10px 20px;
            background-color: #9E1B32;
            color: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
        }

        .hero-content button:hover {
            background-color: #7C1C28;
        }

        /* Tabs and Content */
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
        }

        .tabs button {
            background-color: #9E1B32;
            color: white;
            padding: 15px 30px;
            border: none;
            cursor: pointer;
            font-size: 18px;
            margin-right: 15px;
            border-radius: 30px;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .tabs button:hover {
            background-color: #7C1C28;
            transform: scale(1.05);
        }

        .tab-content {
            display: none;
            text-align: center;
        }

        .tab-content.active {
            display: block;
        }

        .price {
            margin-top: 10px;
            font-size: 1.5em;
            color: #5C6BC0;
        }

        /* Product Cards */
        .product-card {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 250px; /* Increased width for larger shirts */
            margin: 15px;
            transition: transform 0.3s ease;
            border: 5px solid #000000; /* Outer border is black */
        }

        .product-card:hover {
            transform: scale(1.05);
        }

        .product-card img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 15px;
            cursor: pointer; /* Pointer cursor for clickable images */
        }

        .product-card button {
            padding: 10px;
            background-color: #ff3333; /* Add to Cart button is red */
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .product-card button:hover {
            background-color: #e60000; /* Slightly darker red on hover */
        }

        /* Lightbox Styles */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 100;
            justify-content: center;
            align-items: center;
        }

        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .close-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #ff3333;
            color: white;
            border: none;
            border-radius: 50%;
            padding: 10px;
            font-size: 18px;
            cursor: pointer;
        }

        /* Order Info Box */
        #order-info {
            display: none;
            position: fixed;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            background-color: #fff;
            color: #000;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            z-index: 20;
            width: 80%;
            max-width: 600px;
            text-align: center;
        }

        #order-info .social-icons a {
            margin: 0 15px;
            display: inline-block;
        }

        #order-info .social-icons img {
            width: 50px;
            height: 50px;
            margin-bottom: 10px;
        }

        /* Search Bar Styles */
        .search-bar {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: white;
            border: 2px solid #9E1B32;
            padding: 10px;
            border-radius: 30px;
            width: 250px;
            display: flex;
            align-items: center;
            z-index: 10;
        }

        .search-bar input {
            border: none;
            outline: none;
            padding: 8px 15px;
            width: 100%;
            border-radius: 30px;
            font-size: 16px;
        }

        .search-bar button {
            background-color: #9E1B32;
            color: white;
            padding: 8px 15px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 30px;
            margin-left: 10px;
        }

        .search-bar button:hover {
            background-color: #7C1C28;
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #9E1B32;
            color: white;
            border: none;
            border-radius: 50%;
            padding: 10px 15px;
            font-size: 20px;
            cursor: pointer;
        }

        .back-to-top:hover {
            background-color: #7C1C28;
        }

        /* Footer Section */
        footer {
            background-color: #000000;
            color: #fff;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .tabs button {
                font-size: 14px;
                padding: 12px 20px;
                margin-right: 10px;
            }

            .hero-content h2 {
                font-size: 1.5em;
            }

            .product-card {
                width: 90%;
                margin: 10px auto;
            }

            .search-bar {
                width: 200px;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>Styles</h1>
        <p>by: Team Impact</p>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h2>Discover Our Latest Styles</h2>
            <button onclick="window.location.href='#home'">Shop Now</button>
        </div>
    </section>

    <!-- Search Bar -->
    <div class="search-bar">
        <input type="text" placeholder="Search..." id="search-input">
        <button onclick="searchFunction()">Search</button>
    </div>

    <!-- Main Content Section -->
    <section id="home">
        <div class="tabs">
            <button onclick="showTab('shirts')" id="shirts-btn">Shirts</button>
            <button onclick="showTab('hoodies')" id="hoodies-btn">Hoodies</button>
            <button onclick="toggleOrderInfo()">Order</button>
        </div>

        <!-- Shirt Tab Content -->
        <div id="shirts" class="tab-content active">
            <div class="product-card">
                <img src="blackshirtdiff.jpg" alt="Shirt 1" onclick="openLightbox('blackshirtdiff.jpg')">
                <h3>Shirt 1</h3>
                <div class="price">$15.00</div>
                <button>Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="www.jpeg" alt="Shirt 2" onclick="openLightbox('www.jpeg')">
                <h3>Shirt 2</h3>
                <div class="price">$15.00</div>
                <button>Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="blackwebp.webp" alt="Shirt 3" onclick="openLightbox('blackwebp.webp')">
                <h3>Shirt 3</h3>
                <div class="price">$15.00</div>
                <button>Add to Cart</button>
            </div>
        </div>

        <!-- Hoodie Tab Content -->
        <div id="hoodies" class="tab-content">
            <div class="product-card">
                <img src="blackhoodie.webp" alt="Hoodie 1" onclick="openLightbox('blackhoodie.webp')">
                <h3>Hoodie 1</h3>
                <div class="price">$20.00</div>
                <button>Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="that.jpg" alt="Hoodie 2" onclick="openLightbox('that.jpg')">
                <h3>Hoodie 2</h3>
                <div class="price">$20.00</div>
                <button>Add to Cart</button>
            </div>
        </div>

        <!-- Testimonials Section -->
        <div class="testimonials">
            <h2>Full refund on what you don't like!</h2>
            <div class="testimonial-card">
                <p>"You will appreciate the time and effort we invest into our quality"</p>
                <p>- Abdullah, k</p>
            </div>
        </div>
    </section>

    <!-- Lightbox Overlay -->
    <div id="lightbox" class="lightbox" onclick="closeLightbox()">
        <img id="lightbox-img" src="" alt="Large Image">
        <button class="close-btn" onclick="closeLightbox()">X</button>
    </div>

    <!-- Order Info Section (Popup) -->
    <div id="order-info">
        <h2>Ordering</h2>
        <div class="social-icons">
            <a href="https://www.instagram.com/dontt_abdullah" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Instagram_icon.png/512px-Instagram_icon.png" alt="Instagram Logo">
            </a>
            <a href="https://twitter.com/dontt_abdullah" target="_blank">
                <img src="twitter.png" alt="Twitter Logo">
            </a>
            <a href="https://www.snapchat.com/add/mes_abthedon" target="_blank">
                <img src="snap.pg.avif" alt="Snapchat Logo">
            </a>
            <a href="sms:+1951****">
                <img src="message.jpeg" alt="Message Logo">
            </a>
        </div>
    </div>

    <!-- Back to Top Button -->
    <button class="back-to-top" onclick="window.scrollTo({ top: 0, behavior: 'smooth' })">↑</button>

    <!-- Footer Section -->
    <footer>
        <p>&copy; Shirts & Hoodies by Kashif, Abdullah</p>
    </footer>

    <script>
        function showTab(tabName) {
            var shirtsTab = document.getElementById('shirts');
            var hoodiesTab = document.getElementById('hoodies');
            if (tabName === 'shirts') {
                shirtsTab.classList.add('active');
                hoodiesTab.classList.remove('active');
            } else {
                hoodiesTab.classList.add('active');
                shirtsTab.classList.remove('active');
            }
        }

        function toggleOrderInfo() {
            var orderInfo = document.getElementById('order-info');
            if (orderInfo.style.display === 'none' || orderInfo.style.display === '') {
                orderInfo.style.display = 'block';
            } else {
                orderInfo.style.display = 'none';
            }
        }

        function searchFunction() {
            var input = document.getElementById('search-input').value.toLowerCase();
            if (input.includes('shirt')) {
                showTab('shirts');
            } else if (input.includes('hoodie')) {
                showTab('hoodies');
            } else {
                alert('No results found.');
            }
        }

        // Open the lightbox when an image is clicked
        function openLightbox(imageSrc) {
            var lightbox = document.getElementById('lightbox');
            var lightboxImg = document.getElementById('lightbox-img');
            lightbox.style.display = 'flex'; // Show the lightbox
            lightboxImg.src = imageSrc; // Set the clicked image in the lightbox
        }

        // Close the lightbox when the close button or overlay is clicked
        function closeLightbox() {
            var lightbox = document.getElementById('lightbox');
            lightbox.style.display = 'none'; // Hide the lightbox
        }
    </script>
</body>
</html>

