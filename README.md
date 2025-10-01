# Ex04 Places Around Me
# Date: 01-10-2025
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
map.html
```
<html>
<head>
<title>My City</title>
</head>
<body>
<h1 align="center">
<font color="red"><b>saidapet</b></font>
</h1>
<h3 align="center">
<font color="blue"><b>kishore Kumar B(25007664)</b></font>
</h3>
<center>
{% load static %}

<img src="{% static 'map.jpg' %}" usemap="#image-map">


<map name="image-map">
    <area target="" alt="anna university" title="anna university" href="/p1/" coords="702,324,539,435" shape="rect">
    <area target="" alt="guindy" title="guindy" href="/p2/" coords="478,432,315,514" shape="rect">
    <area target="" alt="siadapet" title="siadapet" href="/p3/" coords="499,141,341,242" shape="rect">
    <area target="" alt="kasi theatre" title="kasi theatre" href="/p4/" coords="187,5,0,109" shape="rect">
    <area target="" alt="tech park" title="tech park" href="/p5/" coords="194,290,13,403" shape="rect">

</map>
</center>
</body>
</html>

```
p1.html
```
<html>
<head>
  <title>My Home Town</title>
</head>
<body bgcolor="lightblue">

  <h1 align="center">
    <font color="darkgreen"><b>Chennai</b></font>
  </h1>

  <h3 align="center">
    <font color="blue"><b>Anna University - Centre of Excellence</b></font>
  </h3>

  <hr size="3" color="green">

  <p align="justify">
    <font face="Georgia" size="5">
      Anna University is one of the most prestigious universities in India, located in Guindy, Chennai. 
      Established in 1978, it is renowned for its engineering, technology, and research programs. 
      The campus is spread over 185 acres and is home to historic buildings, laboratories, libraries, 
      and modern facilities. Anna University also affiliates hundreds of engineering colleges across 
      Tamil Nadu. With its strong academic reputation and vibrant student community, it continues 
      to be a hub for innovation and higher learning.
    </font>
  </p>

</body>
</html>

```
p2.html
```
<html>
<head>
  <title>My Home Town</title>
</head>
<body bgcolor="lightgreen">

  <h1 align="center">
    <font color="darkgreen"><b>Chennai</b></font>
  </h1>

  <h3 align="center">
    <font color="blue"><b>Guindy National Park - Urban Nature Reserve</b></font>
  </h3>

  <hr size="3" color="brown">

  <p align="justify">
    <font face="Georgia" size="5">
      Guindy National Park is one of the smallest national parks in India, located in the heart of 
      Chennai city. Spanning about 2.7 km², it is home to <b>blackbuck, spotted deer, jackals</b>, and 
      over 100 species of birds. The park preserves the tropical dry evergreen forest and provides a 
      peaceful escape from the busy city life. It also has a <b>children's park</b> and a <b>snake park</b>, 
      making it a popular spot for families and nature lovers.
    </font>
  </p>

</body>
</html>
```
p3.html
```
<html>
<head>
  <title>My Home Town</title>
</head>
<body bgcolor="lightpink">

  <h1 align="center">
    <font color="darkred"><b>Chennai</b></font>
  </h1>

  <h3 align="center">
    <font color="blue"><b>Saidapet - My Hometown</b></font>
  </h3>

  <hr size="3" color="red">

  <p align="justify">
    <font face="Georgia" size="5">
      Saidapet is one of the oldest and most vibrant localities in Chennai, 
      situated on the banks of the Adyar River. It is well known for the 
      historic <b>Karaneeswarar Temple</b> and bustling markets. 
      Saidapet also serves as a major connecting point between southern 
      suburbs and the central parts of Chennai through its railway station, 
      bus terminus, and metro connectivity. With its blend of tradition and 
      modern life, Saidapet is a place full of culture, heritage, and community spirit.
    </font>
  </p>

</body>
</html>

```

p4.html
```
<html>
<head>
  <title>Kasi Theatre</title>
</head>
<body bgcolor="lightyellow">

  <h1 align="center">
    <font color="darkgreen"><b>Chennai</b></font>
  </h1>

  <h3 align="center">
    <font color="brown"><b>Kasi Theatre</b></font>
  </h3>

  <hr size="3" color="green">

  <p align="justify">
    <font face="Georgia" size="5">
      Kasi Theatre is one of the most popular and iconic cinema theatres in Chennai, 
      located in Ashok Nagar. It is a favorite destination for movie lovers, known for 
      its lively atmosphere and energetic crowds. With its large screens and modern 
      digital facilities, Kasi Theatre has been entertaining audiences for decades. 
      More than just a theatre, it stands as a landmark of Chennai’s vibrant 
      cinema culture.
    </font>
  </p>

</body>
</html>


```


p5.html
```
<html>
<head>
  <title>My Home Town</title>
</head>
<body bgcolor="lightyellow">

  <h1 align="center">
    <font color="darkred"><b>Chennai</b></font>
  </h1>

  <h3 align="center">
    <font color="blue"><b>Tamarai Tech Park - IT Hub</b></font>
  </h3>

  <hr size="3" color="red">

  <p align="justify">
    <font face="Georgia" size="5">
      Tamarai Tech Park is one of the well-known IT parks in Chennai, located in Guindy. 
      It is home to several multinational companies and technology firms. 
      The campus is designed with modern infrastructure, spacious offices, and essential 
      facilities to support IT and business operations. Its location provides easy access 
      to transport, making it a convenient workplace for professionals. Tamarai Tech Park 
      contributes significantly to the city's reputation as a growing IT and business hub.
    </font>
  </p>

</body>
</html>
```
views.py
```

from django.http import HttpResponse
from django.shortcuts import render

def index(request):
    return render(request, "map.html")

def place1(request):
    return render(request,'p1.html')

def place2(request):
    return render(request,'p2.html')
    

def place3(request):
    return render(request,'p3.html' )

def place4(request):
    return render(request,'p4.html')

def place5(request):
    return render(request,'p5.html')

```

# OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4f02b74e-871e-40e9-83d2-afd82a92b4ca" />
<img width="1920" height="1129" alt="image" src="https://github.com/user-attachments/assets/47f527d8-caec-4816-8219-7bdbab446672" />
<img width="1920" height="1098" alt="image" src="https://github.com/user-attachments/assets/92fbc806-53bf-43aa-b8f2-84634c415e85" />
<img width="1920" height="1104" alt="image" src="https://github.com/user-attachments/assets/97704a9a-f3e5-4f99-adb3-2f87f0de5d59" />
<img width="1923" height="1110" alt="image" src="https://github.com/user-attachments/assets/7e39361c-211a-4509-9ba2-f264ae6170de" />





# RESULT
The program for implementing image maps using HTML is executed successfully.
