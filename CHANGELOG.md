# Changelog

## 1.0.7 (2019-10-23)
- Customer Addressed Issues
- Fix for un-clickable category links within Mega Nav flyout when there are nested categories beneath 3rd level.
- Fix for subcategory images on category pages appearing out of alignment in some instances. We have set a min-height for the text links beneath the images which will make the floated divs clear and align correctly as there is already a min-height set for the divs containing the images.
- Added Theme Editor options for independent control of Main Nav dropdown font-colors found here: Header & Footer > Main Navigation > Dropdown menu text color. This was only an issue when using white font setting for Main nav.
- Added Theme Editor options to hide/show product tabs on product page. Product Overview tab open by default.
- Added Theme Editor options to change mobile Nav icon colors. Found here: Mobile.

- BigCommerce Bug Report
- THEME-1890: Fix for: Vault – 2 deep level categories become unresponsive when using Simple Dropdown Menu display. This has been corrected. When simple dropdown setting is active, Flyout will work as expected and only display levels 1-3.
- THEME-1891: Fix for: Vault – Customizing theme to show product reviews results in hiding the reviews. This has been corrected so that when Theme Editor option within Products > Display Settings > “Show product reviews” is toggled it will hide/show accordingly.
- THEME-1894: Fix for: Vault – Category links in Mega Menu are unresponsive if they exceed 3 sub-categories deep. This has been corrected and tested using both simple & alternate menu settings.
- THEME-1851: Fix for: Vault 1.0.5 – Special characters in Brand name appear at front of string in menu. This has been corrected with style added to set direction: ltr;

- Core files updated with files from Cornerstone 4.2.1
- .travis.yml
- Gemfile
- Gemfile.lock
- Gruntfile.js
- karma.conf.js
- lighthouse-config.js
- package-lock.json
- package.json
- stencil.conf.js
- webpack.common.js
- webpack.dev.js
- webpack.prod.js

- AMP files updated with files from Cornerstone 4.2.1
- /templates/components/amp
- /templates/layout/amp-iframe.html
- /templates/layout/amp.html
- /templates/pages/amp

- JS files updated with files from Cornerstone 4.2.1
- /assets/js

- SCSS files updated with files from Cornerstone 4.2.1
- All with exception to vault.scss & custom.scss

- Custom Template files updated with responsive-img code from Cornerstone 4.2.1
- /templates/products/card.html (responsive-img code added)
- /templates/layout/base.html: (script calls within head section above {{ getFontsCollection }} updated so lazyload product images will be visible on all product cards)
- /templates/layout/blog.html: (script calls within head section above {{ getFontsCollection }} updated so lazyload product images will be visible on all product cards)
- /templates/layout/checkout.html: (script calls within head section above {{ getFontsCollection }} updated so lazyload product images will be visible on all product cards)
- /templates/layout/home.html: (script calls within head section above {{ getFontsCollection }} updated so lazyload product images will be visible on all product cards)
- /templates/layout/product.html: (script calls within head section above {{ getFontsCollection }} updated so lazyload product images will be visible on all product cards)
- /templates/components/carousel.html (responsive-img code added)
- /templates/components/cart/content.html (responsive-img code added)
- /templates/components/cart/preview.html (responsive-img code added)
- /templates/components/common/cart-preview.html (responsive-img code added)
- /templates/components/products/list-item.html (responsive-img code added)
- /templates/components/products/modals/writeReview.html (responsive-img code added)
- /templates/components/products/options/product-list.html (responsive-img code added)
- /templates/components/products/product-view.html (responsive-img code added)
- /templates/pages/brand.html (responsive-img code added)
- /templates/pages/brands.html (responsive-img code added)
- /templates/pages/category.html (responsive-img code added)
- /templates/pages/compare.html (responsive-img code added)
- /templates/components/account/order-contents.html (responsive-img code added)
- /templates/components/account/orders-list.html (responsive-img code added)
- /templates/components/account (responsive-img code added)
- /templates/components/account/returns-list.html (responsive-img code added)
- /templates/components/blog/post-page.html (responsive-img code added)
- /templates/components/blog/post-post.html (responsive-img code added)



## Draft
## 1.0.6 (2019-09-06)
- BigCommerce Bug Report
- THEME-1829: Fix for: Subcategory image grid shows gaps when subcategory title occupies more than one line of text. Increased min height in stylesheet to correct the spacing issue when category title is more than one line.
- THEME-1832: Fix for: Next Button on Product Reviews does not work properly. Added custom jquery to scroll to and then activate the reviews tab when review pagination is clicked after page is loaded.
- THEME-1845: Fix for: Dropdown menu color cannot be modified. Active dropdown and active parent background color can now be controlled within Theme Editor found here: Main Navigation > Dropdown menu background. Default is set to white on all 3 variations.
- THEME-1797: Fix for on 6/21/19 in version 1.0.4. Incorrect auto-capitalization in place on Contact Form comment box. Removed text-transform: capitalize; rule from .form-input.
- THEME-1794: Fix for: Undersized Amazon Pay button on add to cart pop-up. Set amazonpay button height to inital in vault stylesheet.
- THEME-1816: Fix for: Out of Stock message unreadable due to inherit Theme Colors. Adjusted alertbox background-color for inventory out of stock notifications on product page when tracking inventory levels by options so that they are visible and readable.

- BigCommerce jQuery Version Update Request
- We have updated all jQuery versions to 3.4.1 and removed all unnecessary/duplicate jQuery calls. One hard-coded reference within the footer must remain due to conditional handlebar statements within custom jQuery, but has been updated to version 3.4.1.

- Updated call to 3.4.1: https://github.com/bigcommerce-themes/lonestar-vault/blob/master/templates/components/common/footer.html#L149
- ALL CALLS REMOVED: https://github.com/bigcommerce-themes/lonestar-vault/blob/master/templates/layout/base.html#L66
- ALL CALLS REMOVED: https://github.com/bigcommerce-themes/lonestar-vault/blob/master/templates/layout/blog.html#L66
- ALL CALLS REMOVED: https://github.com/bigcommerce-themes/lonestar-vault/blob/master/templates/layout/checkout.html#L58
- ALL CALLS REMOVED: https://github.com/bigcommerce-themes/lonestar-vault/blob/master/templates/layout/product.html#L65


## 1.0.5 (2019-06-28)
- Many revisions listed in the previous version (1.0.4) did not make it into the update so this version includes everything mentioned
in 1.0.4 as well as the following.
- Search placeholder changed to simply read "Search".
- Added Theme Editor option to toggle "Created by Lone Star Templates" within Footer.
- iPad hero images will now stretch full-width.


## 1.0.4 (2019-06-21)
- Fix for top of hero carousel being cut off. There was a negative margin set on the heroCarousel class, which has now been removed.
- Mega Nav button: Shop & burger icon hover color in main nav can now be modified using the setting in the theme editor located here: Header & Footer > Mega Navigation > Hover / Active color.
- All hover & active colors within the Mega Nav dropdown & flyout can now be modified using a single setting in the theme editor located here: Header & Footer > Mega Navigation > Hover / Active color.
- Top border color for sticky nav can now me modified in the theme editor located here: Header & Footer > Sticky Navigation > Sticky nav top-border color.
- Cleaned up the organization of theme editor options within the Header & Footer section.
- Added Theme Editor option for phone number color & phone number hover color in Main Navigation found here: Header & Footer > Main Navigation > Phone Number color, Phone Number hover color.
- Added Theme Editor option for cart counter color found here: Header & Footer > Main Navigation > Cart counter color.
- Mobile menu will now show all categories beyond 8.
- Added Theme Editor options to edit all colors and hover colors within the QuickSearch Results product cards found here: Products > Product cards (quick search).
- Adjusted option:checked color within config file so that selected color swatch on product page is apparent.
- Adjusted option:checked color within config file so that checkmark for product options is visible.
- Adjusted alertbox background-color for inventory out of stock notifications on product page when tracking inventory levels by options so that they are visible and readable.
- Character limits within text fields will now show a popup error when set requirements are not met after clicking add to cart button.
- Updated input-font-color within config.json file to #2f2f2b for all variations just like “Bright” variation so that text is more visible.
- Removed text-transform: capitalize; rule from .form-input.
- Qty increment / decrement boxes styling cleaned up.
- Updated js library, package.json, all webpack files, karma.config.js, manifest.json, & amp files to Cornerstone version 3.5.0
- THEME-1787: Fix for blog image overlapping blog text.

## 1.0.3 (2019-06-04)
- used specificity to ensure that our styles with the class of header refer only to the actual header. This was done in case the class header is used within the body as it was causing z-index issues with the flyout nav.
- z-index fix for mobile close action. This was an issue if at the top of the page.

## 1.0.2 (2019-05-29)
- Featured Banner fixes for Cool and Natural Variations within Theme Editor.
- z-index fixes for dropdowns within header and main navigation. There were certain scenarios where z-indexes were competing.

## 1.0.1 (2019-05-24)
- Correction of misspellings within meta images
- Fix for second-level categories within flyout. Removed collapsible attribute so that when clicked they will now go to their correct url.

## 1.0.0 (2019-05-23)
- Initial Launch
