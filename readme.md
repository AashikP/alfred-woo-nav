## Credits 

* Inspired by WPCOM workflow by Chris
* Workflow icon: https://www.iconfinder.com/icons/211784/navigate_icon

## WooCommerce Navigation Workflow

### What's this?

This Alfred workflow to guide user to navigate WooCommerce configuration option by pasting the path to the front most app on your mac.


### Is it useful to me?

Only if your work includes sending instructions on accessing various WooCommerce features and configuration options :) 

## Setup

1. Download `WooCommerce Navigation.alfredworkflow`
2. Install the workflow on your device
3. Search for navigation paths by `wn YOUR_QUERY`


## Usage

### `wn YOUR_QUERY`

* By default, the keyword is set to `wn` for stock configuration options
* Eg: If you want to search for the configuration path for `Hold Stock`, launch alfred and type `wn hold stock`:
    ![https://d.pr/i/1Loer6+](https://d.pr/i/1Loer6+)
* Output would be: `WooCommerce > Settings > Products > Inventory > Hold stock (minutes) > Define - Hold Stock in minutes`

### `wnb YOUR_QUERY`

* Same as `wn`. Only difference is that the output would be bold (markdown)
* Eg: The same query above, using `wnb` results in: `**WooCommerce > Settings > Products > Inventory > Hold stock (minutes) > Define - Hold Stock in minutes**`

### `wns YOUR_QUERY`

* Same as `wn`. Output is bold (HTML).
* Eg: The same query above, using `wns` results in: `<strong>WooCommerce > Settings > Products > Inventory > Hold stock (minutes) > Define - Hold Stock in minutes**</strong>`

### `wnca NAME|PATH`

* This would add a new, custom navigation path to a separate db table
* Make sure that the custom path does not have the same name as any of the existing stock names. This is because the workflow only searches the custom database if there are no results found for your query in stock database
* Custom path is saved in a different table so that if there's an update to this workflow in the future, your custom paths are not lost

### `wncr NAME` or `wncr PATH`

* Removes the custom name|path combination that you've added
* **This is irreversible** as there's no backup of custom table anywhere outside of your device
* Please also note that **there is no warning** prior to removing a custom item

### Is there a way to add `WP Admin` prefix to the navigation path?

Use `wpn YOUR_QUERY` instead of `wn YOUR_QUERY` and the results would include `WP Admin >` appended to the start. You can also use `wpnb YOUR_QUERY` and `wpns YOUR_QUERY` to obtain the results in bold format as Markdown or HTML respectively


### What about the [upcoming changes in WooCommerce navigation](https://developer.woocommerce.com/2021/01/15/call-to-action-create-access-for-your-extension-in-the-new-woocommerce-navigation/)?
Use `wnn YOUR_QUERY` instead of `wn YOUR_QUERY` and the results would be in the new WooCommerce Navigation format. You can also use `wnnb YOUR_QUERY` and `wnns YOUR_QUERY` to obtain the results in bold format as Markdown or HTML respectively


## How to update?

* **If you don't have any custom navigation paths added:** just delete the existing workflow, and install new one

* **If you have custom navigation paths added:**
    1. Right-click on workflow and open the folder in finder
    2. Copy the `custom.db` file to a different folder
    3. Delete the workflow
    4. Install the latest version of workflow
    5. Open the workflow folder in finder, and replae the `custom.db` file with the one you copied in `step 2`.
    6. All your custom path should now be retained.

### Changelog

#### 1.3.0

* Added support for new [WooCommerce Navigation](https://developer.woocommerce.com/2021/01/15/call-to-action-create-access-for-your-extension-in-the-new-woocommerce-navigation/).

#### 1.2

* Updated navigation paths to reflect the changes to Coupon path (Marketing > Coupon)
* Default queries don't include WP Admin now.
* CSV file names changed.