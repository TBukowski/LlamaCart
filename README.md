
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
    5. use cors on backend / DONE

Add webpack
    1. cd frontend / DONE
    2. npm install -D webpack webpack-cli webpack-dev-server / DONE
    3. npm uninstall live-server / DONE
    4. "start": "webpack-dev-server --mode development --watch-content-base --open" / DONE
    5. move index.html, style.css and images to frontend folder / DONE
    6. rename app.js to index.js / DONE
    7. update index.html / DONE
    8. add <script src="main.js"></script> before <body> / DONE
    9. npm start / DONE
    10. npm install axios / DONE
    11. change fetch to axios in HomeScreen / DONE

Install Babel for ES6 syntax
    1. npm install -D babel core, cli, node, preset-env / DONE
    2. create .babelrc and set preset to @babel/preset-env / DONE
    3. npm install -D nodemon / DONE
    4. set start nodemon --watch backend --exec babel-node backend/server.js / DONE
    5. convert require to import in server.js / DONE
    6. npm start / DONE

Enable code linting
    1. npm install -D eslint / DONE
    2. install vscode eslint extension / DONE
    3. create .eslintrc and set module.exports for env to node / DONE
    4. set vscode setting for editor.codeActionsOnSave source.fixAll.eslint to true / DONE
    5. check result for linting error / DONE
    6. npm install eslint-config-airbnb-base and eslint-plugin-import / DONE
    7. set extends to airbnb-base / DONE
    8. set parserOptions to ecmaVersion 11 and sourceType to module / DONE
    9. set rules for no-console to 0 to ignore linting error / DONE

Install VS Code Extension
    1. JavaScript (ES6) code snippets / DONE
    2. ES7 react/redux/graphql/react-native snippets / DONE
    3. prettier - code formatter / DONE
    4. html&less grammer injections / DONE

Create Rating Component
    1. create components/Rating.js / DONE
    2. create div.rating / DONE
    3. link to fontawesome.css in index.html / DONE
    4. define Rating object with render() / DONE
    5. if !props.value return empty / DONE
    6. else use fa fa-star, fa-star-half-o and fa-star-o / DONE
    7. last span for props.text || '' / DONE
    8. style div.rating, span and last span / DONE
    9. edit HomeScreen / DONE
    10. add div.product-rating and use Rating component / DONE