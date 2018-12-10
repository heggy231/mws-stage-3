# mws-stage-3
Run mws files:
1) cd to client folder
====
> 1. start up a simple HTTP server to serve up the site files on your local computer. Python has some simple tools to do this, and you don't even need to know Python. For most people, it's already installed on your computer. 

In a terminal, check the version of Python you have: `python -V`. If you have Python 2.x, spin up the server with `python -m SimpleHTTPServer 8000` (or some other port, if port 8000 is already in use.) For Python 3.x, you can use `python3 -m http.server 8000`. If you don't have Python installed, navigate to Python's [website](https://www.python.org/) to download and install the software.

> 2. With your server running, visit the site: `http://localhost:8000`, and look around for a bit to see what the current experience looks like.
====

2) cd to server folder: Development local API Server
_Location of server = /server_
Server depends on [node.js LTS Version: v6.11.2 ](https://nodejs.org/en/download/), [npm](https://www.npmjs.com/get-npm), and [sails.js](http://sailsjs.com/)
Please make sure you have these installed before proceeding forward.

Let's start with running commands in your terminal, known as command line interface (CLI)

###### Install project dependancies
```Install project dependancies
# npm i
```
###### Install Sails.js globally
```Install sails global
# npm i sails -g
```
###### Start the server
```Start server
# node server
```
### You should now have access to your API server environment
debug: Environment : development
debug: Port        : 1337









- Todo: watch Flexbox tutorial! https://scrimba.com/playlist/pL65cJ
- IDB resources: https://github.com/jakearchibald/idb use when user has network https://developer.mozilla.org/en-US/docs/Web/API/NavigatorOnLine/onLine

- issues: when refresh unfav does'nt stay line restaurant.html 44 follow the logic

Done: 
Does drop down form need lable for a11y?  does screen reader? 


Restaurant Reviews: Stage 3

Functionality

CRITERIA
MEETS SPECIFICATIONS
User Interface

Users are able to mark a restaurant as a favorite, this toggle is visible in the application. A form is added to allow users to add their own reviews for a restaurant. Form submission works properly and adds a new review to the database.

Offline Use

The client application works offline. JSON responses are cached using the IndexedDB API. Any data previously accessed while connected is reachable while offline. User is able to add a review to a restaurant while offline and the review is sent to the server when connectivity is re-established.

Responsive Design and Accessibility

CRITERIA
MEETS SPECIFICATIONS
Responsive Design

The application maintains a responsive design on mobile, tablet and desktop viewports. All new features are responsive, including the form to add a review and the control for marking a restaurant as a favorite.

Accessibility

The application retains accessibility features from the previous projects. Images have alternate text, the application uses appropriate focus management for navigation, and semantic elements and ARIA attributes are used correctly. Roles are correctly defined for all elements of the review form.

Performance

CRITERIA
MEETS SPECIFICATIONS
Site Performance

Lighthouse targets for each category exceed:

Progressive Web App: >90
Performance: >90
Accessibility: >90


-- 
Understanding aria-labelledby:

<p id="restaurant-address" tabindex="0" aria-labelledby="address_label"></p>
       <label id="address_label" class="aria-label">Restaurant Address</label>
to do aria on this HTML element, I simply give it the attiribute aria-labelledby="address_label"
then I create another html element
<label id="address_label" class="aria-label">Restaurant Address</label>
now understand what this attribute on the label is very important class="aria-label"
in your css you are going to need to add this to your file:
.aria-label {
 display: none;
}
what this does is effectively hide the aria-labels
now what's neat is because you can add aria labels in HTML and have them hidden, but in your JavaScript ... modify the contents! So when you are autogenerating your restaurants, you can autogenerate the aria labels too.
here is a code example here:
const aria_label = document.createElement('label');
 aria_label.id = restaurant_name + "_label";
 aria_label.className = "aria-label";
 aria_label.innerHTML = "Link: Restaurant " + restaurant.name + " Details. Neighborhood: " + restaurant.neighborhood + " Address: " + restaurant.address;
that was the aria for a label for a restaurant button. here is the code to make the restaurant button and assign the aria label to it:
const more = document.createElement('button');
 var label_attribute = document.createAttribute("aria-labelledby");
 var restaurant_name = restaurant.name;
 restaurant_name = restaurant_name.replace(/\s+/g, '');
 label_attribute.value = restaurant_name + "_label";
 more.setAttributeNode(label_attribute);
 more.innerHTML = 'View Details';


 - KatieGirl phase 1 project here: https://portfolio.katiegirl.net/2018/07/10/restaurant-reviews-app-stage-1/

 review her aria-labels