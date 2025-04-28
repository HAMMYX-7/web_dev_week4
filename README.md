# web_dev_week4
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <!-- Main Content -->
    <div class="container">
        <header>
            <h1>Welcome to Our Website</h1>
        </header>

        <section class="main-content">
            <div class="content-box">
                <h2>Content Section 1</h2>
                <p>This is a sample content section.</p>
            </div>
            <div class="content-box">
                <h2>Content Section 2</h2>
                <p>This is another sample content section.</p>
            </div>
            <div class="content-box">
                <h2>Content Section 3</h2>
                <p>This is a third sample content section.</p>
            </div>
        </section>

        <footer>
            <p>© 2025 Your Company</p>
        </footer>
    </div>

</body>
</html>

/* Reset some default styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Basic styling */
body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    padding: 0;
    margin: 0;
    background-color: #f4f4f4;
}

/* Navigation bar */
nav {
    background-color: #333;
}

.nav-links {
    list-style-type: none;
    text-align: center;
    padding: 0;
}

.nav-links li {
    display: inline;
    margin-right: 20px;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-size: 18px;
}

.nav-links a:hover {
    color: #ff6347;
}

/* Main container using Flexbox */
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
}

/* Header */
header {
    text-align: center;
    margin-bottom: 20px;
}

/* Main content using Flexbox */
.main-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    width: 100%;
}

.content-box {
    background-color: #fff;
    padding: 20px;
    width: 30%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    border-radius: 5px;
}

/* Footer */
footer {
    text-align: center;
    margin-top: 40px;
    font-size: 14px;
    color: #777;
}

/* Media Queries for Responsiveness */

/* Tablet */
@media (max-width: 768px) {
    .main-content {
        flex-direction: column;
        align-items: center;
    }

    .content-box {
        width: 80%;
        margin-bottom: 20px;
    }
}

/* Mobile */
@media (max-width: 480px) {
    .nav-links {
        text-align: left;
        padding: 10px;
    }

    .nav-links li {
        display: block;
        margin-bottom: 10px;
    }

    .main-content {
        flex-direction: column;
    }

    .content-box {
        width: 90%;
    }
}
