# EX01 Developing a Simple Webserver
## Date:27/04/2024
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
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GT</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        a{
            padding: 10px;
            text-decoration: none;
            color:white;
            font-family: arial;
            font-size: 18px;
        }
        a:hover{
            color: rgb(242, 44, 44);
        }   
    </style>
</head>
<body style="background-color:black;">
     <div style="display:flex">
        <div style="width: 20%"><img style="width: 70%" src="logo.webp"></div>
        <div style="width: 55%;padding-top: 13px    ">
            <a href="   ">Home</a>
            <a href="">About</a>
            <a href="">CARS</a>
            <a href="">RACE</a>
            <a href="">My List</a>
            <a href="">Browse by language</a>
        </div>  
        <div style="width: 20%;padding-top: 8px">
        <input style="width: 80%;height: 30px;background-image: url('search.jpeg');background-color: white; background-size: contain;background-repeat: no-repeat;padding-left: 40px;" type="text" placeholder="search" >
        </div>
     </div>
     
     <h1 style="color:white;text-align: center;font-style: italic;font-size: 50px;">TOP 10 ON CARS</h1>
     <div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="s3.jpeg" class="d-block w-100" alt="..." width="50%">
          </div>
          <div class="carousel-item">
            <img src="s1.jpeg" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s2.jpeg" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s4.jpg" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s5.webp" class="d-block w-100" alt="...">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
     <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>  
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=('',8000)
httpd=HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=('',8000)
httpd=HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()


```
## OUTPUT:
S.ANANTTHAVETHAN=212221043001
![Screenshot 2024-03-27 092553](https://github.com/anandsandy4623/simplewebserver/assets/135193077/b4b86084-0c39-4b91-ae53-c0d70b39f4fe)
![Screenshot 2024-03-27 093145](https://github.com/anandsandy4623/simplewebserver/assets/135193077/b1ada8a3-fbc0-4858-9959-8d98b0ce1579)



## RESULT:
The program for implementing simple webserver is executed successfully.
