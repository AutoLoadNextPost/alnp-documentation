# Auto Load Next Post Documentation

## Repeater Template

Auto Load Next Post uses a templating system referred to as a **Repeater Template** to manage the front-end display of your Ajax loaded content.

The [repeater template](https://github.com/autoloadnextpost/auto-load-next-post/blob/master/template/content-alnp.php) is a file that will execute over and over to display post content within ALNP loop. This template will look for and load the appropiate template files according to your theme using core WordPress functions such as `locate_template()` and `get_template_part()` to load in the content.

However, should the default repeater template not be suited to your theme structure, it can be overridden by copying it from the plugin directory `wp-content/plugins/auto-load-next-post/template/content-alnp.php` to `wp-content/themes/yourtheme/auto-load-next-post/content-alnp.php`

1. Create an `auto-load-next-post` directory in the root of your current theme folder.
2. Copy and paste `content-alnp.php` in the newly created `auto-load-next-post` directory.
3. Update the new `content-alnp.php` file however you wish. It will not be overwritten when the plugin is updated.

When making the modifications to your repeater template file, make sure it matches your theme structure and loads the content for a single post. The same if you were supporting a child-theme.

> ✏️ Note: Overriding the repeater template is not always required. You may find that just using the [alnp_template_location](https://github.com/autoloadnextpost/alnp-documentation/blob/master/en_US/filter-hooks.md#filter-alnp_template_location) filter is all that you need to support Auto Load Next Post in your theme.

In the default repeater template there are [action hooks](https://github.com/autoloadnextpost/alnp-documentation/blob/master/en_US/action-hooks.md) that can be used to display before and after the loop and content.

---

If you have any issues with this guide, or the documentation that is linked throughout, please [open a new issue](https://github.com/autoloadnextpost/alnp-documentation/issues/new) in this repository for it to be reviewed. Thank you!