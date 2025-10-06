# Ex.08 Design of Interactive Image Gallery
## Date: 6/10/25

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<html>
<head>
    <title>Interactive Image Gallery</title>
<style>
        	.gallery-container 
{
            position: relative;
            max-width: 600px;
            margin: auto;
            background:linear-gradient(120deg,white,pink);
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        	}
        	.gallery-image 
{
            width: 100%;
            height: 400px;
            object-fit:fill;
            border-radius: 10px;
        	}
        	.caption 
{           
            margin-top: 10px;
            font-size: 18px;
            text-align:center;
        	}
        	.gallery-buttons 
{
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
        	}
        	button 
{
            padding: 10px 20px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #021122ff;
            color: white;
            transition: 0.3s;
        	}
            body{
                background:linear-gradient(300deg,pink,white)
            }
    	</style>
</head>
<body>
    	<div class="gallery-container">
        		<img id="galleryImage" class="gallery-image" src="{% static '1.png' %}">
        		<div id="caption" class="caption">Image 1</div>
        		<div class="gallery-buttons">
            		<button onclick="prevImage()">Previous</button>
            		<button onclick="nextImage()">Next</button>
        		</div>
    	</div>

    	<script>
        		const images = [
{ src: 'leaf.jpg' , caption: "Image 1" },
{ src: 'download.jpg', caption: "Image 2" },
{ src: 'levi.jpg' , caption: "Image 3" },
{ src:  'm.jpg', caption: "Image 4" },
{ src: 'nice.jpg', caption: "Image 5" },
];
let Index = 0;
        
function updateGallery( ) 
{
document.getElementById("galleryImage").src = images[Index].src;
document.getElementById("caption").textContent = images[Index].caption;
}

function nextImage( ) 
{
Index = (Index + 1) % images.length;
updateGallery( );
}

function prevImage( ) 
{
Index = (Index - 1 + images.length) % images.length;
updateGallery( );
}

</script>
</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2025-10-06 222932.png>)
![alt text](<Screenshot 2025-10-06 222954.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
