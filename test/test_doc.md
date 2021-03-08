# Developers Guide to Headless Commerce

<div class="otp" id="no-index">

### On this page
- [Developers Guide to Headless Commerce](#developers-guide-to-headless-commerce)
    - [On this page](#on-this-page)
  - [Ways to implement headless](#ways-to-implement-headless)
    - [Pre-built solutions](#pre-built-solutions)
    - [Starter apps](#starter-apps)
    - [Custom solutions](#custom-solutions)
  - [Storefront channels](#storefront-channels)
  - [Multisite](#multisite)
  - [Catalog Management](#catalog-management)
    - [Real time catalog](#real-time-catalog)
    - [Real time pricing and inventory](#real-time-pricing-and-inventory)
  - [Cart management](#cart-management)
    - [Sync the catalog](#sync-the-catalog)
    - [Guest Cart](#guest-cart)
    - [Content management system](#content-management-system)
  - [Checkout management](#checkout-management)
  - [Related resources](#related-resources)
    - [Articles](#articles)
    - [Endpoints](#endpoints)
    - [Tools](#tools)

</div>

This article providers a high level guide to using BigCommerce to power headless storefronts; we'll assume you're already familiar with headless commerce as a concept; if you're not, check out our whitepaper, [A New Era of Ecommerce: Headless Commerce](https://www.bigcommerce.com/new-era-headless-caas/) or the Help Center's [Healdess Commerce Guide](https://support.bigcommerce.com/s/article/The-Headless-Approach).

## Ways to implement headless

Which headless approach fits your business requirements?

* [I want to use BigCommerce headlessly with little or no coding](#pre-built-solutions).
* [I want to build a custom solution, but I don't want to code it from scratch](#starter-apps).
* [I want to extend an existing solution or build one from scratch](#custom-solutions).

### Pre-built solutions

Want to build a headless storefront powered by a BigCommerce back-end, but don't want to write a bunch of code? Use one of the pre-built headless storefront solutions below.

|  Solution | Method of Integration | Platform | Type |
| --- | --- | --- | --- |
| [DEITY Falcon](https://www.bigcommerce.com/apps/deity-falcon-pwa-storefront/) | BigCommerce App | DEITY Faclon | PWA |
| [Bloomreach](https://www.bigcommerce.com/apps/bloomreach/) | BigCommerce App | Bloomreach | CMS / DXP |
| [Sitrecore Extend](https://www.bigcommerce.com/apps/sitecore-extend/) | BigCommerce App | Sitecore | CMS |
| [BigCommerce for Wordpress](https://wordpress.org/plugins/bigcommerce/) | WordPress Plugin | WordPress | CMS |
| [BigCommerce for Drupal](https://www.drupal.org/project/bigcommerce) | Drupal Module | Drupal | CMS |

[See more headless solutions and tools](https://developer.bigcommerce.com/tools-resources).

### Starter apps

Need code up a custom storefront but don't want to start from scratch? Kick-start your development with one of the following starter apps.

|  Starter | Stack |
| --- | --- |
| [gatsby-bigcommerce-netlify-cms-starter](https://github.com/bigcommerce/gatsby-bigcommerce-netlify-cms-starter) | Node / React / Gatsby / Netlify |
| [bc-nuxt-vue-starter](https://github.com/bigcommerce/bc-nuxt-vue-starter) | Node / Vue / Nuxt |
| [acf_bc](https://github.com/thirdandgrove/acf_bc) |PHP / ACF / Drupal |

[See more headless starter apps and tools](https://developer.bigcommerce.com/tools-resources).

### Custom solutions

Need to build a custom solution from scratch? Bigcommerce has APIs, SDKs, and toolkits to help you do whatever you need, headlessly.

* [Create storefront channels with the Channels API.](https://developer.bigcommerce.com/api-docs/channels/quick-start).
* [Mannage sites and routes for headless storefronts with the sites and routes API](https://developer.bigcommerce.com/api-reference/store-management/sites).
* [Manage 301 redirects for one or more storefronts with Redirects V3 API](https://developer.bigcommerce.com/api-reference/store-management/redirects)
* [Create storefront specific product listings with the Channels API](https://developer.bigcommerce.com/api-reference/cart-checkout/channels-listings-api).
* [Query storefront data with GraphQL](https://developer.bigcommerce.com/api-docs/storefront/graphql/graphql-storefront-api-overview).
* [Use customer impersonation tokens to query data specific to the shopper](https://developer.bigcommerce.com/api-docs/storefront/graphql/graphql-storefront-api-overview#customer-impersonation-tokens).
* [Create carts with the Server-to-Server Carts API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-cart-api).
* [Fetch and display abandoned cart information using the Abandoned Carts API](https://developer.bigcommerce.com/api-reference/cart-checkout/s2s-abandoned-carts).
* [Create and manage shopper wishlists with the Wislists API](https://developer.bigcommerce.com/api-reference/store-management/wishlists)
* [Manage product data with the Catalog API](https://developer.bigcommerce.com/api-reference/catalog/catalog-api).
* [Embed BigCommerce's checkout in an iFrame with Embedded Checkout](https://developer.bigcommerce.com/api-docs/storefronts/embedded-checkout/embedded-checkout-overview).
* [Redirect to BigCommerce's hosted checkout using the Server-to-Server Checkout API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-checkout-api)
* [Create custom BigCommerce hosted checkout pages from scratch using Checkout SDK](https://developer.bigcommerce.com/stencil-docs/customizing-checkout/checkout-sdk-quickstart).
* [Create a custom BigCommerce hosted checkout from a fork of BigCommerce's Checkout-JS](https://github.com/bigcommerce/checkout-js).
* [Build a custom checkout experience from scratch using the Server-to-Server Checkout API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-checkout-api).
* [Restyle the BigCommerce hosted checkout](https://developer.bigcommerce.com/stencil-docs/customizing-checkout/optimized-one-page-checkout).
* [Process payments using the Payments API](https://developer.bigcommerce.com/api-reference/payments/payments-process-payments).
* [Manage orders with Orders V2 and V3 APIs](https://developer.bigcommerce.com/api-docs/store-management/orders).
* [Use webhooks to get notified when specific events occur in BigCommerce](https://developer.bigcommerce.com/api-docs/store-management/webhooks/overview).


## Storefront channels

Want to market your headless storefront as an app in BigCommerce's control panel? Use [Channels Toolkit](https://developer.bigcommerce.com/api-docs/channels/guide/channels-toolkit-reference) to install a storefront channel into [Channel Manager](https://support.bigcommerce.com/s/article/Selling-Everywhere-with-Channel-Manager) during the [single-click app](https://developer.bigcommerce.com/api-docs/apps/guide/types) installation process.

![Channel Manager](https://storage.googleapis.com/bigcommerce-production-dev-center/images/channels/channels-sf-new.png "Channel Manager")

[Learn how to build a storefront channel](https://developer.bigcommerce.com/api-docs/channels/tutorials/storefront).

## Multisite

Use BigCommerce as the back-end for several stores. By placing an application layer between the storefront and the APIs, the application can control which catalog information is pushed to which storefront.

[Learn more about multisite ecommerce with WordPress and BigCommerce](https://medium.com/bigcommerce-developer-blog/multi-site-ecommerce-with-wordpress-and-bigcommerce-40dee194f8a) (medium.com).

## Catalog Management

Using the [Catalog API](https://developer.bigcommerce.com/api-reference/catalog/catalog-api) you can return product data to your product details page and product listing page.



### Real time catalog

If your catalog is changing all the time, you can use the Catalog API to return real time product information.

### Real time pricing and inventory

If you prefer working with a local copy of your data, but want to make sure that high priority pieces of data like pricing and inventory are always up to date, you can consider a hybrid model. A hybrid model would cache only certain product details and pull the other information in real time. BigCommerce has webhooks that you can use for listening to store events.

## Cart management

Use the [Server to Server Cart API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-cart-api) to create carts for existing customers and guest customers.


### Sync the catalog

Best practice is to get product details and cache them in a database to display them. This will speed up the application and allow you to control what information is shown to the customer. Caching the details also lets you implement search in your application.

### Guest Cart

A guest cart assumes the shopper is not a customer and is not logging in or creating an account during checkout. Handle guest checkouts by displaying the cart data to the customer and then moving them to Checkout using the Checkout API.

### Content management system

Using a CMS is a good way to offer a custom shopper experience without needing build a content engine as well. The CMS needs to have a database so catalog information can be stored and retrieved and a way to store accounts. The [BigCommerce WordPress plugin](https://wordpress.org/plugins/bigcommerce/) loads the catalog into the database while using an embedded checkout to display cart and checkout details to customers.

## Checkout management

Use the [Checkout API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-checkout-api) to move the cart to checkout and turn an existing checkout into an order.
is a guest
	3. Add Line Items or Custom Line Items
	4. Add a Billing Address
	5. Add a Shipping Address
	5. Add a Shipping Address
	6. 
	7. bigcommerce

2.  Send a request /POST request to [Orders](/api-reference/orders/orders-api/orders/createanorder)
	8. Make sure the `status_id` is 0
	9.  Add the Customer ID or leave blank if the shopper is a guest
	10. Add Line Items or Custom Line Items
	11. Add a Billing Address
	12. bigcommerce
	13. Add a Shipping Address
	14. Add a Shipping Address
	15. bigcommerce

  GET

	16. Create a custom shipping quote
3.  Take a Payment for the Order using one of the two methods below
4.  Vaulted Card -- The shopper has saved a credit card
	17. [Get Payment Methods](/api-reference/payments/payments-create-payment-token-api/payment-methods/paymentsmethodsget)
	18. [Create Access Token](/api-reference/payments/payments-create-payment-token-api/payment-access-token/paymentsaccesstokenspost)
	19. [Process Payment](/api-reference/payments/payments-process-payments/payment/paymentspost)
5.  Credit Card -- The shopper has not saved a credit card
	20. [Create Access Token](/api-reference/payments/payments-create-payment-token-api/payment-access-token/paymentsaccesstokenspost)
	21. [Process Payment](/api-reference/payments/payments-process-payments/payment/paymentspost)

## Related resources

### Articles
- [Customers Overview](https://developer.bigcommerce.com/api-docs/customers/customers-subscribers-overview)
- [Customer Login API](https://developer.bigcommerce.com/api-docs/customers/customer-login-api)
- [Launching your store](https://support.bigcommerce.com/s/article/Launching-Your-Store)
- [PCI Compliance](https://support.bigcommerce.com/s/article/PCI-Compliance)
- [Multisite Ecommerce with WordPress and BigCommerce](https://medium.com/bigcommerce-developer-blog/multi-site-ecommerce-with-wordpress-and-bigcommerce-40dee194f8a)
- [Matter Makes Waves with a Headless Build using BigCommerce for WordPress](https://medium.com/bigcommerce-developer-blog/matter-makes-waves-with-a-headless-build-using-bigcommerce-for-wordpress-a572bad4bdf8)
- [New Era in Headless CaaS](https://www.bigcommerce.com/new-era-headless-caas/)
- [BigCommerce Doubles Down on Headless Commerce with BloomReach, Sitecore, Adobe Experience Manager, and More](https://www.bigcommerce.com/blog/flexible-headless-commerce-solutions/)
- [Merchants Classification Levels Visa](https://usa.visa.com/support/small-business/security-compliance.html#3)
- [Merchants Classification Levels Mastercard](https://www.mastercard.us/en-us/merchants/safety-security/security-recommendations/merchants-need-to-know.html)
- [Self Assessment Questionnaire (SAQ) Types and Identifying which SAQ is for you](https://www.pcisecuritystandards.org/documents/SAQ-InstrGuidelines-v3_2_1.pdf?agreement=true&time=1562173376464)
- 
- [Maintaining Payment Security](https://www.pcisecuritystandards.org/pci_security/maintaining_payment_security)



### Endpoints
- [Catalog API](https://developer.bigcommerce.com/api-reference/catalog/catalog-api)
- [Server to Server Checkout API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-checkout-api)
- [Server to Server Cart API](https://developer.bigcommerce.com/api-reference/cart-checkout/server-server-cart-api)
- [Orders API](https://developer.bigcommerce.com/api-reference/orders/orders-api)
- [Payments API](https://developer.bigcommerce.com/api-reference/payments)
- [Customers API](https://developer.bigcommerce.com/api-reference/customer-subscribers/v3-customers-api)
- [Validate Customer Password](https://developer.bigcommerce.com/api-reference/customer-subscribers/customers-api/customer-passwords/validatecustomerpassword)

### Tools
- [Checkout SDK](https://github.com/bigcommerce/checkout-sdk-js)
- [WordPress Plugin](https://wordpress.org/plugins/bigcommerce/)