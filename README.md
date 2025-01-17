# Introduction:

Enhance your online store with the Product Preview extension, allowing customers to quickly view product details, check availability, and add items to their cart without leaving the page. The Quick View button opens a modal with essential product information, improving user engagement and boosting conversions. Admins can customize the display of SKU, product number, quantity, and full description from the admin panel.


# Unlock Growth with Bagisto's Feature-Packed ProductQuickView Extension!

* **Quick View Modal:** Users can access detailed product information instantly by clicking a "Quick View" button on the product page.
* **Stock Status:**  Customers can easily see whether the product is in stock or out of stock.
* **Responsive Design:** The modal is fully responsive and works seamlessly across all devices, providing a smooth experience for both desktop and mobile users.
* **User-Friendly:** Intuitive and easy-to-use interface to enhance the shopping experience
* **Increased Conversion Rates:**  By allowing customers to quickly view product details and add them to the cart, this extension streamlines the shopping process.
* **Add to Cart:**  The ability to add the product directly to the cart from the modal without navigating away from the page.
* **Integration Compatibility:** Seamlessly integrate with existing e-commerce platforms for smooth operation and enhanced functionality.
* **Multilingual Support:** The extension will function across 19 different languages, which are currently supported by Bagisto.


# Requirements:
* Bagisto: v2.0.0, v2.2.2
* PHP: 8.1 or higher
* Composer 2.6.3 or higher

# Installation :
Unzip the respective extension zip and then merge "packages" folder into project root directory

* Goto config/app.php file and add following line under 'providers'

```
Brainstreaml\ProductQuickView\Providers\ProductQuickViewServiceProvider::class
```

* Goto composer.json file and add following line under 'psr-4'

```
"Brainstream\\ProductQuickView\\": "packages/Webkul/ProductQuickView/src"
```
* Run these below commands to complete the setup:

```
composer dump-autoload
```
```
php artisan migrate
```
```
php artisan optimize:clear
```

```
composer require tightenco/ziggy
```

* Add the below code in the ProductResource File of Shop Package :

```
'short_description' => $this->short_description,
```


That's it, now just execute the project on your specified domain.
