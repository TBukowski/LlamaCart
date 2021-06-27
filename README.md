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
    8. Fix flex styling for list products

Render dynamic home screen
    1. create data.js
    2. export an array of 6 products
    3. create screen/HomeScreen.js
    4. export HomeScreen as an object with render() method
    5. implement render()
    6. import data.js
    7. return products mapped to lis inside ul
    8. create app.js
    9. link app.js to index.html as module
    10. set main id to main_container
    11. create router() function
    12. set main_container innerHTML to HomeScreen.render()
    13. set load event of window to router() function