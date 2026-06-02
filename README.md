# Ex.06 Restuarant Website
## Date:

## AIM:
To develop a static Resturant website to display the menu and services provided by the resturant.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
home 

```
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>KERALA CAFE</title>
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>

<nav>
    <h2>KERALA CAFE</h2>
    <a href="/">Home</a>
    <a href="/menu/">Menu</a>
    <a href="/administration/">Administration</a>
    <a href="/contact/">Contact</a>
</nav>

<section class="hero">
    {% load static %}
    <img src="{% static 'images/image.png' %}" width="100%" height="400">
    <h1>Welcome to Kerala Cafe</h1>
    <p>Delicious food served with love and homely taste.</p>
    <a href="/menu/" class="btn">View Menu</a>
</section>

<section class="about">
    <h2>About Us</h2>
    <p>
        Kerala Cafe is a premium restaurant serving authentic and delicious kerala food
    </p>
</section>

<footer>
    <p>Created by Nanditha Shaji</p>
</footer>

</body>
</html>

```

menu 
```
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>Menu - Kerala Cafe</title>
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>

<nav>
    <h2>Kerala Cafe</h2>
    <a href="/">Home</a>
    <a href="/menu/">Menu</a>
    <a href="/administration/">Administration</a>
    <a href="/contact/">Contact</a>
</nav>

<h1 class="title">Our Special Menu</h1>

<div class="menu-container">

    <div class="card">
        {% load static %}
<img src="{% static 'images/image copy.png' %}" width="200" height="150">
        <h2>biriyani</h2>
        <p>Price: ₹250</p>
    </div>

    <div class="card">
           {% load static %}
<img src="{% static 'images/image copy 2.png' %}" width="200" height="150">
        <h2>porotta</h2>
        <p>Price: ₹100</p>
    </div>

    <div class="card">
          {% load static %}
<img src="{% static 'images/a.png' %}" width="200" height="150">
        <h2>chicken curry</h2>
        <p>Price: ₹120</p>
    </div>

    <div class="card">
         {% load static %}
<img src="{% static 'images/image copy 3.png' %}" width="200" height="150">
        <h2>chicken fry</h2>
        <p>Price: ₹150</p>
    </div>

   

</div>

<footer>
    <p>Created by Nanditha Shaji</p>
</footer>

</body>
</html>
```
administration
```
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>Administration - Kerala Cafe</title>
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>

<nav>
    <h2>Kerala Cafe</h2>
    <a href="/">Home</a>
    <a href="/menu/">Menu</a>
    <a href="/administration/">Administration</a>
    <a href="/contact/">Contact</a>
</nav>

<h1 class="title">Administration Team</h1>

<div class="admin-container">

    <div class="card">
        <h2>Restaurant Manager</h2>
        <p>Handles restaurant operations and customer service.</p>
    </div>

    <div class="card">
        {% load static %}
<img src="{% static 'images/b.png' %}" width="100%" height="400">
        <h2>Head Chef</h2>
        <p>Expert in preparing delicious dishes with quality taste.</p>
    </div>

    <div class="card">
        <h2>Service Team</h2>
        <p>Provides fast and friendly service to customers.</p>
    </div>

</div>

<footer>
    <p>Created by Nanditha Shaji</p>
</footer>

</body>
</html>
```
contact
```
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>Contact - Nanditha Shaji</title>
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>

<nav>
    <h2>Nanditha Shaji</h2>
    <a href="/">Home</a>
    <a href="/menu/">Menu</a>
    <a href="/administration/">Administration</a>
    <a href="/contact/">Contact</a>
</nav>

<h1 class="title">Contact Us</h1>

<div class="contact-box">

    <p><b>Address:</b> gp road, Tamil Nadu</p>

    <p><b>Phone:</b> +91 9940666777</p>

    <p><b>Email:</b> keralacafe@gmail.com</p>

    <p><b>Opening Hours:</b> 10:00 AM - 11:00 PM</p>

</div>

<footer>
    <p>Created by Nanditha Shaji</p>
</footer>

</body>
</html>
```
css
```
body{
    margin:0;
    font-family: Arial, sans-serif;
    background-color:#f4f4f4;
}

nav{
    background-color:#8B0000;
    padding:15px;
    text-align:center;
}

nav h2{
    color:white;
    display:inline;
    margin-right:30px;
}

nav a{
    color:white;
    text-decoration:none;
    margin:15px;
    font-size:18px;
}

nav a:hover{
    color:yellow;
}

.hero{
    text-align:center;
    padding:100px 20px;
    background-color:#ffcccb;
}

.hero h1{
    font-size:50px;
    color:#8B0000;
}

.hero p{
    font-size:22px;
}

.btn{
    background-color:#8B0000;
    color:white;
    padding:12px 25px;
    text-decoration:none;
    border-radius:5px;
}

.btn:hover{
    background-color:black;
}

.about{
    padding:40px;
    text-align:center;
}

.title{
    text-align:center;
    color:#8B0000;
    margin-top:30px;
}

.menu-container,
.admin-container{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:20px;
    padding:30px;
}

.card{
    background:white;
    width:250px;
    padding:20px;
    border-radius:10px;
    box-shadow:0px 0px 10px gray;
    text-align:center;
}

.card:hover{
    transform:scale(1.05);
    transition:0.3s;
}

.contact-box{
    width:50%;
    margin:auto;
    background:white;
    padding:30px;
    border-radius:10px;
    box-shadow:0px 0px 10px gray;
    margin-top:30px;
    text-align:center;
}

footer{
    background-color:#8B0000;
    color:white;
    text-align:center;
    padding:15px;
    margin-top:40px;
}
```



## OUTPUT:
<img width="1920" height="1080" alt="Screenshot 2026-05-26 143214" src="https://github.com/user-attachments/assets/7a5872ce-870a-4e7f-9b17-d02ff6d65c15" />
<img width="1920" height="1080" alt="Screenshot 2026-05-26 143227" src="https://github.com/user-attachments/assets/36b2db03-db83-40eb-961c-e7fb63fbd5ec" />
<img width="1920" height="1080" alt="Screenshot 2026-05-26 143239" src="https://github.com/user-attachments/assets/222b3b92-0cff-4356-8e77-55ef08fbe605" />
<img width="1920" height="1080" alt="Screenshot 2026-05-26 143250" src="https://github.com/user-attachments/assets/30812850-64a6-4025-92e8-7003b3944143" />




## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
