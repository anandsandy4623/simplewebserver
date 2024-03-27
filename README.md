# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SLIDERS</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
      .icon{
        color: #db53c0;
        font-size: 25px;
        padding:5px;
      }
      i:hover{
        color: rgba(30, 6, 246, 0.832);
      }
    </style>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
</head>
<body>
  <div class="row border border-3" >
    <div class="col-5" >
      <i class="bi bi-whatsapp icon hover"></i>
      <i class="bi bi-facebook icon hover"></i>
      <i class="bi bi-twitter icon hover"></i>
      <i class="bi bi-linkedin icon hover"></i>
      <i class="bi bi-instagram icon hover"></i>
      <i class="bi bi-youtube icon hover"></i>
    </div>
    <div class="col-4" >
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent" >
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item ">
                <a class="nav-link active" aria-current="page " href="#">WEB PROJECT</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">NARESH.R</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  DEPARTMENT
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" href="#">CSC DEPARTMENT</a></li>
                  <li><a class="dropdown-item" href="#">AIML DEPARTMENT</a></li>
                  <li><hr class="dropdown-divider"></li>
                  <li><a class="dropdown-item" href="#">ECE DEPARTMENT here</a></li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
    <div class="col-3" >
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
  <div style="display: flex;">
        <div style="width: 20%;">
            <div class="card" style="width: 18rem;">
                <a href="https://www.saveetha.ac.in"><img src="SEC L.jpg" class="card-img-top" alt="..."></a>
                <div class="card-body">
                  <h5 class="card-title">SAVEETHA ENGINEERING COLLEGE</h5>
                  <p class="card-text">
                    Approved by the All India Council for Technical Education (AICTE), a statutory body of the Government of India, and also by the Government of Tamil Nadu</p>
                </div>
                <ul class="list-group list-group-flush">
                  <li class="list-group-item"><a href="https://saveetha.ac.in/index.php/admissions/courses-offered">COURSES</a></li>
                  <li class="list-group-item"><a href="https://www.saveetha.ac.in/index.php/life-at-sec/student-life">LIFE AT SEC</a></li>
                  <li class="list-group-item"><a href="https://www.saveetha.ac.in/index.php/about/about-sec">ABOUT</a></li>
                  <li class="list-group-item"><a href="https://www.saveetha.ac.in/index.php/placements/overview">PLACEMENTS</a></li>
                </ul>
              </div></div>
        <div style="width: 80%;">
            <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-indicators">
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3" aria-label="Slide 4"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="4" aria-label="Slide 5"></button>
                </div>
                <div class="carousel-inner">
                  <div class="carousel-item active">
                    <img src="web 3.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="SEC 1.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="SEC 2.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item active">
                    <img src="SEC 3.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item active">
                    <img src="SEC 1.jpg" class="d-block w-100" alt="...">
                  </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                  <span class="carousel-control-next-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Next</span>
                </button>
              </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>

```
## OUTPUT:


## RESULT:
The program for implementing simple webserver is executed successfully.
