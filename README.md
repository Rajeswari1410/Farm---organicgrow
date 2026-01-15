if
# OrganicGrow – Organic Farming Guide Platform

## Description
OrganicGrow is a web-based platform to educate farmers about organic farming,
including crop-specific tips, natural fertilizers, and pest control methods.

index.html (Home Page)
<!DOCTYPE html>
<html>
<head>
    <title>OrganicGrow | Organic Farming Guide</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>OrganicGrow</h1>
    <p>Learn & Practice Organic Farming</p>
</header>

<nav>
    <a href="index.html">Home</a>
    <a href="crops.html">Crops</a>
    <a href="fertilizers.html">Organic Fertilizers</a>
    <a href="pest-control.html">Pest Control</a>
</nav>

<section class="hero">
    <h2>Grow Naturally, Farm Sustainably</h2>
    <p>100% Organic • Eco-Friendly • Healthy Crops</p>
</section>

<footer>
    <p>© 2026 OrganicGrow. All rights reserved.</p>
</footer>

</body>
</html>

crops.html (Crop Guide Page)
<!DOCTYPE html>
<html>
<head>
    <title>Crops | OrganicGrow</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Organic Crop Guide</h1>
</header>

<nav>
    <a href="index.html">Home</a>
    <a href="fertilizers.html">Organic Fertilizers</a>
</nav>

<section class="content">
    <h2>Rice</h2>
    <p>Use compost manure and green manure for healthy growth.</p>

    <h2>Vegetables</h2>
    <p>Apply vermicompost and natural pest control techniques.</p>

    <h2>Fruits</h2>
    <p>Maintain soil moisture and use neem-based sprays.</p>
</section>

</body>
</html>

fertilizers.html (Organic Fertilizers Page)
<!DOCTYPE html>
<html>
<head>
    <title>Organic Fertilizers | OrganicGrow</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Organic Fertilizers</h1>
</header>

<nav>
    <a href="index.html">Home</a>
    <a href="pest-control.html">Pest Control</a>
</nav>

<section class="content">
    <ul>
        <li>Compost manure</li>
        <li>Vermicompost</li>
        <li>Green manure</li>
        <li>Neem cake</li>
        <li>Bio fertilizers</li>
    </ul>
</section>

</body>
</html>

pest-control.html (Organic Pest Control Page)
<!DOCTYPE html>
<html>
<head>
    <title>Pest Control | OrganicGrow</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Natural Pest Control</h1>
</header>

<nav>
    <a href="index.html">Home</a>
    <a href="crops.html">Crops</a>
</nav>

<section class="content">
    <p>Use neem oil spray to control insects.</p>
    <p>Introduce beneficial insects like ladybugs.</p>
    <p>Use garlic-chili spray for pest management.</p>
</section>
if
</body>
</html>


html>
🎨 style.css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f3fff3;
}

header {
    background-color: #2f8f2f;
    color: white;
    padding: 20px;
    text-align: center;
}

nav {
    background-color: #4caf50;
    padding: 10px;
    text-align: center;
}

nav a {
    color: white;
    margin: 15px;
    text-decoration: none;
    font-weight: bold;
}

.hero, .content {
    padding: 40px;
    text-align: center;
}

ul {
    list-style-type: none;
}

footer {
    background-color: #2f8f2f;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}


app.py (Backend Code)
from flask import Flask, render_template

app = Flask(__name__)

# Home page
@app.route('/')
def home():
    return render_template('index.html')

# Crops page
@app.route('/crops')
def crops():
    return render_template('crops.html')

# Fertilizers page
@app.route('/fertilizers')
def fertilizers():
    return render_template('fertilizers.html')

# Pest control page
@app.route('/pest-control')
def pest_control():
    return render_template('pest-control.html')

if __name__ == "__main__":
    app.run(debug=True)


OrganicGrowApplication.java

package com.organicgrow;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class OrganicGrowApplication {

    public static void main(String[] args) {
        SpringApplication.run(OrganicGrowApplication.class, args);
    }

}


package com.organicgrow.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class PageController {

    @GetMapping("/")
    public String home() {
        return "index";   // renders index.html
    }

    @GetMapping("/crops")
    public String crops() {
        return "crops";   // renders crops.html
    }

    @GetMapping("/fertilizers")
    public String fertilizers() {
        return "fertilizers";  // renders fertilizers.html
    }

    @GetMapping("/pest-control")
    public String pestControl() {
        return "pest-control";  // renders pest-control.html
    }

}


package com.organicgrow.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class PageController {

    @GetMapping("/")
    public String home() {
        return "index";   // renders index.html
    }

    @GetMapping("/crops")
    public String crops() {
        return "crops";   // renders crops.html
    }

    @GetMapping("/fertilizers")
    public String fertilizers() {
        return "fertilizers";  // renders fertilizers.html
    }

    @GetMapping("/pest-control")
    public String pestControl() {
        return "pest-control";  // renders pest-control.html
    }

}



