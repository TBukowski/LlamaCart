TO DO STEPS

**Using "JavaScript Tutorial - Full ECommerce in 7 Hours [2021]" by Coding with Basir ( https://youtu.be/N3FDyheHVMM ) to gain base knowledge of the working of an ecommerce site. I then plan on making minor to major alterations and creating a inventory management mock app for warehouse use. Possibly, creating a new app all together.

Create folder structure:
    1. create root folder "C:\Users\shute\OneDrive\Desktop\Js\LlamaCart" / DONE
    2. add frontend and backend folders / ADDED FRONTEND
    3. create src folder in frontend / DONE
    4. create index.html / DONE
    5. run npm init in frontend folder / DONE
    6. run npm install -D live-server / FAILED-NEED TO RUN WHILE CONNECTED TO INTERNET
    7. add start command as live-server src --verbose / FAILED
    8. run npm start for test / FAILED

Design
    1. create style.css
    2. link styesheet to index.html / DONE
    3. create div.grid-containter / DONE
    4. create header, main, footer / DONE - ADDED CLASS "brand" TO HEADER
    5. style html and body / DONE
    6. style grid-container, header, main, footer / DONE

Create static home screen
    1. create ul.products / DONE
    2. create li / DONE
    3. create div.product / DONE
    4. add .product-image, .product-name, .product-brand, .product-prize / DONE
    5. style ul.products and internal divs / DONE
    6. duplicate twice to show 3 products / DONE
    7. Add images saved as "product-1.jpg", "product-2.jpg", etc fitting the descriptions / CREATED IMAGES IN PAINT FOR PRODUCT IMAGE
    8. Fix flex styling for list products / DONE ADDED MISSING LI TAGS TO SEPERATE LIST ITEMS

Render dynamic home screen
    1. create data.js / DONE
    2. export an array of 6 products / DONE
    3. create screen/HomeScreen.js / DONE
    4. export HomeScreen as an object with render() method / DONE
    5. implement render() / DONE
    6. import data.js / DONE
    7. return products mapped to lis inside ul / DONE
    8. create app.js / DONE
    9. link app.js to index.html as module / DONE
    10. set main id to main_container / DONE
    11. create router() function / DONE
    12. set main_container innerHTML to HomeScreen.render() / DONE
    13. set load event of window to router() function / DONE

Build URL router
    1. create routes as route:screen object for home screen / DONE
    2. create utils.js / DONE
    3. export paseRequestURL() / DONE
    4. set url as hash address split by slash / DONE
    5. return resource, id and verb of url / DONE
    6. update router() / DONE
    7. set request as parseRequestURL() / DONE
    8. build parsedUrl and compare with routes / DONE
    9. if route exists, render it. else, render Error404 / DONE
    10. create screens/Error404.js and render error message / DONE
    11. Routes are broken, goes to " ~/ ". Needed http://127.0.0.1:8080/ and not http://127.0.0.1:5500/

Add a .gitignore file / DONE

Create Node.js server
    1. run npm init in root folder / DONE
    2. npm install express / DONE
    3. create server.js / DONE
    4. add start command as node backend/server.js / DONE
    5. require express / DONE
    6. move data.js from from frontend to backend / DONE
    7. create route for /api/products / DONE
    8. return products in data.js / DONE
    9. run npm start / DONE

Load product from backend
    1. edit Homescreen.js / DONE
    2. make render async / DONE
    3. fetch products from '/api/products' / DONE
    4. make router() async and call await HomeScreen.render() / DONE
    5. use cors on backend / NEED TO 'npm install cors' in new terminal instance

Add webpack
    1. cd frontend
    2. npm install -D webpack webpack-cli webpack-dev-server
    3. npm uninstall live-server
    4. "start": "webpack-dev-server --mode development --watch-content-base --open"
    5. move index.html, style.css and images to frontend folder
    6. rename app.js to index.js
    7. update index.html
    8. add <script src="main.js"></script> before <body>
    9. npm start
    10. npm install axios
    11. change fetch to axios in HomeScreen