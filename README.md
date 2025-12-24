# Project Responsive Web Design using Bootstrap
# Date:19-12-2025
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
views.py
from django.shortcuts import render

def project_view(request):
    return render(request, 'project.html')
```
```
urls.py
from django.contrib import admin
from django.urls import path
from app import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.project_view, name='project'),   
]
```
```
project.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Products | HealthPlus Pharmacy</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
        body {
            background: #f8fafc;
            font-family: 'Poppins', sans-serif;
        }

        .navbar {
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

        .product-hero {
            background: linear-gradient(135deg, #16a34a, #22c55e);
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .medicine-card {
            background: #ffffff;
            border-radius: 20px;
            overflow: hidden;
            position: relative;
            transition: all 0.35s ease;
            box-shadow: 0 10px 25px rgba(0,0,0,0.08);
        }

        .medicine-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .medicine-card img {
            width: 100%;
            height: 180px;
            object-fit: contain;
            padding: 15px;
        }

        .price-tag {
            position: absolute;
            top: 15px;
            right: 15px;
            background: #16a34a;
            color: white;
            padding: 6px 14px;
            border-radius: 50px;
            font-size: 13px;
        }

        .medicine-body {
            padding: 20px;
            text-align: center;
        }

        footer {
            background: #16a34a;
            color: white;
            text-align: center;
            padding: 15px;
        }
    </style>
</head>

<body>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-success">
    <div class="container">
        <a class="navbar-brand fw-bold" href="/">💊 HealthPlus</a>
        <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#menu">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="menu">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="/">Home</a></li>
                <li class="nav-item"><a class="nav-link active" href="/products/">Products</a></li>
                <li class="nav-item"><a class="nav-link" href="/about/">About</a></li>
                <li class="nav-item"><a class="nav-link" href="/contact/">Contact</a></li>
            </ul>
        </div>
    </div>
</nav>

<!-- Hero -->
<section class="product-hero">
    <h2>Healthcare Essentials</h2>
    <p>Safe • Reliable • Affordable</p>
</section>

<!-- Products -->
<section class="container py-5">
    <div class="row g-4">

        <!-- Card 1 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹30</span>
                <img src="{% static 'Screenshot 2025-12-24 101816.png' %}">
                <div class="medicine-body">
                    <h6>Tablets</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- Card 2 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹120</span>
                <img src="{% static 'Screenshot 2025-12-24 101943.png' %}">
                <div class="medicine-body">
                    <h6>Injections</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- Card 3 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹90</span>
                <img src="{% static 'Screenshot 2025-12-24 102018.png' %}">
                <div class="medicine-body">
                    <h6>Thermometer</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- Card 4 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹60</span>
                <img src="{% static 'Screenshot 2025-12-24 102126.png' %}">
                <div class="medicine-body">
                    <h6>Oxy-Meter</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- Card 5 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹250</span>
                <img src="{% static 'Screenshot 2025-12-24 102243.png' %}">
                <div class="medicine-body">
                    <h6>Bandages</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- Card 6 -->
        <div class="col-lg-4 col-md-6">
            <div class="medicine-card">
                <span class="price-tag">₹80</span>
                <img src="{% static 'Screenshot 2025-12-24 102305.png' %}">
                <div class="medicine-body">
                    <h6>ORS</h6>
                    <button class="btn btn-outline-success btn-sm w-100">Add to Cart</button>
                </div>
            </div>
        </div>

    </div>
</section>

<!-- Footer -->
<footer>
    © 2025 HealthPlus Pharmacy | Designed by Sree Ram
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
# OUTPUT:
![alt text](<../Screenshot 2025-12-24 110106.png>)
# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
