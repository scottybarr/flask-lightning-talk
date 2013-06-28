#Flask Lightening Talk - Sipping From The Flask

#What is Flask?
 - Web framework written in Python
 - April Fools Joke - Originally ~800 LOC - Turns out it was pretty good code!

# Your First Flask Project
 - First things first - Dependencies!
 - Initialise a new variable called app that calls the Flask constructor.
 - Define a route on '/' that decorates the method named 'hello'. This route will return a string saying "Hello World!"
 - Run the app!

# Flask vs Django - Overview
 - One of the big talking points in Python web communities is Flask vs Django.
 - Flask is simple and extensible. It is rather barebones by not including batteries.
 - Django is rather monolithic and encourages tight coupling.
 - It includes the batteries (Templating, ORM, auth, even a debug toolbar...)

# Flask vs Django - URL Routing
 - Flask has beautiful URL routes.
 - Supports basic types (string, int, float, ...) but you can also define your own rules!
 - Django uses regex

# Flask vs Django - Accepted HTTP Request Methods
 - In Flask you can define the accepted Request Methods in the URL route. If you attempt to use a method that is not supported by that route you will get a 405 method not allow.
 - In Django you have to do your own checking on those methods in your view and do the 405 yourself...

# Flask vs Django - Returning JSON
 - In Flask you have a jsonify method that takes a python dictionary or list, encodes it as JSON and sets the appropriate mimetype.
 - As you can see in Django, you have to do all of that yourself...
 
# Interesting URL Route
 - Similar to a simplified URL carhire route.
 - Begins with a string indicating it's a results page.
 - Defines a locale separated by a hyphen.
 - a currency
 - iata codes
 - a driver age.
 - We can provide types to the Flask route for each individual parameter to ensure URL validity. Flask will also convert these parts into the defined type when it passes these as parameters to the view method.
