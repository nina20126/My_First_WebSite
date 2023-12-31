﻿# House of Horrors - My First WebSite

### Introduction

I have some background with earlier versions of HTML. I remember how all styles were written inside html tags, and how tables were coolest thing ever when creating layouts. Then there were iframes. Web design was so different back then. I used to create web sites just for fun, and mainly the subject for those web sites were horses. Then life went on, I got some other hobbies but every now and then I was memorizing how I used to enjoy my time with web sites. One day I just decided that I want to refresh my knowledge and I took part one of Open University courses (XAMK - Learn HTML & CSS) where anybody can participate. So I call this my first web site that is created with modern language using HTML5 and CSS3. No JavaScript or other technologies is used here.

### Welcome to House of Horrors!

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/cf1a7f09-c0f2-4e07-b692-75e219d6ff4c)

The Final project of the course was to create a website of student’s own interests. I am a huge fan of horror films and horror culture, so I decided to create website for this theme. My idea was that somewhere in the world is a haunted mansion, which is a hotel for those who are looking for some unforgettable experience. And because it is a hotel, there must be possibility to book a room. There is also a restaurant in the hotel and image gallery presents different servings. The hotel has its own horror themed library and movie theatre and of course there is a presentation page for the staff. I also choose a location for the hotel just that I can try embedding google maps on the web site.
<br><br>
### HTML

The assignment was to use different html tags as versatile as possible. The web site should contain ordered/unordered list, images, links, table, form and image gallery.  

#### HTML lists and table

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/ac05ef74-2819-440b-a59b-6dfa5fdbc8c9)

I included both ordered and unorderd list to my web page. There is a site called library, and the idea was that the hotel has its own collection of most famous horror books. Visitors can borrow the books while staying in the hotel and sink deep in the world of horrors. HTML lists was good way to pop up some spesific books. Below is a table where the whole collection is listed.

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/3ea39115-84b6-4b06-8c9a-2d0cb39de59b)

  
```
<div id="lista1">
	  <h3> Most popular books </h3>
	  <ol>
		<li>Interview with a Vampire, by Anne Rice</li>
		<li>The Legend of Sleepy Hollow, by Washington Irving</li>
		<li>Dracula, by Bram Stoker</li>
		<li>Pride and Prejudice and Zombies, by Jane Austen & Seth Grahame-Smith</li>
		<li>Necronomicon, by H. P. Lovecraft</li>
	  </ol>
</div>
```

```
<div id="lista2">
	  <h3>Our recommendations:</h3>
	  <ul>
		<li>Carmilla, by Sheridan Le Fanu</li><br>
		<li>The Raven, by Edgar Allan Poe</li><br>
		<li>American Gothic, by Jonathan Rigby </li><br>
	  </ul>
</div>
```
Both lists (ordered / unorderd) is placed in their own divs so it was possible to place them side by side. Divs "lista1" and "lista2" are placed in one div called row, and that div also includes the text above the lists.
<br>

#### HTML image gallery

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/11cb2b69-ebbf-4683-80fc-37d698e6871a)

Image gallery is greated using divs. Inside the body there is one row which is divided into four columns. Images are inserted in the columns with 100% width. When image is clicked, it opens in a new tab with full size. 

```
<a target="_blank" href="images/gallery/bowl-breakfast-calcium-cereal-414262.jpg">
<img src="images/gallery/bowl-breakfast-calcium-cereal-414262.jpg" style="width:100%"></a>
```
If I would work with this project now, I would rename the images. 
<br>
#### HTML form

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/77dcbd6c-55e0-4372-9e12-31e901d95e47)

```
	<form>
	<fieldset id="form1">
		<legend>Book a room</legend>
		<form action="/action_page.php" method="post>
		
		<label for="First Name">First name</label>
		<input type="text" value=""><br><br>
		
		<label for="Last Name">Last name</label>
		<input type="text" value=""><br><br>
		
		<label for="email">Email</label>
		<input type="email" id="email" name="email"><br><br>
		
		<label for="phone">Phone number</label>
		<input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"><br><br>
		
		<label for="datemin">Check in</label>
		<input type="date" id="datemin" name="datemin" min="2020-04-01"><br><br>
		
		<label for="datemin">Check out</label>
		<input type="date" id="datemin" name="datemin" min="2020-04-01"><br><br>
		
		<label for="rooms">Choose a room</label>
		<select id="rooms" name="rooms">
			<option value="single" selected>Single room</option>
			<option value="twin">Twin room</option>
			<option value="double">Double room</option>
			<option value="suite">Suite</option>
		</select><br><br>
		
		<label for="rooms">Message</label><br><br>
		<textarea name="message" rows="10" cols="30"></textarea><br><br>
		
		<input type="submit" value="Submit">
	</fieldset>
	</form>
```
The form is created with very basic elements, labels, and inputs. I tried to think what would be essential when booking a room. Little title "Book a room" is created with legend-tag. 
Because JavaScript wasn't included in this course, there is no action in the form. If I would develop this forward, there could be a calculator for the price of selected room (and maybe some other services - breakfast for bed?) and maybe some payment methods listed. I also recognise some bad, hardcoded information in the HTML.  
<br>
### Styles

#### Backgroung

It is not very common to use images as background anymore, but I wanted to do so, and I think that it fits for the theme of the website. The background image is full screen and scalable. It does not repeat itself and it stays still when user is scrolling the page. 
```
body {
	background-image: url("images/angel-3889929.jpg");
	background-repeat: no-repeat;
	background-position: left top;
	background-attachment: fixed;
	background-size: cover;
}
```
The background of the actual content uses a class named card. The colour of this card has been defined white (255, 255, 255) and there is 50% opacity (0.5) and that’s how the background image is hovering through.
```
.card {
	background-color: rgba(255, 255, 255, 0.5);
	padding: 20px;
	margin-top: 20px;
```

#### Navigation

![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/2e8a311d-699f-40b1-8921-0441c0730f69)

Navigation is created in ```top-nav``` class in html and there is a list of links. The link text is defined white, and the background is black. When user points a cursor top of the links, colours switch their places.
```
.topnav {
	overflow: hidden;
	background-color: black;
	color: white;
	padding-left: 130px;
}

.topnav a {
	float: left;
	display: block;
	color:#f2f2f2;
	text-align: center;
	padding: 14px 16px;
	text-decoration: none;
	text-align: center;
	display: inline-block;
}

.topnav a:hover {
	background-color: #ddd;
	color: black;
}
```
![image](https://github.com/nina20126/My_First_WebSite/assets/77397102/cc80333a-423c-45ed-8f9e-c88c7b3c7dab)

Also, the table (located in Library-site) is using same kind of hovering efect because the list is so long. Now it is much easier for the user to browse the collection. (Unfortunately, the cursor is not visible in the screenshot.)

### What did I learn?

HTML was developed a lot since last time I was using it. CSS part was practically all new to me. Even if I had written some styles in the middle of HTML earlier, it was very different world. It was like chancing the font colour or background colour, and that all. Participating in this course was a good reminder that I still love this kind of doing and at the same year (2020) I applied to study Information and Communication technologies at Häme University of Applied Sciences and got approved. There are many things that I would do differently right now, and there are some mistakes, but I wanted to leave the project as it is. This is where all started. At the time I was very proud of this project.
