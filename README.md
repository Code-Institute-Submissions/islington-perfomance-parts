![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/logo-flags.png "Islington Performance Parts logo")

# ISLINGTON PERFORMANCE PARTS: WEBSITE

## DESCRIPTION

***

This is a case for a new website and design for Islington Performance Parts (IPP), a fictitous motor vehicle parts shop in the north of Stockholm, Sweden. 
The main purpose of IPP is to provide high end alloy wheels to service the vehicle after-market modification community in Stockholm. 

Currently, the shop services a small community of enthusiasts in the North of Stockholm but is planning to enlarge their sales and after-service facilities to a much larger and wider market. This will be the first time the shop will be listed via a website with the view to attracting more customers from around Sweden and neighbouring Nordic countries.

The shop, located in the Vällingby area in the north of Stockholm, gets very few customers from beyond Kungsholmen (Central Stockholm). The purpose of the webpage and associated order forms, including a digital monthly catalogue, is to increase the customer-base to include a greater reach in the region. 

The website will be divided into four categories in a hope to encourage tech savvy motor enthusiasts:

1. Home: Introduction of IPP, opening hours and a small gallery of performance vehicles enhanced in the shop.
2. Shop: A showcase of the eight most popular alloy wheels with option to purchase and book a fitting.
3. Gallery: An exhibit of the latest styles and trends in the motor vehicle enthusiast's community. 
4. Sign-up: A membership application form with the view to receive a monthly catalogue as well as prospective specials. 
5. Pop-up Bookings: Located on every page in the footer and central on the front page, users can book a time to have their car fitted with new alloys. 

***

## DEPLOYMENT AND LIVE DEMO

The site has been deployed to github and is accessible on [github pages](https://pauld0051.github.io/islington-perfomance-parts).

***

## WIREFRAME

A detailed wire framing process was undertaken to oversee the structure of the site and ensure proper organization of content on desktop and mobile versions of the site.

The final version of the wireframe can be found [here](https://github.com/pauld0051/islington-perfomance-parts/raw/master/IPP%20Wireframe.pdf).

***

## UX

### Brand and visual identity

The IPP logo and font appears on every page the user accesses giving a common theme and expected outcome when users visit any page on the website. The logo font Faster One is coupled with Chivo for text and Exo 2 for headings.

### Users of the site

The vast majority of the users will be either previous customers or new customers looking to buy new wheels for their cars.

Existing and New Customers:

- I want to know what products you're currently stocking
- I want to book a fitting for my vehicle
- I want to know the profiles of the products
- I want to know where the location of the fitting is
- I want to know your opening hours
- I want to know if there are any membership specials

New Customers:

- I want to know can I get any specials for becoming a member

These goals are accomplished by various methods:

- Opening hours is clearly located on the [home page](https://pauld0051.github.io/islington-perfomance-parts/index.html)
- A map for location is clearly located on the [home page](https://pauld0051.github.io/islington-perfomance-parts/index.html)
- Buttons for "Book a fitting" are located in the footer of each page
- The [shop page](https://pauld0051.github.io/islington-perfomance-parts/shop.html) has profile information about each wheel
- A "specials" tag is located on the top of the home page
- Specials are noted on the shop page
- A [gallery page](https://pauld0051.github.io/islington-perfomance-parts/gallery.html) showcases the latest trends and styles of vehicles fitted with new wheels by IPP
- The [sign-up page](https://pauld0051.github.io/islington-perfomance-parts/sign-up.html) gives users a reason to return to the shop time and again

### Responsive design

Customers who visit the page can do so on any device, desktop, tablet, mobile etc.

![alt text](https://github.com/pauld0051/islington-perfomance-parts/raw/master/assets/images/ami-responsive.jpg "islington Perfomance Parts responsive web designs")

The site was built responsive, and users will see the site cut roughly into thirds on each page for ease of access to information and content. 

***

## FEATURES

The site uses various features many of which are native to bootstrap:

-   Image carousels to give users a look into the type of work IPP does on motor-vehicles.
-   Footers and headers are consistent across every page. Users are not surpried with unique content displays on any page.
-   Modal windows on the [shop](https://pauld0051.github.io/islington-perfomance-parts/shop.html) page to display information about products.
-   Progress bars in the modal windows to display the metal-alloy contents of each wheel.
-   On mobile devices the [gallery](https://pauld0051.github.io/islington-perfomance-parts/gallery.html) page changes to a single picture carousel, displaying the content in a more user-friendly fashion. Users can swipe left and right to navigate the information.

### Features still to implement

- JavaScript for form filling rather than eight separate modals in from the shop page. 
- Backend and Database technologies for all forms and purchasing (hence, prices were not included in this version).

## TESTING

The site was tested on various platforms to ensure proper display across different screen sizes.

The HTML was validated on [W3C Validator](https://validator.w3.org/) and CSS on [W3C Validator](https://jigsaw.w3.org/css-validator/).

Form testing was carried out on all forms, including Book a Fitting forms (every page in footer and home page under opening hours) and "Buy Now" forms on the shop page with the eight wheels currently listed for sale. 

The only known issues are with the "Buy Now" forms as no backend is currently available. The CCV help would have also been a "pop-over" however, there is a Javascript requirement preventing this from working as anticipated. 

***

### Issues and bugs

- The map was originally used using an API from Google Maps. However a cost was associated with this technique, instead the map was embedded directly from Google Maps itself. No API or Javascript was required this way and the site loaded considerably faster.
- Users on Firefox may not experience the date and time picker on the form as expected. The icon does not appear on Firefox but does on Chrome. The overall experience is not changed and users can still fill the form as expected. 
- The shop is not open on Sunday, but the "Book a fitting" button allows users to pick Sundays on the date picker. Because of the user accessibility of the built-in datepicker, this was not changed. A Javascript will be incorperated in a later upload to correct for this. 
- The mobile carousel in the gallery added extra padding on the right on load in the inspect module of Chrome. The cause of issue was the "no-gutters" rule which was fixed on discovery. 
- Noted that limiting numbers on the forms needed to be done with the "pattern" attribute with a text input type. Max or minlength do not work for number input types.
- Did not require the MDB CDN for the lightbox carousel as it caused conflicts between the natural Bootstrap and MDB. 
- Discovered on Chrome "inspect" an unexpected padding in the body on very specific circumstances possibly ddue to a Bootstrap module. To remove this, an overflow-x: hidden command was added to the body of all pages.  
- Bootstrap modals adds 17px to padding-right causing "screen jump". To remove this a CSS class for body was created with padding-right: 0 !impotant;

### Load speeds

The site will mostly be accessed from Sweden, however, the site was built to be accessed internationally. With this in mind, images in carousels had the potential to slow the loading speeds. Therefore, to lower the size of all images, tinypng was used. No image deterioration was detectable.

To test speeds, pingdom was used with the following results:

#### Frankfurt Servers (Home, Shop, Gallery and Sign-up)
Fig 1. Results of the Frankfurt (closest) server test for the home page:
![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/home-pingdom.jpg "results of pingdom test for home - Frankfurt servers")

Fig 2. Results of the Frankfurt (closest) server test for the shop page:
![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/shop-pingdom.jpg "results of pingdom test for shop - Frankfurt servers")

Fig 3. Results of the Frankfurt (closest) server test for the gallery page:
![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/gallery-pingdom.jpg "results of pingdom test for home - Frankfurt servers")

Fig 4. Results of the Frankfurt (closest) server test for the sign-up page:
![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/sign-up-pingdom.jpg "results of pingdom test for shop - Frankfurt servers")

The results, although extremely positive, do show that embedded objects (for example, Google Maps) can have a significant effect on the speed of loading. For the most users will not notice or be inconvenienced by the small improvements in using Google APIs or removing the map all together. 

Images (for example, the 18 images in the gallery) have all been compressed to increase speed. Images, however, will still slow any browser load. It is up to the IPP to choose the importance of showing their work with a small trade-off of slower load speeds. It is anticipated that the carousels will never be extended beyond 18 images. 

During the development stage, all code was checked on the latest versions of Chrome, Firefox and Android (Chrome) on a Huawei P20 Pro simultaneously. The use of Bootstrap and similar frameworks was to ensure that most modern browser support was available. However, due to the use of Bootstrap frameworks some older browsers will not support the current site format. Microsoft Edge was also tested in the post production stage, with no noticable differences for the user. Opera browsers are not supported.

Fig 5. Selected results from 25 browser/operating system tests from browserstack.com:
![alt text](https://raw.githubusercontent.com/pauld0051/islington-perfomance-parts/master/assets/images/browserstack.jpg "results of browserstack tests for various combination of browsers and operating systems")

***

### SCALABILITY

For the most, the shop itself can easily increase the number of wheels that are available and a carousel could be introduced for this. When the shop expands, a menu on the left hand side of the shop will allow for other product types (eg, tyres, hoses, clamps etc).
When backend is incorperated, the shop will then be fully extended to data-fetch for all products that are for sale. Prices will then also be included and changes can easily be made in the database. 
A control management system (CMS) should be implemented so as new products come into the shop, employees (even with little experience) can add the product, and images, directly to the website with no need to involve a web-design team. This would also allow employees to add new pictures to the carousels on the home and gallery pages. 

It is also advised that the site uses analytic monitoring to help increase customer base. 
 

## TECHNOLOGIES

### Languages and Frameworks

-   HTML
-   CSS
-   Bootstrap
-   JQuery
-   Hover.css
-   Fontawesome

### Tools Used

-   Balsamiq: Used to create wireframes
-   Gitpod: IDE used for creating and editing code
-   [Font Awesome](https://fontawesome.com): used for all icons throughout the site
-   [Google Maps](https://www.google.com/maps/): used for custom map on homepage
-   [Google Fonts](https://fonts.google.com/): Faster One, Chivo, Exo 2 and Permanent Marker
-   [Gimp](https://www.gimp.org/) 2.10.14: For creation and editing of the logo and adding transparency to wheel images
-   Windows Paint 3d: To resize images appropriately for container sizes and responsive behaviours
-   [W3C Validator](https://validator.w3.org/) used to validate HTML code
-   [W3C Validator CSS](https://jigsaw.w3.org/css-validator/validator)
-   The "buy now" form was partially templated [from tutorialzine.com](https://tutorialzine.com/2016/11/simple-credit-card-validation-form) (multiple modifications were used)
-   Colour gradients (header and footer) were coded [here at colorzilla](https://www.colorzilla.com/gradient-editor/)
-   Images were compressed [here at tinypng](https://tinypng.com/)
-   404 page idea from template at [bootsnipp.com](https://bootsnipp.com/snippets/Qb71)

## MEDIA

-   Photos for the [home page](https://pauld0051.github.io/islington-perfomance-parts/index.html) were sourced from [Pixabay](https://pixabay.com/)
-   Product images were sourced from [Image Wheels UK](https://www.imagewheels.co.uk/dbw-alloy-wheel/)
-   Gallery carousel images were sourced from [TSW After-Market Wheels](https://www.tsw.com/aftermarket-wheels.php)

## ACKNOWLEDGMENTS

-   Many thanks to [Felipe Alarcon](https://github.com/felipe-alarcon) and [Anthony O' Brien](https://github.com/auxfuse) for their invaluable help and feedback and to the Code Institute slack community for their constant support.
