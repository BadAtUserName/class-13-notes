# class-13-notes
Class 13 notes

Local storage and how to use it

1. Quick summary
  A. Storing info locally on a users computer is strong Strat for dev creating something for web 
  B. http is stateless you open it/close it resets upon close. 
  C. When closing app on desktop it is restored to prior state normally…like excel
  D. Must store state of interface somewhere
  E. Local storage keeps key on users computer, and reds it out when user returns 

II. C is for cookie. Is that good enough for me? 
     A. Classic way to store a state is by using a cookie.
	a. Cookie is text file hosted on users computer and connected to the domain your website runs on<br>
		1. Can store info read them out and delete them
	b. Cookies limitations 
		1. They add to the load of very doc accessed on the domain
		2. Only allow up to 4KB of data storage. 
		3. Cookies used to spy on peeps behavior security conscious people and companies turn them off. 

III. Using local strong in html5-capable browsers
      A. Local storage in modern browsers super easy. 
	a. Today the local storage obj in JS. Can do that directly or use the setItem() and getItem() method
	b. See this link right here for example 
IV. Working Around The Strings Only Issue
	a. Short coming of local storage can only store strings in different keys. 
		1. When have obj won’t be stored correctly. 
	b. Can work around with native JSON.stringify() and JSON.parse() methods:

V. Where to find local storage data and how to remove It
	A. Sometimes you are stuck and just want to remove everything, flip the table and clear it. 
		a. Can do so by going to preferences -> Advanced -> storage
			i. Can view see which domains have local storage and how much. 
		b. Doing so in chrome is a little trickier

VI. Use Case 1 local storage of web service data
	A. Caching data so load times are faster on the second round. 
		a. Following code uses jQuery provides main functionality for this. 
			1. If local store is supported and a key called thewholefrigginworld t
			2. Then call the render() method which displays the information.n 
			3. Otherwise show a loading message and make call to Geo API
			4. Once data has loaded. Store it in thewholefrigginworld & call render()
	B. Can be powerful if web service allow you to only make a certain number of calls per hour but data doesn’t change often. 
	C. Common when using web services  server side local caching keep you from being banned. 
	D. Also means if api fails you still have something to display

VII. Use Case 2 maintain the state of an Interface Simple Way.
	A. Another use case is to store the state of interfaces. 
		a. Could be as crude as storing the entire HTML or as clever as maintains an object with the state of all your stuff/widgets.
		b. Do note need YUI/ just makes it easier. 
			1. Logic always the same check if submit button has been activated if yes store in innerHTML of entire form. 
			2. Or just ready from local storage and override with innerHTML

VII. The Dark Side Of Local Storage
	A. With great power comes great responsibility. 
		1. Demo called ever cookie spooky


Why would a developer use local storage for a web application?
	a. If you have something that is very large on load, using local storage means that on the following load it will not take that long. 
What information should not be stored in local storage?
	a. You should not store sensitive information in local storage. 
Local storage can store what type of data? How would you convert it to that type before storing?
	a. Local storage can only store strings, you can get around this by using JSON.stringify() and JSON.parse() methods. 

## Things i want to know more about
evercookie
