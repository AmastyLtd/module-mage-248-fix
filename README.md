<h1>Magento 2.4.8 Issues Fix Module</h1>

<h2>Overview</h2>
<p>This module is required to address several specific issues in Magento 2.4.8:</p>
<ul>
    <li>
        <strong><a target="_blank" href="https://github.com/magento/magento2/issues/39817">#39817</a></strong>: Ignored .less styles with <code>min-width: (@screen__l)</code>.
    </li>
    <li>
        <strong><a target="_blank" href="https://github.com/magento/magento2/issues/39806">#39806</a></strong>: Store switcher not working (page served from cache after store switch).
    </li>    <li>
        <strong><a target="_blank" href="https://github.com/magento/magento2/issues/39831">#39831</a></strong>: Calendar popup opens over display.
    </li>
    <li>
        <strong><a target="_blank" href="https://github.com/magento/magento2/issues/39847">#39847</a></strong>: Table prefix is not taken into account.
    </li>
</ul>
<p>By resolving these issues, the module ensures a smoother and more reliable Magento 2.4.8 experience for both administrators and end-users.</p>

<h2>Issue Details</h2>

<h3>Issue #39817: Ignored .less Styles with <code>min-width: (@screen__l)</code></h3>
<p>
    This issue occurs when Magento 2.4.8 ignores styles defined in <code>.less</code> files with the media query <code>min-width: (@screen__l)</code>. 
    As a result, certain responsive styles are not applied, leading to inconsistent or broken layouts on larger screens.
</p>

<h3>Issue #39806: Store Switcher Not Working (Page Served from Cache)</h3>
<p>
    This issue arises when switching between stores using the store switcher functionality. Instead of loading fresh content for the selected store, Magento serves the page from the cache, displaying outdated or incorrect content.
</p>

<h3>Issue #39831: Calendar popup opens over display</h3>
<p>
    Datepicker calendar popup may open over display or in wrong position after scrolling the page.
</p>

<h3>Issue #39847: Table prefix is not taken into account</h3>
<p>
   If you are using a table prefix, there will be an error on the theme change page because the table prefix is not taken into account. Fixed missing table prefix usage.
</p>

<h2>Installation</h2>
<h3>Option 1: Installation via Composer (Recommended)</h3>
<ol>
    <li>Open your terminal and navigate to the root directory of your Magento 2.4.8 installation.</li>
    <li>Run the following command to install the module:
        <pre><code>composer require amasty/module-mage-248-fix -W</code></pre>
    </li>
    <li>Enable the module by running:
        <pre><code>php bin/magento setup:upgrade</code></pre>
        <pre><code>php bin/magento setup:di:compile</code></pre>
        <pre><code>php bin/magento cache:flush</code></pre>
    </li>
</ol>

<h3>Option 2: Manual Installation</h3>
<ol>
    <li>Download the module files from the repository.</li>
    <li>Place the module files in the <code>app/code/Amasty/Mage248Fix</code> directory of your Magento 2 installation.</li>
    <li>Run the following commands to enable the module:
        <pre><code>composer require wikimedia/less.php:^5.3.1</code></pre>
        <pre><code>php bin/magento setup:upgrade</code></pre>
        <pre><code>php bin/magento setup:di:compile</code></pre>
        <pre><code>php bin/magento cache:flush</code></pre>
    </li>
</ol>

<h2>Requirenements</h2>
<p>This module require:</p>
<ul>
    <li>Magento 2.4.8 version</li>
    <li>Amasty Base module exists</li>
    <li>wikimedia/less.php:^5.3.1</li>
</ul>

<h2>Configuration</h2>
<p>No additional configuration is required. The module automatically applies the fixes upon installation and activation.</p>

<p>The issues above partially break the functionality of Amasty modules; however, they can be reproduced without our modules being installed and may generate problems on a clean Magento instance. This is why we made this package public.</p>

<h2>This package is required for the proper functioning of the following Amasty extensions:</h2>
-> <a href="https://amasty.com/lite-layered-navigation-for-magento-2.html" rel="dofollow" target="_blank">Layered Navigation for Magento 2</a><br>
-> <a href="https://amasty.com/advanced-product-reviews-for-magento-2.html" rel="dofollow" target="_blank">Advanced Product Reviews for Magento 2</a><br>
-> <a href="https://amasty.com/advanced-reports-for-magento-2.html" rel="dofollow" target="_blank">Advanced Reports for Magento 2</a><br>
-> <a href="https://amasty.com/advanced-search-for-magento-2.html" rel="dofollow" target="_blank">Advanced Search for Magento 2</a><br>
-> <a href="https://amasty.com/ajax-shopping-cart-for-magento-2.html" rel="dofollow" target="_blank">AJAX Shopping Cart for Magento 2</a><br>
-> <a href="https://amasty.com/automatic-related-products-for-magento-2.html" rel="dofollow" target="_blank">Automatic Related Products for Magento 2</a><br>
-> <a href="https://amasty.com/blog-pro-for-magento-2.html" rel="dofollow" target="_blank">Blog Pro for Magento 2</a><br>
-> <a href="https://amasty.com/b2b-company-account-for-magento-2.html" rel="dofollow" target="_blank">B2B Company Account for Magento 2</a><br>
-> <a href="https://amasty.com/custom-form-for-magento-2.html" rel="dofollow" target="_blank">Custom Form for Magento 2</a><br>
-> <a href="https://amasty.com/customer-group-auto-assign-for-magento-2.html" rel="dofollow" target="_blank">Customer Group Auto Assign for Magento 2</a><br>
-> <a href="https://amasty.com/free-gift-for-magento-2.html" rel="dofollow" target="_blank">Free Gift for Magento 2</a><br>
-> <a href="https://amasty.com/full-page-cache-warmer-for-magento-2.html" rel="dofollow" target="_blank">Full Page Cache Warmer for Magento 2</a><br>
-> <a href="https://amasty.com/gdpr-for-magento-2.html" rel="dofollow" target="_blank">GDPR Pro for Magento 2</a><br>
-> <a href="https://amasty.com/cookie-consent-for-magento-2.html" rel="dofollow" target="_blank">Cookie Consent (GDPR) for Magento 2</a><br>
-> <a href="https://amasty.com/improved-layered-navigation-for-magento-2.html" rel="dofollow" target="_blank">Improved Layered Navigation for Magento 2</a><br>
-> <a href="https://amasty.com/landing-pages-for-magento-2.html" rel="dofollow" target="_blank">Landing Pages for Magento 2</a><br>
-> <a href="https://amasty.com/multiple-wishlist-for-magento-2.html" rel="dofollow" target="_blank">Multiple Wishlist for Magento 2</a><br>
-> <a href="https://amasty.com/one-step-checkout-for-magento-2.html" rel="dofollow" target="_blank">One Step Checkout Pro for Magento 2</a><br>
-> <a href="https://amasty.com/out-of-stock-notification-for-magento-2.html" rel="dofollow" target="_blank">Out of Stock Notification for Magento 2</a><br>
-> <a href="https://amasty.com/product-tabs-for-magento-2.html" rel="dofollow" target="_blank">Product Tabs for Magento 2</a><br>
-> <a href="https://amasty.com/quick-order-for-magento-2.html" rel="dofollow" target="_blank">Quick Order for Magento 2</a><br>
-> <a href="https://amasty.com/request-a-quote-for-magento-2.html" rel="dofollow" target="_blank">Request a Quote for Magento 2</a><br>
-> <a href="https://amasty.com/shipping-cost-calculator-for-magento-2.html" rel="dofollow" target="_blank">Shipping Cost Calculator for Magento 2</a><br>
-> <a href="https://amasty.com/shop-by-brand-for-magento-2.html" rel="dofollow" target="_blank">Shop by Brand for Magento 2</a><br>
-> <a href="https://amasty.com/special-promotions-for-magento-2.html" rel="dofollow" target="_blank">Special Promotions for Magento 2</a><br>
-> <a href="https://amasty.com/store-pickup-for-magento-2.html" rel="dofollow" target="_blank">Store Pickup for Magento 2</a><br>
-> <a href="https://amasty.com/subscriptions-recurring-payments-for-magento-2.html" rel="dofollow" target="_blank">Subscriptions & Recurring Payments for Magento 2</a><br>
-> <a href="https://amasty.com/store-pickup-for-magento-2.html" rel="dofollow" target="_blank">Color Swatches Pro for Magento 2</a><br>
