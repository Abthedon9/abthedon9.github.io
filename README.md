<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shirts & Hoodies</title>
    <style>
        /* Reset some basic styles */
        body, h1, p {
            margin: 0;
            padding: 0;
        }

        /* Basic styles for the body */
        body {
            font-family: Arial, sans-serif;
            background-color: #000000; /* Black background for the body */
            color: #fff; /* White text for the body */
            line-height: 1.6;
            padding: 20px; /* Add padding around the entire body */
            margin: 0;
            padding-bottom: 50px; /* Add space at the bottom for the footer */
        }

        /* Header styles without image background */
        header {
            background-color: #9E1B32; /* Solid red background */
            color: #fff; /* Default text color for the header */
            text-align: center;
            padding: 40px 20px;
            margin-bottom: 20px;
            border-radius: 10px; /* Rounded corners for the header */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3); /* Subtle shadow for depth */
            position: relative;
            overflow: hidden;
        }

        header h1 {
            font-size: 3em; /* Increase font size for the title */
            margin-bottom: 10px;
            color: #ff3333; /* Red color for the title */
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4); /* Dark shadow effect */
            z-index: 1; /* Ensure text appears above the background */
        }

        header p {
            font-size: 1.2em;
            margin-bottom: 5px;
            color: #fff; /* White color for "by: Team Impact" text */
            z-index: 1; /* Ensure text appears above the background */
        }

        /* Content section with image and text */
        .content-container {
            display: flex;
            justify-content: space-between;
            padding: 20px;
            gap: 20px;
        }

        .side-image {
            width: 45%; /* The image takes up 45% of the page width */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        /* Image container for vertical layout */
        .vertical-images {
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
        }

        .vertical-images img {
            width: 80%; /* Make images smaller */
            max-width: 400px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        /* Tab styles */
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }

        .tabs button {
            background-color: #9E1B32; /* Dark red color */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            margin-right: 10px;
            border-radius: 5px; /* Rounded corners for buttons */
        }

        .tabs button:hover {
            background-color: #7C1C28; /* Darker red when hovered */
        }

        .tab-content {
            display: none;
            text-align: center;
        }

        .tab-content.active {
            display: block;
        }

        /* Price box styles */
        .price {
            margin-top: 10px;
            font-size: 18px;
            color: #5C6BC0;
        }

        /* Footer styles */
        footer {
            background-color: #000000;
            color: #fff;
            text-align: center;
            padding: 10px;
            width: 100%;
            position: relative; /* Change to relative */
            margin-top: 20px; /* Add space above footer */
        }

        /* Button styles */
        button {
            background-color: #9E1B32; /* Dark red color */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px; /* Rounded corners for buttons */
        }

        button:hover {
            background-color: #7C1C28; /* Darker red when hovered */
        }

        /* Positioning Order Button under Shirt & Hoodie buttons */
        .order-btn-container {
            text-align: center;
            margin-top: 20px; /* Space above the "Order" button */
            margin-bottom: 20px; /* Space below the "Order" button */
        }

        /* About Me and Contact Info styles */
        #order-info {
            display: none;
            position: absolute;
            top: 80px;
            right: 20px;
            background-color: #310000;
            padding: 20px;
            width: 250px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }

        /* Light fire effect at the bottom of the website */
        .fire-effect {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 150px;
            background: linear-gradient(180deg, rgba(255, 87, 34, 0.7), rgba(255, 193, 7, 0.7));
            box-shadow: 0 0 20px rgba(255, 87, 34, 0.6);
            transition: transform 0.2s ease-out;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            .content-container {
                flex-direction: column; /* Stack the sections vertically on small screens */
                align-items: center;
            }

            .side-image, .about-me {
                width: 80%; /* Both sections take up most of the page */
                margin-bottom: 20px;
            }

            nav ul {
                text-align: left;
            }

            nav ul li {
                display: block;
                margin: 10px 0;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>🆁🆃 🆂🅷🅸🆁🆃🆂 🅰🅽🅳 🅷🅾🅾🅳🅸🅴🆂</h1>
        <p>by: Team Impact</p>
    </header>

    <!-- Main Content Section -->
    <section id="home">
        <h2></h2>

        <!-- Tabs for Shirts and Hoodies -->
        <div class="tabs">
            <button onclick="showTab('shirts')">Shirts</button>
            <button onclick="showTab('hoodies')">Hoodies</button>
        </div>

        <!-- Order Button placed here -->
        <div class="order-btn-container">
            <button onclick="toggleOrderInfo()">Order</button>
        </div>

        <!-- Shirt Tab Content -->
        <div id="shirts" class="tab-content">
            <div class="vertical-images">
                <img src="blackshirtdiff.jpg" alt="Shirt 1">
                <div class="price">$15.00</div>

                <img src="hoodtpyeblack.webp" alt="Shirt 2">
                <div class="price">$15.00</div>

                <img src="hoodtype.webp" alt="Shirt 3">
                <div class="price">$15.00</div>

                <!-- Add more shirt images here -->
            </div>
        </div>

        <!-- Hoodie Tab Content -->
        <div id="hoodies" class="tab-content">
            <div class="vertical-images">
                <img src="blackhoodie.webp" alt="Hoodie 1">
                <div class="price">$20.00</div>

                <img src="that.jpg" alt="Hoodie 2">
                <div class="price">$20.00</div>

                <!-- Add more hoodie images here -->
            </div>
        </div>
    </section>

    <!-- Order Info (About Me and Contact) -->
    <div id="order-info">
        <h2></h2>
        <p>Owner: Kashif, Abdullah</p>
        <p>Best shirt and hoodie designs!</p>
        <p>Team: Abdullah, Abdullah(Chota), Mahad, and Zaid</p>

        <h2>Contact</h2>
        <p>Reaching out:</p>
        <p>abdullahhk120@gmail.com</p>
        <p>951-***-****</p>

        <p><a href="https://www.instagram.com/dontt_abdullah" target="_blank" style="color: white; text-decoration: none;">Follow me on Instagram</a></p>
    </div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; Shirts & Hoodies by Kashif, Abdullah</p>
    </footer>

    <!-- Fire Effect at the Bottom -->
    <div class="fire-effect"></div>

    <!-- JavaScript Section -->
    <script>
        function showAlert() {
            alert('lol buy something!');
        }

        // JavaScript to switch tabs
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

        // Initially show shirts
        showTab('shirts');

        // Function to toggle visibility of Order Info
        function toggleOrderInfo() {
            var orderInfo = document.getElementById('order-info');
            if (orderInfo.style.display === 'none' || orderInfo.style.display === '') {
                orderInfo.style.display = 'block';
            } else {
                orderInfo.style.display = 'none';
            }
        }

        // Fire Effect Scroll Animation
        window.addEventListener('scroll', function() {
            var fireEffect = document.querySelector('.fire-effect');
            var scrollPosition = window.scrollY;
            fireEffect.style.transform = 'translateY(' + scrollPosition * 0.2 + 'px)';
        });
    </script>

</body>
</html>

