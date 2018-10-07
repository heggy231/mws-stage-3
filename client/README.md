# Mobile Web Specialist Certification Course
---
#### _Three Stage Course Material Project - Restaurant Reviews_

## Stage 2: ###########################################################

1) Run terminal, CD to API server directory: [Server code](https://github.com/heggy231/mws-restaurant-stage-2)
2) Run the following code your terminal:    
    ###### Install project dependencies
    ```Install project dependencies [don't copy the # hashtag, it is just the indication that this is a code you need to put inside of terminal, run this for the first time only]
    # npm i
    ```
    ###### Install Sails.js globally (run this for the first time only)
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

3) copy http://localhost:1337/restaurants to your browser and see your data running on Sails server!

info:
info:                .-..-.
info:
info:    Sails              <|    .-..-.
info:    v0.12.14            |\
info:                       /|.\
info:                      / || \
info:                    ,'  |'  \
info:                 .-'.-==|/_--'
info:                 `--'-------'
info:    __---___--___---___--___---___--___
info:  ____---___--___---___--___---___--___-__
info:
info: Server lifted in `/Users/****/Desktop/mws-restaurant-stage-2`
info: To see your app, visit http://localhost:1337
info: To shut down Sails, press <CTRL> + C at any time.


# Local Development API Server
## Usage
#### Get Restaurants
```
curl "http://localhost:1337/restaurants"
```
#### Get Restaurants by id
````
curl "http://localhost:1337/restaurants/{3}"
````

## Architecture
Local server
- Node.js
- Sails.js

## Contributors

- [Brandy Lee Camacho - Technical Project Manager](mailto:brandy.camacho@udacity.com)
- [David Harris - Web Services Lead](mailto:david.harris@udacity.com)
- [Omar Albeik - Frontend engineer](mailto:omaralbeik@gmail.com)

## Getting Started Stage 2

### Development local API Server
_Location of server = /server_
Server depends on [node.js LTS Version: v6.11.2 ](https://nodejs.org/en/download/), [npm](https://www.npmjs.com/get-npm), and [sails.js](http://sailsjs.com/)
Please make sure you have these installed before proceeding forward.

Great, you are ready to proceed forward; awesome!

Let's start with running commands in your terminal, known as command line interface (CLI)




If you find a bug in the source code or a mistake in the documentation, you can help us by
submitting an issue to our [Waffle Dashboard](https://waffle.io/udacity/mwnd-issues). Even better you can submit a Pull Request with a fix :)




## Project Overview: Stage 1 ####################################
- Introduction video watch here >>> https://www.youtube.com/watch?time_continue=1&v=N-Tf905Oerk

For the **Restaurant Reviews** projects, you will incrementally convert a static webpage to a mobile-ready web application. In **Stage One**, you will take a static design that lacks accessibility and convert the design to be responsive on different sized displays and accessible for screen reader use. You will also add a service worker to begin the process of creating a seamless offline experience for your users.

### Specification

You have been provided the code for a restaurant reviews website. The code has a lot of issues. It’s barely usable on a desktop browser, much less a mobile device. It also doesn’t include any standard accessibility features, and it doesn’t work offline at all. Your job is to update the code to resolve these issues while still maintaining the included functionality. 

### Requirements
  1. Make the provided site fully responsive. All of the page elements should be usable and visible in any viewport, including desktop, tablet, and mobile displays. Images shouldn't overlap, and page elements should wrap when the viewport is too small to display them side by side.

  2. Make the site accessible. Using what you've learned about web accessibility, ensure that alt attributes are present and descriptive for images. Add screen-reader-only attributes when appropriate to add useful supplementary text. Use semantic markup where possible, and aria attributes when semantic markup is not feasible.

  3. Cache the static site for offline use. Using Cache API and a ServiceWorker, cache the data for the website so that any page (including images) that has been visited is accessible offline.

### What do I do from here?
- Option 1
1. Run with Web Server for Chrome
2. CHOOSE FOLDER to your site file local repo.
3. Check mark on Options: Accessible on local network
   Check mark on Auto show index.html
   Enter Port: 8887
   Set CORS headers
4. Set your URL to http://127.0.0.1:8887

- Option 2
1. In this folder, start up a simple HTTP server to serve up the site files on your local computer. Python has some simple tools to do this, and you don't even need to know Python. For most people, it's already installed on your computer. 
  In a terminal, check the version of Python you have: `python -V`. If you have Python 2.x, spin up the server with `python -m SimpleHTTPServer 8777` (or some other port, if port 8000 is already in use.) For Python 3.x, you can use `python3 -m http.server 8000`. If you don't have Python installed, navigate to Python's [website](https://www.python.org/) to download and install the software.
2. With your server running, visit the site: `http://localhost:8777`, and look around for a bit to see what the current experience looks like.
3. Explore the provided code, and start making a plan to implement the required features in three areas: responsive design, accessibility and offline use.
4. Write code to implement the updates to get this site on its way to being a mobile-ready website.

## Leaflet.js and Mapbox:

This repository uses [leafletjs](https://leafletjs.com/) with [Mapbox](https://www.mapbox.com/). You need to replace `<your MAPBOX API KEY HERE>` with a token from [Mapbox](https://www.mapbox.com/). Mapbox is free to use, and does not require any payment information. 

### Note about ES6

Most of the code in this project has been written to the ES6 JavaScript specification for compatibility with modern web browsers and future proofing JavaScript code. As much as possible, try to maintain use of ES6 in any additional JavaScript you write. 



