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
* **Promotional Tools:** Utilize gift cards as part of promotional campaigns, driving sales and customer engagement.
* **Multilingual Support:** The extension will function across 19 different languages, which are currently supported by Bagisto.
* **Version Compatible:** The extension is compatible with both Bagisto version 2.0.0 and the latest version 2.2.2. You can find these versions listed under the Tags [Tags](https://github.com/brainstreaminfo/bagistogiftcard/tags).

# Requirements:
* Bagisto: v2.0.0, v2.2.2
* PHP: 8.1 or higher
* Composer 2.6.3 or higher

# Installation :
Unzip the respective extension zip and then merge "packages" folder into project root directory

* Goto config/app.php file and add following line under 'providers'

```
Brainstream\Giftcard\Providers\GiftcardServiceProvider::class
```

* Goto composer.json file and add following line under 'psr-4'

```
"Brainstream\\Giftcard\\": "packages/Brainstream/Giftcard/src"
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

* Run the below command and select the Giftcard Service provider from the selection :

```
php artisan vendor:publish --force
```
* Include the PayPal credentials in the loadPayPalScript method. Additionally, ensure that the credentials are entered in the PayPal payment gateway section within the Bagisto admin panel.

* Add the mail credentials in the .env file to receive the giftcard via email.

* Add the below code in the CartResource File after the payment_method_title :

```
$this->mergeWhen($this->giftcard_number, [
    'giftcard_number'           => $this->giftcard_number,
    'giftcard_amount'           => $this->giftcard_amount,
    'remaining_giftcard_amount' => $this->remaining_giftcard_amount,
]),
```


That's it, now just execute the project on your specified domain.
