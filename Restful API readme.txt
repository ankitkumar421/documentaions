* Getting Started With APIs
	
	API (Application programming interface) , in a nutsheel we can say it acts like a bridge between your wesite and the server
	Its major function is sending/reciving datas from servers or your local Database.

	Which API you want to use depends on your application and your choice because all APIs have there pros and cons.

	Types of APIs are :-
	1> GET 
	2> POST
	3> PUT
	4> DELETE


	* GET - It is one of the most commonly and widely used method in APIs and websites. In GET request parameters are to be sent within the url.
		EXAMPLE - GET/http://localhost3000/student
			  http://localhost3000/student?name=ankit
		The above url is an example of a GET request with an endpoint student, So let us say there is a database of students which contains information of all the students
		So, the above url should return all the students info.

		BUT what is we want to get detail of one perticular student with an unique ID?
		So, in that case we can pass an paramerter like (GET/http://localhost3000/student/:id) or  and it will give the detail of the student with specific ID

		Quite easy.....well, its not the safest way as you have seen above you pass the paraeter which is here the ID of a student, as this an URL so it can be bookmarked along with the ID which not safe!!
		as it can be accessed by anyone.

		Then you will think ... ok I will use this method to get basic information and parapeters but again here comes the twist as you can do so but.. there are limitaion of caracters which you can pass while 
		using GET request.There is a limit of aprrox of 2000 char in the URL.

		After this all restrictions you would be thinking so what if I want to recive a data which is private or something important or I want a url with no char restrictions. So here the POST request comes handy


        * POST - POST is the HTTP method that is designed to send loads of data to a server from a specified resource. Most common HTML forms on the web operate using this request method. 
		 It usually transmits relatively small loads of data to a receiver. This method allows data to be sent as a package in a separate communication with the processing script. 
		 This means that data sent through the POST method will not be visible in the URL, as parameters are not sent along with the URI.

		 POST method is safer and not easily cracked up. POST parameters are not maintained in the server or webpages thus it is not easily accessed. 
		 It is therefore discouraged for one to inscribe delicate information through the GET method such as credit card pins and passcodes. Such information is detectable as information posted on the URL is accessible to anyone.

		 (POST/http://localhost3000/newStudent) this url can be used to add new student to student DB and as the parameter are not passed in the url its data can not be retrived by anyone

	* PUT - This api is genrally used for update operation(s), It can be send as GET using url (PUT /student/:id), it don't matters how many times you send the request it will be equivalent to sending one update request

	* DELETE - As the name suggests the DELETE api is used to delete a data from server or DB (http://localhost3000/student/:id) can be send with DELETE api to delete the data of student with specific ID.

* Getting hands on nodes

	NODE JS is an open source platform which works on JavaScript Runtime Envoirnment 

	But before diving in first we need to install some pakeges for this open the terminal
	using "Ctrl+Shift+`". After the terminal is open....

	Lets install a pakege : npm i express;

	Now, lets try to print a msg on browser "Hello World", using get request.

	let express = require('express'); // calling the express pakage in our file 
	let app = express() // lets keep the express package in variable (app)

	* Making a GET request url

		app.get('/home', (req, res) => {
			res.send('Hello World');
		});


		app.listen(3000, () => {
    		console.log(`server is running on port 3000`); // app.listen is used to tell the node where to run the app	
		});												   // in this case it will run on port 3000


	To test this open crome and write
	(localhost3000) in the url. You should get Hello World redering on the page




		
		
	
// Documentation to be covered	
	javascript events
	cookies and session storage and local storage
	data types: number, string, objects, array
	select list, radio, checkbox and checkboxes,
	error handling
	form validation
	promise
	prototype
	ajax
	jquery
	